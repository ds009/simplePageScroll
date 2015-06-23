# simplePageScroll
This plugin prevents web browsers' default mouse wheel scroll actions and animate pages like slides.
Currently, it only has vertical scroll and may have other bugs, it's under construction.
I will try to finish it as soon as possible. A demo will be availble soon.
这个插件可以帮助实现网页幻灯片效果，鼠标滚轮和方向键可以控制翻页，也可以自由设定每页显示前后的动画。
还有很多功能有待完善，但因为时间问题只能一点点弄了，希望谅解。

## Installation
Download the script simplePageScroll and include it in your page, then use it following instructions below.
## Usage
1. Installation
2. write your html page as normally, give an ID to the slide wrapper and a class name to all slides in this wrapper.
3. Add CSS sytles to set sizes of the wrapper and the slides. For whole page slide show, you may set:
```
html, body, #slideWrapper, .slide {
    width:100%;
    height: 100%;
}
```
4. At the end of page body, initialize the plugin by:
```
$("#slideWrapper").simplePageScroll({
    slideTagName: ".slide",             // Default is 'slide'
    slideContainer: "#slideContainer",  // The wrapper, default value is slideContainer
    animationTime: 1000,                // Change page animation time
    quietPeriod: 500,                   // Minimal duration between each slide change event 
    keyboard: true,                     // Allow keyboard event to control the page scroll
    pageSelectorID:"slide-btn",         // Only use this when you have a ul of li with links(look at the example) as page selectors
    loop:true,                          // Default as false, no more animation after the last page
    doBeforeEach:"resetSomething"       //doBeforeEach and doAfterEach execute before/after each slide show
});
```
5. You can specify functions to each slide so that it can be executed before and after showing by adding `data-beforeSlideShow="functionName"` or `data-afterSlideShow="functionName"` to the slide definition.

An exemple of html page:
```
<div id="slideContainer">
    <div class="slide slide-1">
        <div >
            <p >Of course you can change style for each slide</p>
        </div>
    </div>
    <div class="slide slide-2" data-beforeSlideShow="sayHello">
        <p >function sayHello will be executed before the slide showing</p>
    </div>
    <div class="slide slide-3">
        <p>You can make animations in each slide by before/after slide show functions</p>
        <img src="xxx.svg"></img>
    </div>
</div>
<div>
<ul id="slide-btn">
    <li class="pageSelector">
        <a href="#" class="active"></a> <!--The plugin will change the active class automaitcally-->
    </li>
    <li class="pageSelector">
        <a href="#"> </a>
    </li>
    <li class="pageSelector">
        <a href="#"> </a>
    </li>
</ul>
</div>
```



## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

Thanks.

## Inspiration

I was inspired by the [onepage-scroll](https://github.com/peachananr/onepage-scroll) project.
It's a great plugin, however I find it kind of complicate and has too much css modification in the plugin.
So I began this project, it's not yet perfect, I will complete it soon.

## License

MIT: http://rem.mit-license.org