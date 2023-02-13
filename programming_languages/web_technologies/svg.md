# SVG Cheat Sheet

Scalable Vector Graphics (SVG) is an XML-based vector image format for two-dimensional graphics with support for interactivity and animation. Here are some basic concepts and elements of SVG.

## SVG Elements

- `<svg>`: Defines the root of the SVG document, which contains the graphic content.

- `<rect>`: Draws a rectangle.

- `<circle>`: Draws a circle.

- `<ellipse>`: Draws an ellipse.

- `<line>`: Draws a line.

- `<polyline>`: Draws a series of connected lines.

- `<polygon>`: Draws a series of connected lines and closes the shape by connecting the last point to the first.

- `<path>`: Draws a path using a series of commands, such as lines, arcs, and curves.

## Coordinate System

SVG uses a coordinate system where (0, 0) is the top-left corner and the positive x-axis goes to the right, while the positive y-axis goes down. By default, the unit of measurement is the pixel.

## Colors and Styling

SVG supports various color models, including RGB, HSL, and CMYK. Colors can be defined in CSS, inline styles, or presentation attributes.

## Animation and Interactivity

SVG supports animation and interactivity through scripting (JavaScript) and declarative animation (SMIL).

## Example

Here is a simple example of an SVG that draws a red circle with a diameter of 50 pixels:

```xml
<svg width="100" height="100">
  <circle cx="50" cy="50" r="25" fill="red"/>
</svg>
```

## Conclusion

This cheat sheet provided an overview of the basic concepts and elements of Scalable Vector Graphics (SVG). To learn more, it is recommended to visit the [W3C SVG specification](https://www.w3.org/TR/SVG11/) and the [MDN web docs.](https://developer.mozilla.org/en-US/docs/Web/SVG)
