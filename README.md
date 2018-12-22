# Blog
For documentation: https://help.github.com/articles/using-jekyll-as-a-static-site-generator-with-github-pages/

### To work with hexo

```yarn global add hexo-cli```

After that: https://hexo.io/docs/setup.html

```
$ hexo init <folder> #For new projects
$ cd <folder>
$ npm install
```

### Initializing this Repo

* Clone repo
* Checkout already existing submodules in this project:
```
git submodule update --init --recursive
```
* Add optional plugins for theme-next (out of source-control)
```
git clone https://github.com/theme-next/theme-next-fancybox3 theme/next/source/lib/fancybox
```

##### Use Hexo Admin
```
hexo server -d
```
Open [http://localhost:4000/admin/](http://localhost:4000/admin/)

### One Shot Commit/Deploy

`gaa; gcm "adding changes"; gp; hexo g; hexo d; `

## Quick Start

### Create a new post

``` bash
$ hexo new "My New Post"
```

More info: [Writing](https://hexo.io/docs/writing.html)

### Run server

``` bash
$ hexo server
```

More info: [Server](https://hexo.io/docs/server.html)

### Generate static files

``` bash
$ hexo generate
```

More info: [Generating](https://hexo.io/docs/generating.html)

### Deploy to remote sites

``` bash
$ hexo deploy
```

More info: [Deployment](https://hexo.io/docs/deployment.html)

### To add a submodule (hexo theme)
`git submodule add https://github.com/theme-next/hexo-theme-next themes/next` 

**Main documentation:** https://hexo.io/docs/

**Configuration:** https://hexo.io/docs/configuration.html
