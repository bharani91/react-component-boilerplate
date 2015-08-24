# React Component Boilerplate

A boilerplate for creating React components. See [React Select Popover](http://github.com/bharani91/react-select-popover) for an example of this boilerplate in action.


The gulpfile includes ```gulp-connect``` and ```livereload``` so running the ```gulp``` command will start up a server that will render files in the ```example``` directory.

The files in the ```dist``` directory are meant to be used when the component is installed directly with a script tag ```<script src="dist/hello.js"></script>```, instead of installing it via npm.


Set the name of your component in the gulpfile
``` javascript

    var standalone = browserify('./src/scripts/components/hello.jsx', {
        standalone: 'Hello',
        extensions: ['.jsx']
    })
```


Include dependencies in ```package.json``` like so:
``` javascript

    "dependencies": {
        "react-onclickoutside": "^0.2.4"
    },
    "browserify-shim": {
        "classnames": "global:classNames",
        "react": "global:React",
        "react-onclickoutside": "global:OnClickOutside"
    }
```


###### Gulp Tasks
1. ```gulp```: Default task - watches for changes and runs browserify, scss and starts the webserver
2. ```gulp lib```: Copies the files from ```src``` into ```lib```
3. ```gulp dist```: Creates distributable version of JS & CSS. The generated files can be included directly in any other component via script/style tags.


----------

**[bharanim](https://www.resumonk.com/bharani) | [Twitter](http://twitter.com/bharani91)**