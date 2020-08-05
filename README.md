# Vue Progression Bar

Progression bar shows how much the user scrolled (progressed) from the beginning of the page.

## Installation

To install this package, use npm:
```
npm i vueprogressionbar --save
```
## Usage

Default example:

```
<template>
  <div id="app">
    <ProgressBar/>
  </div>
</template>

<script>

import ProgressBar from 'vueprogressionbar'
export default {
  name: 'App',
  components: {
    ProgressBar
  }
}
</script>
```
## Options
There are 3 options you can chose from:
* **Option 1:  rounded** - rounded bar edges (false by default)  ![Imgur](https://imgur.com/QtBrtJ0.png)
```
 <ProgressBar rounded/>
```
* **Option 2: size** (medium by default):
```
 <ProgressBar size="[small-big]"/>
 ```
small (5px height) ![img](https://imgur.com/IP9ezNU.png) 
medium (7px) ![img](https://imgur.com/9kNqOqB.png)
big (10px) ![img](https://imgur.com/Fs9nfbU.png)


* **Option 3: color** (blueish by default - #76ceff)
Ex:
```
 <ProgressBar color="red"/>
 ```
## CSS
```
.progress-bar-container{
    width: 100%;
    position: fixed;
}
.progress-bar{
    height: 100%;
    background-color: #76ceff;
    transition: 0.1s ease;
}
.progress-bar--small{
    height: 5px;
}
.progress-bar--medium{
    height: 7px;
}
.progress-bar--big{
    height: 10px;
}
.progress-bar--rounded{
    border-radius: 5px;
}

```
## Gif example
 ![gif](https://media.giphy.com/media/QvetFy5WqoWuuZPQzY/giphy.gif)