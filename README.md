# Vendor-Mixins
Set of SaaS-Syntax mixins providing cross-browser compatibility.
***

# Cross-Browser compatibility
It is widely known that when you create your CSS you have to care about cross-browser compatibility.
As most of the CSS properties are "universal" (works the same way in all popular browsers), they are some not fully compatible.
Let's focus on these. 
We can divide them into two groups:
- Totally incompatible
- Compatible with vendor prefix

If it comes about totally incompatible we can't do anything excluding replacing them by another propeties/ideas.
But we are able to make our CSS more cross-browser compatible by using vendor prefixes.
***

# Vendor prefixes
If you don't know what vendor prefixes are you will find out now.

For example when you want to make your div's corners rounded the simplest solution is using *"border-radius"* CSS property.
Following CSS code might looks like this:

**Pure CSS Syntax:**
```css
#radius {
    border-radius: 5px;
}
```

**SASS Syntax:**
```sass
#radius
    -moz-border-radius: 5px
    -webkit-border-radius: 5px
    border-radius: 5px
```

But looking on [**W3C Docs**](https://www.w3schools.com/cssref/css3_pr_border-radius.asp) *"border-radius"* property is incompatible with:
- **Chrome** < *5.0*
- **Firefox** < *4.0*
- **Safari** < *5.0*

But looking deeply feature of rounding corners was introduced earlier into those browsers but it was called differently (depending on the browser):
- **Chrome** >= *4.0* as *"-webkit-border-radius"*
- **Firefox** >= *3.0* as *"-moz-border-radius"*
- **Safari** >= *3.1* as *"-webkit-border-radius"*

So when we was to create more compatible CSS code, we have to do it like:

**Pure CSS Syntax:**
```css
#radius {
    -moz-border-radius: 5px;
    -webkit-border-radius: 5px;
    border-radius: 5px;
}
```

**SASS Syntax:**
```sass
#radius
    -moz-border-radius: 5px
    -webkit-border-radius: 5px
    border-radius: 5px
```

Now all browsers compatible with *"border-radius"* will ignore properties with prefixes while browsers which require the stuff like this will be able to handle it.

Various browser have their own prefixes:
- **Chrome:** *-webkit-*
- **Firefox:** *-moz-*
- **IE:** *-ms-*
- **Opera:** *-webkit-* **or** *-o-*
- **Safari:** *-webkit-*

*To be continued*