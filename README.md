# StarBugs Weekly
[![Netlify Status](https://api.netlify.com/api/v1/badges/a1926bf8-7473-4fdb-bbb7-60740e2d89bb/deploy-status)](https://app.netlify.com/sites/recommend-starbugs/deploys)

- Recommend Website: https://recommend.starbugs.dev/
- Weekly Website: https://weekly.starbugs.dev/
- Blog Website: https://medium.com/starbugs
## Contribution

### Contribute recommend article

1. fork a current repository to your account
2. create a new issue via an issue template
3. add a new file to directory `posts/contribution`

### Contribute a conference

1. fork a current repository to your account
2. create a new issue via an issue template
3. add a new file to directory `posts/conference`

### Contribute an activity

1. fork a current repository to your account
2. create a new issue via an issue template
3. add a new file to directory `posts/activity`


### First-time contribution

If you contribute this repo first-time, you should add information to `_data/metadata.json` to keep the article working fine.

```json
  ...
  "contributors": {
    "starbugs": {
      "name": "starbugs",
      "intro": "星巴哥技術週刊",
      "avatarUrl": "/img/authors/starbugs_logo.png",
      "site": "https://weekly.starbugs.dev/"
    }
  },
  ...
```

1. Add your avatar to `img/authors`. 
2. create a personal post template for yourself
3. modify the name
4. The avatar should work on a post list, a post page, and the about page.

You could also see the [document of contribution detail](./contribution-detail.md). There are some images to help you understand the workflow.

## Development

```
npm install
npm run watch
```

## Deployment 

Deployment is trigger by release.

## Reference

- [Eleventy Documentation](https://www.11ty.dev/docs/collections/)
- [Nunjucks template document](https://mozilla.github.io/nunjucks/templating.html)

## the project forks from the following projects: 

- [Cymetrics Tech Blog](https://github.com/cymetrics/blog)
- [error-baker-blog](https://github.com/Lidemy/error-baker-blog) 
- [eleventy-high-performance-blog](https://github.com/google/eleventy-high-performance-blog)
