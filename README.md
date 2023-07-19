# TC_WIKI
Teamcenter &amp; Active Workspace Wiki

[Wiki js 설치 가이드](Documents/INSTALLATION.md)

## Main Home CSS

```css
table.docuLinks {
  padding-left: 25px;
  padding-right: 25px;
  border: none!important;
  border-bottom: solid grey 1px!important;
  padding-bottom: 15px!important;
  border-radius: 0!important
}
table.docuLinks tr td {
  text-align: left;
  background-color: transparent!important;
  border: none!important
}
table.docuLinks caption {
  text-align: left;
  font-size: 1.6rem;
  font-weight: 600;
  margin-top: 10px;
  margin-bottom: 15px
}
table.docuLinks td::before {
  content: "📃 "
}
```


## Header Theme

Jquery 및 

```html
<script src="https://code.jquery.com/jquery-3.7.0.min.js"></script>
<script type="text/javascript">
/*! Table of Contents jQuery Plugin - jquery.toc * Copyright (c) 2013-2016 Nikhil Dabas * http://www.apache.org/licenses/LICENSE-2.0 */
!function(a){"use strict";var b=function(b){return this.each(function(){var c,d,e=a(this),f=e.data(),g=[e],h=this.tagName,i=0;c=a.extend({content:"body",headings:"h1,h2,h3"},{content:f.toc||void 0,headings:f.tocHeadings||void 0},b),d=c.headings.split(","),a(c.content).find(c.headings).attr("id",function(b,c){var d=function(a){0===a.length&&(a="?");for(var b=a.replace(/\s+/g,"_"),c="",d=1;null!==document.getElementById(b+c);)c="_"+d++;return b+c};return c||d(a(this).text())}).each(function(){var b=a(this),c=a.map(d,function(a,c){return b.is(a)?c:void 0})[0];if(c>i){var e=g[0].children("li:last")[0];e&&g.unshift(a("<"+h+"/>").appendTo(e))}else g.splice(0,Math.min(i-c,Math.max(g.length-1,0)));a("<li/>").appendTo(g[0]).append(a("<a/>").text(b.text()).attr("href","#"+b.attr("id"))),i=c})})},c=a.fn.toc;a.fn.toc=b,a.fn.toc.noConflict=function(){return a.fn.toc=c,this},a(function(){b.call(a("[data-toc]"))})}(window.jQuery);
</script>
<script type="text/javascript">
    $("#toc").toc();
</script>
```
