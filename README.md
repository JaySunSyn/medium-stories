[![Build Status](https://travis-ci.org/JaySunSyn/medium-stories.svg?branch=master)](https://travis-ci.org/JaySunSyn/medium-stories)
[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/jaysunsyn/medium-stories)
[![Maintainability](https://api.codeclimate.com/v1/badges/33892f06bcbe36a4218f/maintainability)](https://codeclimate.com/github/JaySunSyn/medium-stories/maintainability)
<a href="https://codeclimate.com/github/JaySunSyn/medium-stories/test_coverage"><img src="https://api.codeclimate.com/v1/badges/33892f06bcbe36a4218f/test_coverage" /></a>

# \<medium-stories\>

A Polymer 2 element which displays the latest stories of your medium account.

![screen shot 2018-01-23 at 12 08 59](https://user-images.githubusercontent.com/5872432/35272843-e20c5140-0036-11e8-9e4c-ac6a32401803.png)

## Demo
<!--
```
<custom-element-demo>
  <template>
    <link rel="import" href="medium-strories.html">
    <medium-stories
        url="https://us-central1-todo-app-5ac02.cloudfunctions.net/medium">
    </medium-stories>
  </template>
</custom-element-demo>
```
-->
```html
<medium-stories url="https://us-central1-todo-app-5ac02.cloudfunctions.net/medium"></medium-stories>
```

## Get the URL
Medium does not offer an API to retrieve your medium stories. 

Luckily https://medium.com/@jalalio/latest?format=json returns json.

The problems: 

1. Medium prevents JSON hacking by putting this string in the beginning of the json `])}while(1);</x>`
2. They don't allow cross domain calls so our AJAX response gets rejected in the browser

The solution: [See here, I made it easy as pie](https://github.com/JaySunSyn/medium-firebase-proxy)
