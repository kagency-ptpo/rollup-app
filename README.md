# rollup-app
A simple rollup application ready to be coded

For installing node dependencies

```
$ npm install

```
For installing image minificator (imagemin)

```
$ npm run preinstall

```


The application use scss which will be compile from assets/scss/main.scss to build/css/style.min.css from . This also happens for JS, which will be compiled from assets/js/main.js to build/js/ main.min.js.

Bootstrap 5 is included from node with partial _theme.scss. For customize the your website, just edit the _theme.scss

When you want to iclude images, please create a folder call "img" <b>in the root of the project</b>. All the images presents in the folder will be optimized in production version. If you want to customize the optimization preset, just edit the follow lines of code in the compress-images.mjs:

```
imageminMozjpeg({ quality: 80 }), //for jpeg images
imageminPngquant({ quality: [0.6, 0.8] }), //for png images

```

If you want to add more optimization images types, just import the right imagemin plugin in the compress-images.mjs.




For development version. Every changes will be watched in real time on localhost (js, scss and html).

```
$ npm run dev

```
For production version

```
$ npm run build

```
The production version will also minimize all the images inside /img folder.
