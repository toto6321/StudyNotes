# CSS

## CSS Basic







## CSS Advanced

### CSS Flexbox

#### CSS Flexbox Layout Module

Before the Flexbox Layout module, there were four layout modes:

- **Block**, for sections in a webpage
- **Inline**, for text
- **Table**, for two-dimensional table data
- **Positioned**, for explicit position of an element

The Flexible Box Layout Module, makes it easier to design  flexible responsive layout structure without using float or positioning.



#### CSS Flexbox Properties

| Property                                                     | Description                                                  | Values                                                       |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| [display](https://www.w3schools.com/cssref/pr_class_display.asp) | Specifies the type of box used for an HTML element           | flex, inline-flex                                            |
| [flex-direction](https://www.w3schools.com/cssref/css3_pr_flex-direction.asp) | This establishes the main-axis, thus defining the direction flex items are placed in the flex container. <br>Flexbox is (aside from optional wrapping) a single-direction layout  concept. Think of flex items as primarily laying out either in  horizontal rows or vertical columns. | row, row-reverse, <br>column, column-reverse                 |
| [flex-wrap](https://www.w3schools.com/cssref/css3_pr_flex-wrap.asp) | By default, flex items will all try to fit onto one line. You can change that and allow the items to wrap as needed with this property. | nowrap, <br>wrap, <br>wrap-reverse                           |
| [flex-flow](https://www.w3schools.com/cssref/css3_pr_flex-flow.asp) | A shorthand property for flex-direction and flex-wrap        |                                                              |
| [justify-content](https://www.w3schools.com/cssref/css3_pr_justify-content.asp) | This defines the alignment along the **main axis**.          | flex-start, start, left<br>flex-end, end, right, <br>center, <br>space-between, space-around, space-evenly |
| [align-items](https://www.w3schools.com/cssref/css3_pr_align-items.asp) | This defines the default behavior for how flex items are laid out along the **cross axis** on the current line. Think of it as the `justify-content` version for the cross-axis (perpendicular to the main-axis). | stretch, <br>flex-start, start, <br>flex-end, end, <br>center, <br>baselin |
| [align-content](https://www.w3schools.com/cssref/css3_pr_align-content.asp) | This aligns a flex container’s lines within when there is extra space in the cross-axis, similar to how `justify-content` aligns individual items within the main-axis. <br>This property has no effect when there is only one line of flex items. | stretch, <br/>flex-start, start, <br/>flex-end, end, <br/>center, <br/>space-between, <br>space-around, <br>space-evenly |
|                                                              |                                                              |                                                              |
|                                                              |                                                              |                                                              |
| [order](https://www.w3schools.com/cssref/css3_pr_order.asp)  | By default, flex items are laid out in the source order. However, the `order` property controls the order in which they appear in the flex container. | 0, 1, 2, 3, -1, -2 ...                                       |
| flex-grow                                                    | This defines the ability for a flex item to grow if necessary. It  accepts a unitless value that serves as a proportion. It dictates what  amount of the available space inside the flex container the item should  take up. | 0, 1, 2 ...                                                  |
| flex-shrink                                                  | This defines the ability for a flex item to shrink if necessary. |                                                              |
| flex-basis                                                   | This defines the default size of an element before the remaining space  is distributed. It can be a length (e.g. 20%, 5rem, etc.) or a keyword.  The `auto` keyword means “look at my width or height property” (which was temporarily done by the `main-size` keyword until deprecated). | auto, content                                                |
| [align-self](https://www.w3schools.com/cssref/css3_pr_align-self.asp) | This allows the default alignment (or the one specified by `align-items`) to be overridden for individual flex items. | auto \| flex-start \| flex-end \| center \| baseline \| stretch |
| [flex](https://www.w3schools.com/cssref/css3_pr_flex.asp)    | A shorthand property for the flex-grow, flex-shrink, and the flex-basis     properties |                                                              |



#### Flexbox illustration

##### flex-direction

![](https://css-tricks.com/wp-content/uploads/2018/10/flex-direction.svg)

##### flex-wrap

![](https://css-tricks.com/wp-content/uploads/2018/10/flex-wrap.svg)

##### flex-flow

flex-flow = flex-direction + flex-wrap

```css
.container {
    flex-flow: column, wrap;
}
```



##### justify-content

![](https://css-tricks.com/wp-content/uploads/2018/10/justify-content.svg)





##### align-items

![](https://css-tricks.com/wp-content/uploads/2018/10/align-items.svg)



##### align-content

![](https://css-tricks.com/wp-content/uploads/2018/10/align-content.svg)

##### ggalign-self

![](https://css-tricks.com/wp-content/uploads/2018/10/align-self.svg)