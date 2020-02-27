##SASS
-extension to css (can use variables, functions and conditionals)
-written in Ruby
-needs to be translated into css

##INSTALL
-install ruby
-standalone app (prepros)

##VARIABLES
```
-start with $
($mainColor: #fff;)
```

##CLEAR FIX TECHNIC
```
:after{
content: "";
display: block;
clear:both;
}
```
##MIXINS

-chunk of reusable css, that can be injected anywhere
```
@mixin mixin-name {
}
```

-to apply mixin:
```
where-to-include {
@include mixin-name;
}
```

##IMPORT EXTERNAL SASS FILES INTO MAIN SASS FILE

-to make code cleaner it is possible to create diff files for variables,
mixins, etc.

@import "file name"; - thats gonna look for external sass file

##PSEUDO CLASSES 
```
.some-class {
     &:hover {
     }
}
```
##MATH OPERATORS 
-math equations can be passed as size rules
-foe ex: if you want a list of element to take up 100% width
 and each element to be equal in width
width: (100% / number of elements)

##MATH GRID
EX from NetNinja tutorial:
```
@mixin grid($cols, $mgn){
  float: left;
  width: ((100% - (($cols - 1) * $mgn)) / $cols );
  margin-right: $mgn;
  margin-bottom: $mgn;
  &:nth-child(#{$cols}n){
    margin-right: 0;
  }
} 
```

```
#projects li{
  @include grid(6, 2%);
  img{
    width: 100%;
  }
}
```

##COLOR FUNCTIONS
-list of built-in functions:
https://sass-lang.com/documentation/modules
