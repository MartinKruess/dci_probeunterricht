# Basic infos about SCSS/SASS ?
SCSS can be described as advanced CSS, which is used to affect the look of websites. A term related to SCSS is SASS. While the ***SASS syntax*** gets by with ***indentation*** and without the curly brackets and semicolons common in CSS, the syntax of SCSS is similar to that of CSS. SCSS is often referred to as the more modern syntax.

In order for SASS to be understood by a browser, the code must first be converted to CSS. That's why SASS is called a ***preprocessor***.

In contrast to CSS, SASS offers various functions that make it easier to write CSS statements.

Due to the development of SASS, the use of SCSS is also possible. The syntax used is recognized automatically.
```
npm i sass
```

## functions

**Variables:** SASS allows information to be stored in variables and reused in different places. Variables are useful, for example, to use fonts, font sizes, colors and other values ​​consistently across the website.

**Nesting:** SASS allows classes and pseudo-classes to be nested, which reduces redundancy and writes less. The BEM methodology1 is also supported.

**Arithmetic operations:** In SASS, simple calculations such as +, -, * and / can be performed.

**Flow control:** SASS knows loops and case distinctions with which repetitions and if/then rules can be implemented.

**Functions, Mixins and Extend:** A @function can be fed with values, which it processes and finally returns the result. A @mixin works similar to an @function, but differs in that it returns CSS instead of a value. @extend allows different CSS classes to share properties with each other.

**Imports:** The SASS @import and @use commands allow the code to be split into subfiles, which allows the code to be better structured and reused in other contexts. In contrast to the CSS import command, no additional HTTP request is generated when the page is called up.

**Advantages of SCSS/Sass over CSS**
- additional functions
- reduction of redundancy (avoids double code)
- high modularity (reusability)


---
## Differences between SCSS and SASS

### SCSS - Sassy CSS

- newer syntax
- similar to CSS syntax
- Default

```
.Container{
  float: left;
  width: 100%;

  p{
    color: #111;
  }
}
```

### SASS - Syntactically Awesome Style Sheets

- original syntax
- shorter syntax

SASS example:

```
.Container
  float: left
  width: 100%

  p
    colour: #111
```

---

### CSS / SCSS / SASS - Syntax and functions

| CSS | SCSS | SASS |
|---|---|---|
| braces & semicolons | braces & semicolons | indentation |
| Spaces are ignored | Spaces are ignored | Strict rules about spaces |
| x | @example-mixin | =example-mixin |
| x | @include example-mixin | +example-mixin |
| x | @import foo | @import foo (same) |
| x | @extend foo | @extend foo (same) |


---

### Mixin - How does it work?

In contrast to variables, which work globally, mixins are a kind of predefined and reusable pattern of CSS attributes that, similar to a function, outputs them via ```@include```.

```
@mixinflex{
    display: flexible;
    display: -webkit-flex;
  }
```



## How to work with SCSS/SASS ?

1. First we initialize git

```
  git init
```

2. SASS and SCSS installation
```
  npm i sass
```

3. Our first simple mixin

```
@mixinflex{
    display: flexible;
    display: -webkit-flex;
    flex wrap: wrap;
  }
```

4. We create global variables
```
//CSS
--primary-color: #ededed; //bg-color
--secondary-color: #242628; //font color

//SCSS
$primary-color: #ededed; //bg-color
$secondary-color: #242628; //font color
```
5. What are partials and how are they used?
Partials are files that are ignored by the compiler until they are imported into a compilable file.
**Important:** To prevent partials from being compiled, you need a prefix before the actual file name. *_name* with the *_* the file is ignored.


```
@mixin border{
    border: solid 2px red;
    border-radius: 1rem;
  }
```

```
@import "./partials/mixin";
```
6. Style the buttons and the paragraph using a mixin within the ***main.scss***.
Use global variables to set padding and margin.

7. Now try to store the finished mixin in ***_mixin.scss*** and import the mixin into *main.scss*.






Quellen:

https://www.npmjs.com/package/sass (Dokumentation)

https://www.youtube.com/watch?v=3wXqwX4nu8I (English)

https://www.youtube.com/watch?v=Vyp3Nh0QvSk&list=PLNmsVeXQZj7oopYYGy5hX-Y6b07_3DPp5 (German)