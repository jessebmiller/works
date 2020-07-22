# Prickle features

## Page layout and CSS

Prickle is layed out as a stack of full width blocks with columns set
within each allowing content to determine the flowlines

### CSS Classes

#### Blocks

* `v-flowline`: Full width viewport dependant height
* `c-flowline`: Full width content dependant height

#### Columns

Between the flowlines, columns are built from gutters, margins, and
columns. Prickle demands the design constraint of two margins and a
column with gutters defined as CSS padding or margins on these
classes.

Margin A + Column + Margin B = Viewport width

* `margin-a`: Viewport dependant width, viewport - (margin b + column)
* `margin-b`: Viewport dependant widtn, viewport - (margin a + column)
* `content`: Viewport dependant width, viewport - margin a + b
* `half-width`: 50% width with a gutter

#### Grid modules (future work)

Between flowlines and within a column space can be broken up further
relative to the bounding column and flowline or relative to the
viewport

### Default base layout and blocks

#### Partials

* `head.html`: Everything in the head element goes here. Static.

Inside the body (and page div) there are three partials each defining
a main flowline

* `header.html`: A "header" block in a `v-flowline` with a default
* `content.html`: A "content" block in a `c-flowline` with no default
* `footer.html`: A "footer" block in a `v-flowline` with a default

* `foot.html`: Hidden block for scripts and tags