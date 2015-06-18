# simplePageScroll
This plugin prevents web browsers' default mouse wheel scroll actions and animate pages like slides.
Currently, it only has vertical scroll and may have other bugs, it's under construction.
I will try to finish it as soon as possible. A demo will be availble soon.

## Installation

You should include in your project [jquery.mousewheel.js](jquery.mousewheel.js) as dependency.
I added it in simplePageScroll.min.js so you don't need to do it if you use the minified version.
If you prefer to include yourself dependencies, you may download the version simplePageScroll.js not minified.

## Usage
1. Installation
2. write your html page as normally, give an ID to the slide wrapper and a class name to all slides in this wrapper.
3. Add CSS sytles to set sizes of the wrapper and the slides. For whole page slide show, you may set:
> html, body, #slideWrapper, .slide {
>     width:100%;
>     height: 100%;
> }
4. At the end of page body, initialize the plugin by:
> $("#slideWrapper").simplePageScroll({
>     slideTagName: ".slide",             // Default is 'slide'
>     slideContainer: "#slideContainer",  // The wrapper, default value is slideContainer
>     animationTime: 1000,                // Change page animation time
>     quietPeriod: 500,                   // Minimal duration between each slide change event 
>     keyboard: true,                     // Allow keyboard event to control the page scroll
>     pageSelectorID:"slide-btn",         //Only use this when you have a ul of li with buttons as page selectors
>     loop:true                           // Default as false, no more animation after the last page
> });

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