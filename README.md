# Vendor-Mixins
Set of SaaS-Syntax mixins providing cross-browser compatibility.
***

# Cross-Browser compatibility
It is widely known that when you create your CSS you have to care about cross-browser compatibility.
As most of the CSS properties are "universal" (works the same way in all popular browsers), they are some no fully compatible.
Let's focus on these. 
We can divide them into two groups:
- Totally incompatible
- Compatible with vendor prefix

If it comes about totally incompatible we can't do anything excluding replacing them by another propeties/ideas.
But we are able to make our CSS more compatible cross-browser by using vendor prefixes.

# Vendor prefixes
If you don't know what vendor prefixes are you will find out now.

Example:
    When you want make your div's corners rounded the simplest solution is using "border-radius" CSS property.
    Following CSS code might looks like this:
    
    ```css
    #radius {
        border-radius: 5px;
    }
    ```
