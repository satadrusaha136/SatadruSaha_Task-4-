/*
===========================================================
1. UNIVERSAL SELECTOR
===========================================================
*/

* {
    /*
    The box-sizing property controls how the total width
    and height of an element are calculated.

    border-box means that the declared width and height
    include the content, padding, and border.

    This makes it easier to control the size of elements
    and prevents padding or borders from increasing the
    final dimensions unexpectedly.
    */
    box-sizing: border-box;
}


/*
===========================================================
2. IMAGE CONTAINER
===========================================================
*/

.image-container {

    /*
    display: grid;

    Converts the element into a CSS Grid container.

    CSS Grid is used to arrange child elements into rows
    and columns.
    */
    display: grid;


    /*
    grid-template-rows: minmax(0, 1fr) auto;

    Creates two rows:

    First row:
    minmax(0, 1fr)

    - The first row occupies the available remaining space.
    - 1fr means one fraction of the available space.
    - The minimum size is 0, allowing the row to shrink if
      necessary.

    Second row:
    auto

    - The second row takes the space required by its content.
    - In this example, the second row contains the button.

    Therefore:
    - The image occupies the first row.
    - The button occupies the second row.
    */
    grid-template-rows: minmax(0, 1fr) auto;


    /*
    width: 50vw;

    Sets the width of the container to 50% of the viewport width.

    vw means viewport width.

    Example:
    If the viewport width is 1200px:

    50vw = 600px
    */
    width: 50vw;


    /*
    height: 80vh;

    Sets the height of the container to 80% of the viewport height.

    vh means viewport height.

    Example:
    If the viewport height is 900px:

    80vh = 720px
    */
    height: 80vh;


    /*
    margin: 10vh 25vw;

    Adds space outside the container.

    Two values are used:

    First value:
    10vh

    - Sets the top and bottom margin to 10% of the viewport height.

    Second value:
    25vw

    - Sets the left and right margin to 25% of the viewport width.

    This places the container away from the edges of the page.
    */
    margin: 10vh 25vw;


    /*
    border: 4px solid black;

    Adds a 4-pixel solid black border around the container.

    This declaration is currently commented out, so it is
    not applied.

    Remove the comment marks to display the border.
    */

    /* border: 4px solid black; */
}


/*
===========================================================
3. IMAGE INSIDE THE IMAGE CONTAINER
===========================================================
*/

.image-container img {

    /*
    width: 100%;

    Makes the image occupy the full width of its parent
    element, which is .image-container.
    */
    width: 100%;


    /*
    height: 100%;

    Makes the image occupy the full height of the grid row
    in which it is placed.
    */
    height: 100%;


    /*
    object-fit: cover;

    Controls how the image fits inside its assigned width
    and height.

    cover means:

    - The image completely fills the available area.
    - The original aspect ratio is maintained.
    - Some parts of the image may be cropped if the
      image and container have different proportions.
    */
    object-fit: cover;


    /*
    display: block;

    Changes the image from its default inline behavior
    to block-level behavior.

    This prevents unwanted empty space that can sometimes
    appear below inline images.
    */
    display: block;
}


/*
===========================================================
4. BUTTON
===========================================================
*/

.bottom-button {

    /*
    width: 100%;

    Makes the button occupy the complete width of its
    parent grid container.
    */
    width: 100%;


    /*
    padding: 15px;

    Adds 15 pixels of internal space on all four sides
    of the button:

    - Top: 15px
    - Right: 15px
    - Bottom: 15px
    - Left: 15px

    Padding increases the space between the button text
    and the button's border.
    */
    padding: 15px;


    /*
    border: none;

    Removes the default border from the button.
    */
    border: none;


    /*
    background: linear-gradient(...);

    Applies a linear gradient as the background of the button.

    The gradient smoothly changes from one color to another.
    */
    background: linear-gradient(

        /*
        to right;

        Specifies that the gradient should move from
        left to right.
        */

        to right,


        /*
        #ffff00;

        Yellow color.

        This is the starting color of the gradient.
        */
        #ffff00,


        /*
        #9acd32;

        Yellow-green color.

        This is the ending color of the gradient.
        */
        #9acd32
    );


    /*
    color: white;

    Sets the text color of the button to white.
    */
    color: white;


    /*
    font-size: 18px;

    Sets the button text size to 18 pixels.
    */
    font-size: 18px;


    /*
    cursor: pointer;

    Changes the mouse cursor to a pointer when the user
    moves the cursor over the button.

    This indicates that the button is clickable.
    */
    cursor: pointer;
}

* 
→ Applies box-sizing: border-box to all elements.

.image-container
→ Creates a grid container with two rows.
→ The image occupies the remaining space.
→ The button occupies the space required by its content.
→ The container is 50vw wide and 80vh high.

.image-container img
→ Makes the image fill its grid area.
→ object-fit: cover maintains the image ratio while filling the area.

.bottom-button
→ Makes the button full-width.
→ Adds 15px padding.
→ Removes the border.
→ Applies a yellow-to-yellow-green gradient.
→ Makes the text white and the cursor a pointer.