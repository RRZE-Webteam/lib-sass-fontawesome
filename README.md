# Library SASS with Font Awesome

This library is a Sass-powered version of [FontAwesome](http://fortawesome.github.io/Font-Awesome/) 
which is configured for several themes of the [RRZE-Webteam](https://github.com/RRZE-Webteam).

*  Font Awesome 4.6.1 by @davegandy - http://fontawesome.io - @fontawesome
*  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 
## Installation

Please use a [SASS Compiler](http://sass-lang.com) to regenerate the css
file font-awesome.css .


### SASS Compile Options

#### for compiling files to font-awesome.css

```sh
sass --style compact --compass --sourcemap=none sass/font-awesome.scss css/font-awesome.css
```


#### for compiling files to font-awesome.min.css

```sh
sass --style compressed --compass --sourcemap=none sass/font-awesome.scss css/font-awesome.min.css
```



## Upgrading to newer Awesome-Versions:

1. Get new version of [FontAwesome](http://fortawesome.github.io/Font-Awesome/) 
2. Unzip and
- copy  $UNZIPFOLDFER/fonts/*   to  fonts/fontawesome/
- copy  $UNZIPFOLDFER/sass/*   to  sass/
- copy  $UNZIPFOLDFER/css/*   to  css/
3. Edit sass/_variables and change this line to match the our font folder:
 $fa-font-path:        "../fonts/fontawesome" !default;
4. Due to problems in compiling with several SASS compilers, copy all icon-settings from css/font-awesome.css towards sass/_icons.scss
   If you compile sass later and your icons get a content: "[]" you did something wrong :)


### Using Netbeans

If you are using [Netbeans IDE](https://netbeans.org) we advise you for the following setting:

Projekt Properties -> CSS Preprocessors:

- Activate "Compile Sass Files on Save"
- "Watch":   I
-- Input /sass
-- Output /css
- "Compiler Options"

```sh
--style compact --compass --sourcemap=none
```

this will only compile css/font-awesome.css .

For getting css/font-awesome.min.css you could change the compiler options to compress.
Otherwise its faster to use the Netbeans Plugin [JS CSS Minify Compress](http://plugins.netbeans.org/plugin/49666/js-css-minify-compress)
to simply mimify css/font-awesome.css once you need.

    

