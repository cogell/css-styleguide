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

## Other Styleguides
BEM, SMACCS, OOCSS, etc - Doesn't really matter what you use **just use something**.



## References and Inspirations

- [Opt-in Typography](http://css-tricks.com/opt-in-typography/)
- [Used and Abused – CSS Inheritance and Our Misuse of the Cascade](http://www.phase2technology.com/blog/used-and-abused-css-inheritance-and-our-misuse-of-the-cascade/)
