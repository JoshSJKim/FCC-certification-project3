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
