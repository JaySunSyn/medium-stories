[![Build Status](https://travis-ci.org/JaySunSyn/medium-stories.svg?branch=master)](https://travis-ci.org/JaySunSyn/medium-stories)
[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/jaysunsyn/medium-stories)

# \<medium-stories\>

Displays the latest stories of your medium account.

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