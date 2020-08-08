# Svelte CUBE CSS Demo

This re-creates the [CUBE CSS dashboard tutorial](https://piccalil.li/tutorial/build-a-dashboard-with-cube-css/) using Svelte to explore how CUBE CSS could be used within a UI component-driven framework. I also made a few refactorings to make components more data-driven. These changes have resulted in a bit more JavaScript than strictly necessary, though Svelte does keep things very slim 😅 (12KB minified, 5KB compressed). The page could also be server-side rendered if desired.

Major changes:
- Global CSS and utilities live in the `/scss` folder and are output to a global stylesheet, allowing them to be used from any Svelte component. Block- and exception-level styling have been moved into individual components. Because of this, some of the nested styles have been flattened since Svelte components automatically scope styles. 
- A `_helpers.scss` file has been added to allow Svelte components to access shared Sass mixins and functions.
- The Summary component now takes props for balance, outgoings, and income.
- The transaction tables are generated from a list of transactions instead of being hard-coded. Date and amount are being formatted in the browser.
