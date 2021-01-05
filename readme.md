# HTML Style Guide for Itobuz HTML Project

## Library you can include
You can only use bootstrap 4. 

## Code pattern
- [Code reuse](#code-1)
- [No global CSS](#code-2)
- [Use two spacing for indentation and commented code ](#code-3)
- [Mobile first responsive pattern](#code-4)
- [Avoid float for layout](#code-5)
- [Avoid pseudo element for icon and background preview](#code-6)
- [Code splitting for stylesheet](#code-7)

## SEO and page speed
- [H1 tag per page only once](#seo-1)
- [Use Svg image](#seo-2)

## Browser support
All HTML need to be checked with Chrome, Firefox, Safari Edge, Native Edge

### Code reuse  <a id="code-1"></a>
Where you want to code re-use you can split into module specific style sheet. like for button button.css, for form you can use form.css. But do not make them global css

##### Bad 
```
button {}
```

##### good 
```
.button-large {}
.button-dark {}
```

### No global CSS  <a id="code-2"></a>
We can not use global css. That can conflict with existing style. You can use normalize but that is already include with bootstrap.

##### Bad 
```
body {}
p {}
button {}
```

##### good 
```
.font-roboto {
}
.section-1 p {}
.button-style-v1 {}
```

### Use two spacing for indentation <a id="code-3"></a>
For indentation we will use two spacing indentation. And add comment for section wise to easier understand. Avoid 4 space and tav indentation


### Mobile first responsive pattern <a id="code-4"></a>
Mobile first responsive pattern is mandatory. See it's importance https://medium.com/@Vincentxia77/what-is-mobile-first-design-why-its-important-how-to-make-it-7d3cf2e29d00

### Avoid float for layout <a id="code-5"></a>
Avoid float based layout. Bootstrap has powerful grid layout concept and they are using with flex. Flex has some better than float. We will use that. Also float have some buggy effect until you are not using clear:both :)
### Avoid pseudo element for icon and background preview <a id="code-6"></a>
This is required for lazy loading. you can not use pseudo element for icon and background preview. With pseudo element lazy load can not be implement. You can use extra dom element instead.

### Code splitting for stylesheet <a id="code-7"></a>
Code splitting is very important for re-use and maintain large codebase. So for that purpose we will use section specific styles into different stylesheet.

### H1 tag per page only once  <a id="seo-1"></a>

It is mandatory to use h1 tag only once per page. So it is good practice to avoid nested h1 styles. So that someone can alter with different heading tag when needed.

##### Bad 
```
.section h1 {}
```

##### good 
```
.section .title {}
```

### Use svg image  <a id="seo-2"></a>
When we are using Figma, we can export image as svg image. Where SVG **export applicable** use SVG image. We can export image as SVG if those graphics are vector. We can not export Raster image as SVG. Because of file size will be larger and that can not scalable.
