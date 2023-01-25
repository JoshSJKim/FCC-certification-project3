# FCC-certification-project3

Technical Documentation Page

- This is the 3rd certification project for FCC.
- It consists of a nav bar that changes position to a sidebar when the screen width gets smaller.
- Will be a good practice to use the @media query.

## Adding syntax edits to code tag for easier readability

- Used br tag for each code break required for easier readability on the web page.
- There has to be a better way to apply this.
- Will need further styling using CSS later to add indentation where required.

- Issue resolved. Use pre tags instead of code tags for longer code examples to retain its form.
- Although code tags can be used for short code snippets, it seems to be more advantageous to use pre tags for all code examples for the sake of uniformity. Especially when there are numerous code snippets in the html. It would also be easier to group the codes into a single class for styling in CSS later.

## Box-sizing

- When using box-sizing: border-box, remove padding from * to utilize the entire web page.

### To do

- Add @media query to change the position of the navbar for smaller screen size.

### New problems encountered

- The page looks fine when it is full. However, when the screen size decreases, the main-doc element is overlapped with the nav bar.
- I also have to figure out how to get the navbar to scroll when using smaller height windows.

## RESET CSS

- The CSS file was getting too bloated and I lost track of which line applies which effect, and which lines are not doing anything.
- Wipe it clean and start over.
- Styling the side nav bar and encountered an issue with scrolling.
- The ul content is visible underneath the header content.

## To do: update

- Figure out a way to make the nav header fixed and ul content scroll beneath the header.
- Then apply @media to reposition the nav bar according to screen size.

### navbar issue

- Able to scroll the side navbar, but the nav-ul content does not scroll under the nav-header.
- Fiddling with position property but unable to achieve desired effect.
- Do some more googling.

### navbar issue (sort of) resolved

```CSS
  .navbar {
    position: fixed;
    top: 0;
    left: 0;
    width: 300px;
    height: 100%;
    border-right: 2px solid black;
    overflow: auto;
  }
```

- Position:fixed with top 0 and left 0 will position the navbar to the left side of the page.
- width: 300px and height: 100% will set the navbar to come out 300px from the left side of the page and fill the height of the entire page.
- border-right property will add a solid border on the right side of the navbar to provide separation from the main-doc element.
- overflow: auto will allow the navbar to scroll up and down if the contents of the nav-ul exceed the height of the page.

```CSS
    .nav-header {
    position: fixed;
    top: 0;
    left: 0;
    text-align: center;
    padding: 20px 0 20px 0;
    font-size: 1.7rem;
    background-color: white;
    width: 300px;
    height: 50px;
  }
```

- position: fixed, top:0, left:0 will fix the nav-header to the top left position of the page.
- text-align: center will center the text.
- padding: 20px 0 20px 0 will add padding to the top and bottom of the text.
- font-size is self explanatory.
- Added background-color: white so that the nav-ul content is not visible beneath the nav-header when scrolling. This felt like 'cheating' in a way. Need to explore more ways to achieve this effect.
- width: 300px and height: 50px will set the width and height of the header (including the extent of the background-color).

```CSS
  .nav-ul {
    list-style-type: none;
    padding: 0;
    margin-top: 90px;
    overflow-y: auto;
    overflow-x: hidden;
    border-top: 1px solid black;
  }
```

- list-style-type: none will remove the bullets from the list items.
- padding: 0 will remove any default padding from the element.
- margin-top: 90px will provide a buffer from the top of the page to the top of the nav-ul to off set the start point of the nav-ul content.
- The overflow-y is set to auto, which means that if the contents of the element exceed the height of the element, a scrollbar will appear vertically. overflow-x is set to hidden, which means that the horizontal scrollbar will be hidden if the contents of the element exceed the width of the element.
- border-top is self-explanatory.

```CSS
  .nav-ul li {
    border-bottom: 1px solid black;
    text-indent: 20px;
    padding: 10px 0 10px 0;
  }
```

- border-bottom is self-explanatory.
- text-indent: 20px will indent the list item text 20px from the left edge of the page.
- padding: 15px 0 15px 0 will provide 10px padding on top and bottom of the list item text.

## navbar issue again at top of page

- I want to have the nav-header scroll up when the main-doc is scrolled, but the nav-header stays fixed while the nav-ul content scrolls up with the main-doc content.
