# LAYOUT

How things are positioned is important because you don't want people getting annoyed while looking at your ugly website. They could write you a mean email that hurts your feelings and really ruins your day.

So here we go. Here are the concepts that you need to know to lay out your page.

## BIG PICTURE

The location of things on a webpage is influenced by HTML and CSS.

HTML is what sets:

* the general order of elements on the page(this element comes before this other element)

* the organization of elements on the page(what elements are nested inside others)

CSS allows for more specific organization of your page with the use of properties.

Here are some important properties to know.

### DISPLAY PROPERTIES

#### Inline
Inline elements accept margin and padding but the element stays inline. The margin and padding will only push other elements horizonally away. Inline elements will not accept height and width. I think of them like cats. You can't really make them do much. They do what they want.

#### Inline-block
Now you *can* set a width and height on an inline-block. Also, make sure you don't say "heighth". People always say "heighth". It's *height*. You're welcome. These elements will set inline on the baseline, which I think means according to the content inside the element.

#### Block
The elements that default to block include:

* divs
* sections
* unordered lists
* paragraphs
* headers

Block elements are also like cats in that they take up as much space(width) as they want.

#### None
This removes the element from the page.

#### Flex
This is my favorite one. It allows you to more efficiently lay things out on your page. A container set to flex expands or shrinks the items to fill it. Flex unlocks a lot of properties and values you can use to get the items and space distributed in a container.

### POSITION

Let's talk about positioning.
There are five position properties:
static
relative
absolute
fixed
inherit

Once you declare one of these you can also use the properties of left, right, top, and bottom to move things around. The default of these directional properties is auto.

#### Static
The default state of all HTML elements.

#### Relative
If you declare relative positioning on an element and begin using directional properties, it will position itself relative to where it would have been.

#### Absolute
If you declare absolute positioning on an element with a parent that also has positioning declared, it will position itself relative to that parent. Doesn't that make a whole lot of sense??????

#### Fixed
A fixed position element will not respect its parents. It will positioned relative to the window. It will stay in the same spot in the window regardless of scrolling.

#### Inherit
If you declare inherit as the value, it will take on the positioning value from its parent.

### LASTLY...THE BOX MODEL PROPERTIES

It's important to understand the box model.

A quick summary is that every element has content, padding, border, and margin. You can also position elements by sizing these properties.
