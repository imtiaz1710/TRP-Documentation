# Filter-Documentation
Trp Filter Panel in Web:

![](https://github.com/imtiaz1710/TRP-Documentation/blob/main/filter%20web.jpg)

Flow of Component:

![](https://github.com/imtiaz1710/TRP-Documentation/blob/main/filterDiagram.png)


**filter-panel**: Here, option for filter dropdown and other information is loaded from endecapodService. From filter panel we pass the options in filter component.

**filter**: Here, single select component is invoked. When we open single select dropdown,'show' event and getValues() method is called. in getValues() method we check whether this.options.exposed (which is lazy loading) is false or not. If false we load the option here.

**single-select-filter**: In single select filter component we use p-dropdown component of primeNg. Which has two event onShow and onHide.If we select an element from dropdown onHide event fire and selected data emit. in the filter component it emits again and in the filter-panel component it saves the value by endecapodService.

