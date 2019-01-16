# Assignment 1 - Hello World: GitHub and d3 

**by Emmett McCann**

[**"Stack"**](https://emmettmccann.github.io/01-ghd3/) explores the names of everyone in this class, progressively generating a histogram of letters used in each student's first name. 

Upon loading, Stack selects a random name from the class and breaks it down into letters, then passing these to a histogram. Once these letters are in their correct places in the histogram, Stack selects a new name and repeats the process. Over time, this builds out a histogram of letters in the first names of everyone in the class.

While it is not interactive, there are a few easy ways to change how this visualization displays. First, the width of the window directly affects the size of the graph. I have found that a vertically oriented window works best. A window that is just under twice as tall as it is wide seems to have the best results. Second, the speed of the visualization is currently set to best show its animations. In order to speed this viz up so that you can get to a completed histogram faster, increase the speed variable in the source code. 1 or 2 are good for viewing the animations, anywhere between 10 and 15 is better for viewing the results.

View viz [here.](https://emmettmccann.github.io/01-ghd3/)


### Resources

The main resource for this project was the d3 API documentation. Additionally, Mike Bostock's [General Update Pattern, Parts I](http://bl.ocks.org/mbostock/3808218) and [How Selections Work](http://bost.ocks.org/mike/selection/) tutorials were immensly helpful. 



### Screenshots

![midAnimation](/midAnimation.png)

This is a screenshot of the full page, mid-placement animation.

![polygonAnimation](/polygonAnimation.png)

This is during the circle to rectangle transition that uses polygons to better show the circle filling out into a rectangle.

![aspect](/Aspect.png)
The best aspect ratio of a window for viewing the histogram. Page must be refreshed when the window sizing is changed.

## Technical and Design Achievements

I had no experience with HTML, CSS, JavaScript, or D3 coming into this class. A lot of my work went into learning the basics of each of these systems and how they work together. I also spend a ton of time learning DOM and how selections and data joins work in D3.

#### Technical

- Multiple animations that are chained together through delays and function calls.
- Circle to Rectangle fill animation
  - Using polygons and multiple, chained animations to create the illusion that each circle melts into its place in the histogram, filling the availiable square space for that data point. Best viewed with the speed variable around 0.5 and a wide window to increase the size of the circles.
- Processing all names into an array of objects that can then be further split down into names and letters for displaying. 
- Grouping and arrangement of rectangles, text, and 'g' objects for displaying the name and animating its breakdown.
- Letter by letter breakdown of name.
- Synchronized creation and deletion of objects in creating transitional effects between the 'staging' and 'chart' svg sections of the page.
- Data-structure of the chart and letter objects to create a dynamically-stacking histogram.

#### Design

- Overall animation to describe exactly what the chart represents without any labels. This form of visualization is (human) language independent. "Show, don't tell"
- Custom color pallete integrated into CSS and JS sections.
- Smooth animated transitions between each letter's life on screen.
- Animation curves to provide somewhat physical feeling movement in the chart.

