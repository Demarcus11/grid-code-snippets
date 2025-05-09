1. When using full-width on a header and you need flex then you'll have to nest the flex inside of a div instead of putting flex directly on the header because it will overwrite the .full-width grid class:

    ```css
    <header class="full-width">
      <div class="flex"></div>
    </header>
    ```
2.  The reason we need to repeat the same class twice for .content-grid and .full-width is because when we have .full-width we need to line up the content inside with the .content-grid and the easiesr way to do that is recreating the grid.

3.  The reason we need grid-template-rows: auto 1fr is because when we have a header we want to be able to use justify-items: start to overwrite the default behavior of grid which is stretch. The header will only take up as much space as it needs and the rest of the content will take up the rest of the space.
