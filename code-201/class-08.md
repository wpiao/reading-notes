# Read: 08 - More CSS Layout - 2/2/2021 

## CSS Layout 

### Float
- `float` - take an element in normal flow and place it as far to the left or right of the containing element as possible
- `clear` - no element (within the same containing element) should touch the left or right-hand sides of a box
- Multi-column layouts - use `width`, `float`, `margin`

### Fixed width layouts 

  - Advantages  
    1. Pixel values are accurate at controlling the size and positioning of elements.
    2. The designer has far greater control over the appearance and position of items on the page than with liquid layouts.
    3. You can control the lengths of lines of text regardless of the size of the user's window.
    4. The size of an image will always remain the same relative to the rest of the page.
  - Disadvantages 
    1. You can end up with big gaps around the edge of a page.
    2. If the user's screen is a much higher resolution than the designer's screen, the page can look smaller and text can be harder to read.
    3. The design works best on devices that have a size or resolution similar to that of desktop or laptop computers.
    4. The page will often take up more vertical space than a liquid layout with the same content.

### Liquid layouts  

  - Advantages 
    1. Pages expand to fill the entire browser window so there are no spaces around the page on a large screen.
    2. If the user has a small window, the page can contract to fit it without the user having to scroll to the side.
    3. The design is tolerant of users setting font sizes larger than the designer intended (because the page can stretch).
  - Disadvantages 
    1. If you do not control the width of sections of the page then the design can look very different than you intended, with unexpected gaps around certain elements or items squashed together.
    2. If the user has a wide window, lines of text can become very long, which makes them harder to read.
    3. If the user has a very narrow window, words may be squashed and you can end up with few words on each line.
    4. If a fixed width item (such as an image) is in a box that is too small to hold it (because the user has made the window smaller) the image can overflow over the text.