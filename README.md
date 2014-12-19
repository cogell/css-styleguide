# CSS Styleguide



## Rules
Don't forget. Rules are meant to be broken.

### Use a Preprocessor
tl;dr SASS with the libsass compiler

There are a number out there: LESS, SASS, Stylus, Rework.  Doesn't so much which just that you use something!  Each precompiler has their issues and tricks.

Notes:
- ATM, I don't like meaningful whitespace
- I've been bitten by many Stylus issues at work
- libsass compiler is less feature rich than its ruby brother but obviously much faster

### Components
tl;dr should be standalone, reusable, and have no knowledge of their parent container

Notes:
- should get their own file, maybe even their own directory

### Classes vs Tag Names
tl;dr add classes, don't tie presentation to tag names (break this rule sometimes)

### Class Naming Conventions
tl;dr BEM style `base__element--modifier`

### Tying Javascript to DOM Elements
tl;dr prefix all classes that javascript uses with `js-`

### Levels of Nesting
tl;dr only 3 levels at most, any more is hard to read

Nesting is inheritence so tread lightly. Here is a great quote from [@micahgodbolt](https://twitter.com/micahgodbolt)
> Avoid multiple inheritance at all costs, as it’s too complex to be useful reliably. If you’re stuck with it, then be prepared to know the class hierarchy and spend time finding where everything is coming from.

### Inheritence Vs. Composition
tl;dr there is nothing short and sweet about this discussion except the following quote from [Learn Ruby the Hard Way](http://learnrubythehardway.org/book/ex44.html#when-to-use-inheritance-or-composition)
> The thing to remember about object-oriented programming is that it is entirely a social convention programmers have created to package and share code.

### Single Colon vs Double Colon

#### Supporting IE*
Always use single colon.

#### Evergreen/modern browsers
Use single colon for puesdo **selectors** and use double colons for puesdo **elements** i.e. `::before` and `::after`


## Other Styleguides
BEM, SMACCS, OOCSS, etc - Doesn't really matter what you use **just use something**.

## Examples

### Global Button Module Inherited
**Q.** Is this good?
```
.button--primary {
  color: blue
  .admin & {
    color: black;
  }
}
```
**A.** Great question!

The `.admin` class/module is inheriting styling from `.button--primary`.  That inheritance breaks the modularity of `.admin`.  That being said this case is used often and I even do it (trying to quit that habit though).

The way to make this code more modular would be to write more code which is less DRY but more standalone.  We might write out a `.admin__button` class that **may** be similar to `.button--primary` but at that cost we gain a decoupled module.  Perhaps both modules `.button--primary` and `.admin__button` would inherit from global theme variables with local fallbacks.

## References and Inspirations

- [Opt-in Typography](http://css-tricks.com/opt-in-typography/)
- [Used and Abused – CSS Inheritance and Our Misuse of the Cascade](http://www.phase2technology.com/blog/used-and-abused-css-inheritance-and-our-misuse-of-the-cascade/)
- [Learn Ruby the Hard Way](http://learnrubythehardway.org/book/ex44.html#when-to-use-inheritance-or-composition)
- [The single responsibility principle applied to CSS](http://csswizardry.com/2012/04/the-single-responsibility-principle-applied-to-css/)
