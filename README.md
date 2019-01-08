# New-Google-Page-Insight-Performance-Audits
New Google Page Insight Performance Audits

> <strong>Change Image tags to background images</strong> where ever applicable as these will load after the page loads, and especially when the elements are initially hidden not visible and are shown on some event or mouse hove or click. The background images will load automatically when an element is made visible.

> <strong>Load images as background image</strong> via CSS instead of image tags to reduce HTML nodes and also reduce initial load time.

> <strong>Avoid excessive depth/hierarchy of HTML elements</strong>, avoid nesting paragraphs and span tags. Remove empty nodes from your HTML document as they have no visual effect, like a empty &lt;ul&gt; or &lt;li&gt;. Also avoid using &lt;br&gt; &lt;hr&gt; and implement this using CSS, all styling should be done via CSS.

> <strong>Load Device specific CSS</strong>. Instead of creating one CSS for all devices try creating separate CSS files for each device, so  we may have one common CSS file and more than one device specific CSS files, this will also reduce the load time and render blocking of content form not loading unnecessary CSS. To implement this we have media attribute media attribute that matches the user's device. Example &lt;link media="screen and (min-width:500px)" ... /&gt;

> <strong>Remove unused CSS rules</strong> from stylesheets to reduce unnecessary bytes consumed by network activity and reduce CSS load time. This is a difficult part but worth doing.

> <strong>Offload popular open-source libraries</strong> to https://developers.google.com/speed/libraries Like For popular JS like jQuery use hosted files to off load these resources https://ajax.googleapis.com/ajax/libs/jquery/1.10.2/jquery.min.js

> <strong>Optimize main menu HTML</strong> to avoid and remove excessive HTML nodes to reduce HTML code depth, like avoid using span and nesting span elements in &lt;li&gt;. Also remove any blank &lt;li&gt; or &lt;ul&gt; nodes from the menu HTML code. And implement one HTML menu code for all devices and handle its appearance using CSS & Javascript.

> <strong>Reduce image resolution</strong> to make it as close possible to the visible dimensions of the image on the page. Like if an image will have a maximum size of 200x200 on any resolution then the actual image source should also be a 200x200 image or as close possible to this dimensions like a 220 x 230 or as close possible. Using large images like 600 x 450 will give you negative score on Mobile devices.

> <strong>Add async or defer to external JavaScript</strong> like Google analytics or GTM code or other tracking scripts that are added to the site

> <strong>Import common font-face from fonts.googleapis.com</strong> and also add (font-display: swap;) style attribute to the @font-face declaration. This will avoid render blocking that would cause from loading a font file, when swap font display is used the page will keep loading as usual and the font will apply as soon the font files are loaded. swap gives the font face an extremely small block period and an infinite swap period.

> <strong>Optimize images</strong> using the recommended libraries like jpegoptim, gifsicle, and optipng. This will reduce the image file size without visible impact to image quality. A separate research document has been written on GitHub for this: https://github.com/WibsoftTechnologies/Image-Optimization-Utilities-for-Website-Performance.

> <strong>Reduce Render-Blocking</strong>. Minimize the number of render-blocking external stylesheets and scripts upon which the page depends. So loading critical CSS and Scripts on first load and remaining can load after the page loaded. This is also a difficult one to implement in existing sites that are already developed but worth doing.

> <strong>Merge CSS and JavaScript</strong> files to reduce number of calls to the server, that will reduce time required to load external CSS and JavaScript.

> <strong>Minify HTML, CSS and JavaScript</strong>. There are many free extensions available and also open source core PHP libraries that can be used to minify these on the fly. One of the minify library is http://code.google.com/p/minify/, the latest version is at https://github.com/mrclay/minify now.

> <strong>Offscreen images</strong> are images that appear below the fold. Since users can't see offscreen images when they load a page, there's no reason to download the offscreen images as part of the initial page load. So we would download those images as soon the user scroll down the page, we can apply this strategy to your JS, HTML, CSS, and other resources as well.
