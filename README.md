# nickertdotdev

## GitHub Pages Release
```
git checkout master && git pull && git branch -D gh-pages && git checkout -b "gh-pages" && npm run build && touch dist/CNAME && echo "cameron.nickert.dev" > dist/CNAME && git add dist -f && git commit -m "release" && git push origin --delete gh-pages && git subtree push --prefix dist origin gh-pages
```

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
