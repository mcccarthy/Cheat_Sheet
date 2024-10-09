
Here’s a **cheatsheet** for the **CSS Flexbox**:

### Flex Container Properties:

1. **display**:
    `flex` | `inline-flex`

    * Defines a flex container.
2. **flex-direction**:
    `row` | `row-reverse` | `column` | `column-reverse`

    * Sets the direction of the flex items.
3. **flex-wrap**:
    `nowrap` | `wrap` | `wrap-reverse`

    * Controls whether flex items wrap onto multiple lines.
4. **flex-flow**:
    `flex-direction` + `flex-wrap`

    * Shorthand for `flex-direction` and `flex-wrap`.
5. **justify-content**:
    `flex-start` | `flex-end` | `center` | `space-between` | `space-around` | `space-evenly`

    * Aligns flex items along the main axis.
6. **align-items**:
    `stretch` | `flex-start` | `flex-end` | `center` | `baseline`

    * Aligns flex items along the cross-axis.
7. **align-content**:
    `stretch` | `flex-start` | `flex-end` | `center` | `space-between` | `space-around`

    * Aligns rows of flex items when there's extra space on the cross-axis.

* * *

### Flex Item Properties:

1. **order**:
    `<number>`

    * Controls the order of flex items.
2. **flex-grow**:
    `<number>` (default: `0`)

    * Defines how much a flex item will grow relative to others.
3. **flex-shrink**:
    `<number>` (default: `1`)

    * Defines how much a flex item will shrink relative to others.
4. **flex-basis**:
    `<length>` | `auto`

    * Sets the initial size of a flex item before growing or shrinking.
5. **flex**:
    `flex-grow` | `flex-shrink` | `flex-basis`

    * Shorthand for `flex-grow`, `flex-shrink`, and `flex-basis`.
6. **align-self**:
    `auto` | `flex-start` | `flex-end` | `center` | `baseline` | `stretch`

    * Allows a flex item to override the `align-items` of the flex container.

* * *

### Flexbox Shortcuts:

1. **One-line flex container setup**:

    ```css
    display: flex; /* or inline-flex */
    flex-flow: row wrap;
    justify-content: space-between;
    align-items: center;
    ```

2. **Shorthand for flex items**:

    ```css
    flex: 1 0 100px; /* flex-grow: 1, flex-shrink: 0, flex-basis: 100px */
    ```

3. **Centering items in both axes**:

    ```css
    display: flex;
    justify-content: center;
    align-items: center;
    ```


This covers most of the important flexbox properties and useful shortcuts!