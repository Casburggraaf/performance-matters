# Performance matters

## Project setup

This project serves an adapted version of the [Bootstrap documentation website](http://getbootstrap.com/). It is based on the [github pages branche of Bootstrap](https://github.com/twbs/bootstrap/tree/gh-pages).

Differences from actual Bootstrap documentation:

- Added custom webfont
- Removed third party scripts
- The src directory is served with [Express](https://expressjs.com/).
- Templating is done with [Nunjucks](https://mozilla.github.io/nunjucks/)

## Getting started

- Install dependencies: `npm install`
- Install Submodules: `git submodules init && git submodules update`
- Install packages for sitespeed `cd sitespeed && npm install`
- Serve: `npm start`
- Run speedtest `sitespeed/bin/sitespeed.js http://localhost:3004/`
- Expose localhost: `npm run expose`

## Performance improvements

#### First Test Run ([Master](https://github.com/Casburggraaf/performance-matters/tree/master))
This test is runned without any improvements.
![alt text](sitespeed-result/test_images/test_1.png "first test")
Or see [Result page](https://github.com/Casburggraaf/performance-matters/tree/master/sitespeed-result/localhost/2018-03-15-14-18-04/index.html)
