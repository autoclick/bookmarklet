# Webpage Snapshot Bookmarklet

This is a simple bookmarklet that captures any webpage and save as png image using HTML5 technologies.

![Bookmarklet Maker](https://autoclick.github.io/bookmarklet/drop.jpg) 

Under the hood it uses [Bookmarklet maker](https://autoclick.github.io/bookmarklet/bookmarklet-maker.html)
 to capture the webpage to canvas,
then we convert the content inside this canvas element to image file.

You may copy the text below and save as bookmark.
`javascript:!function()%7Bfunction%20e()%7Bthis&&this.parentNode&&this.parentNode.removeChild(this),html2canvas(document.body).then(function(e)%7Breturn%20new%20Promise(function(t)%7Be.toBlob(t)%7D)%7D).then(function(e)%7Bvar%20t=document.createElement(%22a%22);return%20t.href=URL.createObjectURL(e),t.download=document.title.replace(/%5B/%5C%7C%5C%5C%60~!@#%5C$%25%5C%5E&%5C*%5C+%5C-=_'%22%5C,%5C.:;%5D+/g,%22_%22)+%22_%22+(new%20Date).getTime()+%22.png%22,t.click(),new%20Promise(function(e)%7BsetTimeout(10,e,t)%7D)%7D).then(function(e)%7B0===e.href.indexOf(%22blob:%22)&&(URL.revokeObjectURL(e.href),e.href=%22###%22)%7D).catch(function(e)%7Bconsole.error(e),e.message&&alert(%22Failed%20to%20capture:%5Cn%22+e.message)%7D)%7Dif(window.html2canvas)return%20e();var%20t=document.createElement(%22script%22);t.onload=e,t.src=%22https://html2canvas.hertzen.com/dist/html2canvas.min.js%22,document.querySelector(%22head%22).appendChild(t)%7D()`

Then trigger this bookmark in any webpage you want to capture.
