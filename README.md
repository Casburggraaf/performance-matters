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
Or see [Detail page](http://htmlpreview.github.io/?https://github.com/Casburggraaf/performance-matters/blob/master/sitespeed-result/localhost/2018-03-15-14-18-04/detailed.html)

#### CSS and JS Minification ([minify](https://github.com/Casburggraaf/performance-matters/tree/feature/minify))
This test is runned with minifycation of css and js, with the tool[minifier](https://github.com/fizker/minifier) .
The Changes are minimal but this practice is a easy win without any setbacks
![alt text](sitespeed-result/test_images/test_minify.png "minify test")
Or see [Detail page](http://htmlpreview.github.io/?https://github.com/Casburggraaf/performance-matters/blob/master/sitespeed-result/localhost/2018-03-15-14-43-37/detailed.html)

#### Subse Fonts ([subset-fonts](https://github.com/Casburggraaf/performance-matters/tree/feature/subset-fonts))
This test is runned with the subset of the fonts, this delets al characters that are not latin. The woff2 fonts are improved from 31 and 77 kb to 12 and 13kb with is a improvement of 61 and 73 %. The tool i used is  [transfonter](https://transfonter.org/) .
![alt text](sitespeed-result/test_images/test_subset-font.png "subset font test")
Or see [Detail page](http://htmlpreview.github.io/?https://github.com/Casburggraaf/performance-matters/blob/master/sitespeed-result/localhost/2018-03-16-11-30-22/detailed.html)

#### Async css ([async-css ](https://github.com/Casburggraaf/performance-matters/tree/feature/async-css))
This test is runned with async-css. The used the method discribed by [filamentgroup](https://www.filamentgroup.com/lab/async-css.html) .
![alt text](sitespeed-result/test_images/test_async-css.png "Async Css test")
Or see [Detail page](http://htmlpreview.github.io/?https://github.com/Casburggraaf/performance-matters/blob/master/sitespeed-result/localhost/2018-03-16-11-47-03/detailed.html)

#### Critical Css ([Critical Css](https://github.com/Casburggraaf/performance-matters/tree/feature/critical-css))
This test is runned with critical css and async-css. Otherwise the critcal css wont do anything. I used  [penthouse](https://github.com/pocketjoso/penthousel) to genarate the critical css .
![alt text](sitespeed-result/test_images/test_critical-css.png "critical Css test")
Or see [Detail page](http://htmlpreview.github.io/?https://github.com/Casburggraaf/performance-matters/blob/master/sitespeed-result/localhost/2018-03-16-12-32-23/detailed.html)

#### All improvement ([all improvement](https://github.com/Casburggraaf/performance-matters/tree/feature/all-improvents))

![alt text](sitespeed-result/test_images/test_all-improvement.png "all improvement")
Or see [Detail page](http://htmlpreview.github.io/?https://github.com/Casburggraaf/performance-matters/blob/master/sitespeed-result/localhost/2018-03-16-13-00-30/detailed.html)

### ToDo improvements

- Gzip(besides it's (serverside)[https://github.com/expressjs/compression])
- Image compression
- Client Hints
- Fonts Async
- Picture elements
