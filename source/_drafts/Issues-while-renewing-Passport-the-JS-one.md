---
title: Issues while renewing Passport - the JS one
tags: [web, authentication, rant, express]
---
No, am not talking about my actual passport, which also needs to be renewed soon by the way. Am talking about PassportJS.

Continuing my rant over the not so good login infrastructure avaible - the following were the gotchas we faced while implementing passportjs:

1. Passport requires a callbackURL when initialzing it. Thanks to https://github.com/jaredhanson/passport-facebook/issues/2 we found out it could also be specified while calling the strategy.
1. Passport assumes the developer will do most of the route wiring. A very important prerequisite is the flow of control in it's documentation. Hint - it's not there. Found a great blog post detailing the same: http://toon.io/understanding-passportjs-authentication-flow/


And now for the cool features of Passport that weren't that obvious at first:
1. **Normalized profiles**: When authenticating using a third-party service such as Facebook or Twitter, user profile information is often available. Each service tends to have a different way of encoding this information. To make integration easier, Passport [normalizes profile information](http://passportjs.org/docs/profile).
1. Probably not the place for this, but express supports [callback chaining](http://expressjs.com/en/api.html#router.METHOD). So potentially before the final route callback we can put many as many authentication/authorization callbacks as we want.  Eg: 
   ``` 
   router.get(
     '/authenticated/route/', 
     (req, res, next)=>{doAuthentication(); next();},
     (req, res, next)=>{doAuthorization(); next();},
     (req, res, next)=>{res.render(page);},
   );
   ```
   which is what passport.authenticate is - one of these callbacks
