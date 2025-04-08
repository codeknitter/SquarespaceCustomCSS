# SquarespaceCustomCSS
Custom CSS added to a Squarespace site to make it more accessible.

## Summary
When I updated my Squarespace site https://kathy-bateman.squarespace.com/ to a new template (Squarespace version 7.0-Bedford familiy, Hayden template) I noticed some issues with accessibility, specifically as it related to indicating interactive elements.

This is a copy of the custom CSS I added to increase the accessibility of my site.

## Goals
The key accessibility needs addressed with this custom css:
- Provide sufficient contrast between foreground and background
- Don’t use color alone to convey information
- Ensure that interactive elements are easy to identify

Some methods used to do this:
- add underlines to links
- add hovers and focus states that are not simple color changes alone
- increase color contrast

Misc other things fixed, but not specific to accessibility:
- some elements didn't reflect the font families I picked for the template and were defaulting to other ones
- added a header to the search page (since I couldn't change the structure itself I had to fake it with content in a `::before` that was styled like an `h1`)
- changed spacing and added border between blog entries on the list page

## Caveats

Unfortunately, the template has some other issues with accessibility that I can't address with a custom CSS overrides alone. 

For example, on the blog list page (https://www.kathybateman.com/blog) the titles of all the blog entries are `h1` but ideally there should only be one `h1` on the page. If able, I would restructure the html of the page to add one `h1` at the top with the blog name and the title of each blog entry would be an `h2`. 

The closest I could get was to change the visual appearance of the page by adding a fake `h1` at the top of the page by adding the text in a `::before` and then giving it the style of an `h1`. And then I styled the title of each blog entry to look like an `h2`. Of course, this only addresses this issue visually, and doesn't address the true underlying accessibility problem which would need to be a structural change. 

Note: I know there are still accessibility issues present on the site. For example I haven't had a chance to add alt text to all images I added years ago, before I knew how important alt text was.
