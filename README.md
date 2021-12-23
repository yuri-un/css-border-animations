# CSS Border Animation Methods

This repository represents a notebook of found and researched methods, from simple to complex and difficult, allowing to implement different border animation effects. This design technique can be quite effective in developing and building different interactive UI for a purpose to focus user attention to different stances of a process. Can be used to submit as different Drag&Drop elements up to different popup modal dialog windows.


## Using Border Colors
* Pros: easy to implement, CSS style is well configurable.

* Cons: limited animation posibilities.

HTML:
```html
        <div class="section sample-1">
            <h2>Using Border Colors</h2>
            <p>          
                <b>Pros:</b> easy to implement, CSS style is well configurable.
            </p>
            <p>
                <b>Cons:</b> limited animation posibilities.
            </p>
        </div>
```

CSS:
```css
.sample-1{
    border:5px solid transparent;

    animation-name:color-animation;
    animation-duration:3s;
    animation-iteration-count:infinite;
}

@keyframes color-animation{
    0%{border-color:#eaebed}
    50%{border-color:#006989}
    100%{border-color:#eaebed}
}
```


##  Using Border Styles
* Pros: easy to implement, CSS style is well configurable.

* Cons: limited animation posibilities.

HTML:
```html
        <div class="section sample-2">
            <h2>Using Border Styles</h2>
            <p>
                <b>Pros:</b> easy to implement, CSS style is well configurable.
            </p>
            <p>
                <b>Cons:</b> limited animation posibilities.
            </p>
        </div>
```

CSS:
```css
.sample-2{
    border:5px solid transparent;

    animation-name:style-animation;
    animation-duration:3s;
    animation-iteration-count:infinite;
}

@keyframes style-animation{
    0%{border:5px solid #006989;}
    50%{border:5px double #006989;}
    100%{border:5px solid #006989;}
}
```


## Using Border Sides
* Pros: easy to implement, CSS style is well configurable.

* Cons: limited animation posibilities.

```html
        <div class="section sample-3">
            <h2>Using Border Sides</h2>
            <p>
                <b>Pros:</b> easy to implement, CSS style is well configurable.
            </p>
            <p>
                <b>Cons:</b> limited animation posibilities.
            </p>
        </div>
```

```css
.sample-3{
    border:5px solid transparent;

    animation-name:border-side-animation;
    animation-duration:2.5s;
    animation-fill-mode:none;
    animation-iteration-count:infinite;
}

@keyframes border-side-animation{
    15%{border-top-color: #006989;}
    40%{border-right-color:#006989;}
    60%{border-bottom-color:#006989;}
    75%{border-left-color:#006989;}
}
```


## Using Border Image
* Pros: allows animations with different geometrical primitives and other uncommon animation styles, mediocre complexity.

* Cons: requires at least 4 image frames for a smooth animation, border can't be changed with CSS styles.

```html
        <div class="section sample-4">
            <h2>Using Border Image</h2>
            <p>
                <b>Pros:</b> allows animations with different geometrical primitives and other uncommon animation styles, mediocre complexity.
            </p>
            <p>
                <b>Cons:</b> requires at least 4 image frames for a smooth animation, border can't be changed with CSS styles.
            </p>
        </div>
```

```css
.sample-4{
    border:6px solid transparent;
    border-image-slice:3;
    border-image-repeat:round;

    animation-name:border-image-animation;
    animation-duration:.5s;
    animation-iteration-count:infinite;
}

@keyframes border-image-animation{
    0%{border-image-source:url(./res/fig-frame-1.png);}
    16.7%{border-image-source:url(./res/fig-frame-2.png);}
    33.4%{border-image-source:url(./res/fig-frame-3.png);}
    50.1%{border-image-source:url(./res/fig-frame-4.png);}
    66.8%{border-image-source:url(./res/fig-frame-5.png);}
    80%{border-image-source:url(./res/fig-frame-6.png);}
    100%{border-image-source:url(./res/fig-frame-1.png);}
}
```


## Using Background Image
* Pros: allows complex animation effects, mediocre complexity, easy to implement, CSS configuration.

* Cons: requires decent amount of frames for a smooth animation, possible border styles are limited.

```html
        <div class="section sample-5">
            <h2>Using Background Image</h2>
            <p>
                <b>Pros:</b> allows complex animation effects, mediocre complexity, easy to implement, CSS configuration.
            </p>
            <p>
                <b>Cons:</b> requires decent amount of frames for a smooth animation, possible border styles are limited.
            </p>
        </div>
```

```css
.sample-5{
    border:5px solid transparent;
    background-image: linear-gradient( white, white), repeating-linear-gradient(45deg, white 0px 10px, #006989 10px 20px);
    background-origin: border-box;
    background-clip: padding-box, border-box;

    animation-name:bg-image-animation;
    animation-duration:.6s;
    animation-iteration-count:infinite;
}

@keyframes bg-image-animation{
    0%{background-image: linear-gradient( white, white), repeating-linear-gradient(45deg, white 0px 10px, #006989 10px 20px);}
    33.3%{background-image: linear-gradient( white, white), repeating-linear-gradient(45deg, white 5px 15px,#006989 15px 25px);}
    66.6%{background-image: linear-gradient( white, white), repeating-linear-gradient(45deg, white 10px 20px, #006989 20px 30px);}
    100%{background-image: linear-gradient( white, white), repeating-linear-gradient(45deg, white 0px 10px, #006989 10px 20px);}
}
```


## Using  SVG
* Pros: allows any type of animation, SVG files can be imported as image, SVG element or background image.

* Cons: high complexity and difficulty, limited CSS configuration.

```html
        <div class="section sample-6">
            <h2>Using SVG</h2>
            <p>
                <b>Pros:</b> allows any type of animation, SVG files can be imported as image, SVG element or background image.
            </p>
            <p>
                <b>Cons:</b> high complexity and difficulty, limited CSS configuration.
            </p>
        </div>
```

```css
.sample-6{
    background-image:url(./res/clouds.svg);
    background-repeat:repeat-x;
    background-position:center top;
    background-size:contain;

    padding-top:80px;

    /* Outline is better suited with SVG BG than border */
    outline:5px solid #396B89;
    outline-offset:-1px;
}
```


## Using Nested Divs
* Pros: same to Using background image method.

* Cons: same to Using background image method.

```html
        <div class="section sample-7">
            <div class="inner">
                <h2>Using Nested Divs</h2>
                <p>
                    <b>Pros:</b> same to Using background image method.
                </p>
                <p>
                    <b>Cons:</b> same to Using background image method.
                </p>
            </div>
        </div>
```

```css
.sample-7{
    background-image:linear-gradient(30deg, #dde7ee, #396b89, #81a5ba, #323456, #dde7ee),
    linear-gradient(#dde7ee, #396b89);
    background-repeat:repeat-x;
    background-size:100% 100%; 
    border:1px solid #006980;

    animation-name:div-animation;
    animation-duration:10s;
    animation-iteration-count:infinite;

}

.sample-7 > .inner{
    position: relative;
    background-color:white;
    border:1px solid #006980;
    
    padding:1em;
}

@keyframes div-animation{
    0%{background-size:100% 250%;}
    50%{background-size:300% 150%;}
    100%{background-size:100% 250%;}
}
```


## Using Outline Style
* Pros: allows any CSS border animation, doesn't affect element box size.

* Cons: limited animation posibilities.

```html
        <div class="section sample-8">
            <h2>Using Outline Style</h2>
            <p>
                <b>Pros:</b> allows any CSS border animation, doesn't affect element box size.
            </p>
            <p>
                <b>Cons:</b> limited animation posibilities.
            </p>
        </div>
```

```css
.sample-8{
    border:1px solid transparent;
    outline: 2px solid #006989;
    outline-offset:1px;

    animation-name:outline-animation;
    animation-duration:1.2s;
    animation-iteration-count:infinite;
    animation-fill-mode:forwards;
}

@keyframes outline-animation{
    0%{outline-style:dotted;
        outline-offset:1px;}
    50%{outline-style:dashed;
        outline-offset:7px;
        border-color:#006989;}
    100%{outline-style:dotted;
        outline-offset:1px;}
}
```


##  Using Box Shadow
* Pros: allows any CSS box-shadow animation, doesn't affect element box size.

* Cons: isn't practical, limited animation posibilities.

```html
        <div class="section sample-9">
            <h2>Using Box Shadow</h2>
            <p>
                <b>Pros:</b> allows any CSS box-shadow animation, doesn't affect element box size.
            </p>
            <p>
                <b>Cons:</b> isn't practical, limited animation posibilities.
            </p>
```

```css
.sample-9{
    box-shadow: 0px 0px 10px 3px #006989;

    animation-name:shadow-animation;
    animation-duration:1.2s;
    animation-iteration-count:infinite;
}

@keyframes shadow-animation{
    0%{box-shadow:0px 0px 10px 0px #006989}
    50%{box-shadow:0px 0px 10px 4px #006989;}
    100%{box-shadow:0px 0px 10px 0px #006989}
}
```