# HTML style guide
- [h1 tag per page only once](#h1-tag-per-page-only-once)


## h1 tag per page only once 
It is mandatory to use h1 tag only once per page. So it is good practice to avoid nested h1 styles. So that someone can alter with different heading tag when needed.

### Bad 
```
.section h1 {}
```

### good 
```
.section .title {}
```
