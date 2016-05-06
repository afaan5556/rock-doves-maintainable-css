# Research Findings

## Article 1: Performance & Organization

* Increased website performance - 80/20 rule generally applies
* Personal preference prevails, but some general guidelines are universal (directory structure for common base styles, user interface components, and modules for example)
* Think about websites rather than individual pages

### OOCSS
Centers around:
* separating skin from structure
* separating content from container

### Scalable & Modular CSS Architecture
Break styles into 5 categories:
* Base
  * Layout
  * Module
  * State
  * Theme
* Keep selectors short!
* Favor classes
* Compression can be measured
* **Sprite images**

## Article 2: MindBEMding - Getting Your Head 'round BEM syntax'

#### BEM = Block, Element, Modifier
Smart way of naming your CSS classes to give more transparency and meaning to other developers

**Try using**
.site-search {} /* Block */
.site-search__field {} /* Element */
.site-search--full {} /* Modifier */

**Another example**
.person {}
.person__hand {}
.person--female {}
.person--female__hand {}
.person__hand--left {}

* Ugly code better than non-maintainable/comprehensible code
* Knowing when to use BEM and when it isn't necessary

## Article 3: Challenging CSS Best Practices

Presents argument to move away from the **separation of concerns (SoC)** principle.
SoC deals with separation of the three layers:
* structure
* presentation
* behavior

**So no more .button class or .media class for example**

Atomic CSS - the smaller the unit, the more reusable and maintainable it is.
Example of **irreducible units**

`<div class="Bfc M-10">
    <a href="http://twitter.com/thierrykoblentz" class="Fl-start Mend-10">
        <img src="thierry.jpg" alt="me" width="40" />
    </a>
    <div class="Bfc Fz-s">
        @thierrykoblentz 14 minutes ago
    </div>
</div>`

`.Bfc {
    overflow: hidden;
    zoom: 1;
}
.M-10 {
    margin: 10px;
}
.Fl-start {
    float: left;
}
.Mend-10 {
    margin-right: 10px;
}
.Fz-s {
    font-size: smaller;
}`

`.Fl-start {
    float: right;
}
.Mend-10 {
    margin-left: 10px;
}`

[CSS Selector Cheat Sheet](http://docs.emmet.io/cheat-sheet/)

#### Bloat has to live somewhere

`<div class="sidebar">`
**vs**
`<div class="Fl-start Mend-10 W-25">`



