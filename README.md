[![Published on NPM](https://img.shields.io/npm/v/@zibuthe7j11/distinctio-maiores-eaque.svg)](https://www.npmjs.com/package/@zibuthe7j11/distinctio-maiores-eaque)

# &lt;@zibuthe7j11/distinctio-maiores-eaque&gt;

Drag and drop for lists as a web component.

## Demo

See [Demo](https://blog.jonas.liljegren.org/@zibuthe7j11/distinctio-maiores-eaque/).

## Features

* Natural movement of items using kinetic momentum

* Performant (using requestAnimationFrame and css translate)

* No dependencies

* Clean and powerful api

* Vertical lists

* Horizontal lists

* Movement between lists

* Supports both mouse and touch interfaces

* Unopinionated styling

* No creation of additional wrapper dom nodes

* Accepts any html elements as draggable

* Allows text selection around and inside items

* Handles elements of different sizes

* Supports drop of element anywhere on page, finding the closest availible drop area

* Handles changing visibility of drop zones

* Optional drag handles

* (almost) supports multiple and nested sortable containers

* Configurable drop zones per container.

* Dispatches events and uses css classes for changing states

* Respects the disabled attribute

* Handles changes in element and page layout during dragging and animations


## Usage

### Installation

```
npm install --save @zibuthe7j11/distinctio-maiores-eaque
```

### In an html file
```html
<script type="module" src="./@zibuthe7j11/distinctio-maiores-eaque.js"></script>
<@zibuthe7j11/distinctio-maiores-eaque><div>A</div><div>B</div></@zibuthe7j11/distinctio-maiores-eaque>
```

Supported attributes are:
* row: elements are displayes horizontal (default)
* column: elements are displayed vertical
* lock: Only move in selected axis
* group: Allow movement to other containers in the same group
* autosave: move element in DOM after drop
* disabled: make container inactive

Events you can listen to on the `@zibuthe7j11/distinctio-maiores-eaque` container:
* drop: details `{element, item}`
* dropoutside: details `{element, item}`

Methods availible on the `@zibuthe7j11/distinctio-maiores-eaque` container:
* reset(): move all items back to their original DOM positions
* commit(): update DOM placing items in their new place
* elements(): lists elements in the container, similar to what you would get from the DOM after a commit()
* elements_removed(): list elements moved to another contianer
* elements_added(): lists elements moved here from another container

The property `is_altered` tells you if anything has changed, like sort order or anything added or removed.

You can also add a `mv-draghandle` in an element for using that for dragging, instead of the whole element.


## Missing features

* Keyboard and accessability support

* Scroll viewport when items are dragged to edge
