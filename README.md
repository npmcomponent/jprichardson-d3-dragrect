*This repository is a mirror of the [component](http://component.io) module [jprichardson/d3-dragrect](http://github.com/jprichardson/d3-dragrect). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/jprichardson-d3-dragrect`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
JavaScript - d3-dragrect
========================

A JavaScript D3 drag selection rectangle component. Only horizontal at the moment. 

This essentially allows you to use a graph that you created in D3 and then drag and visually select portions of the graph. You can create multiple selections.


Screenshots and examples coming when the API stabilizes a bit.


Install
-------


### Script

```html
<script src="/path/to/d3-dragrect.js"></script>
```


### Browserify

    npm install --save d3-dragrect


### Component

    component install jprichardson/d3-dragrect


Usage
-----

### Example


```javascript
//only use 'require' if using browserify or component
var d3dragrect = require('d3-dragrect') 

//'svg' is your svg element, typically 'height' would be the height of 'svg'
var dragBehavior = d3dragrect(d3, svg, xScale, height)

svg.call(dragBehavior)

```

### Methods

#### dragBehavior.createRect(x, y, width, height, [id])

#### dragBehavior.isPointInAnyRect(pt)

#### dragBehavior.getLastRectData()

#### dragBehavior.deleteAllSelected(callback)

#### dragBehavior.on('dragstart|drag|dragend', callback)


### Styling

The default styling will be very ugly. This makes it look alright:

```css
.d3-dragrect {
  stroke: steelblue;
  stroke-dasharray: 5,5;
  fill: aliceblue;
  fill-opacity: 0.5;
  hover: ;
}

.d3-dragrect:hover {
  stroke: red;
  fill-opacity: 0.7;
  stroke-dasharray: 1,1;
}

.d3-dragrect.selected {
  stroke: red;
  fill-opacity: 0.5;
}
```


License
-------

(MIT License)

Copyright 2013, JP Richardson  <jprichardson@gmail.com>


