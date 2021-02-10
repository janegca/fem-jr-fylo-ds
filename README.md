# Frontend Mentor Jr Challenge - Fylo Data Storage Component

[Challenge Files](https://www.frontendmentor.io/challenges/fylo-data-storage-component-1dZPRbV5n)

## Criteria

Your users should be able to:

- View the optimal layout for the site depending on their device's screen size

## Visual Components

| Class                 | Description            | Tag     | Element(s)                 |
| --------------------- | ---------------------- | ------- | -------------------------- |
| fds                   | namespace              | article | .fds-Header .fds-Indicator |
| fds-Header            | page header            | header  | img .icons                 |
| fds-Indicator         | data storage indicator | article | p[span] \_bar \_callout    |
| fds-Indicator_bar     | the progress bar       | div     | [div span .dot p em]       |
| fds-Indicator_callout | available storage      | p       | strong em                  |

## Colors

- Gradient: hsl(6, 100%, 80%) to hsl(335, 100%, 65%)

- Pale Blue: hsl(243, 100%, 93%)
- Grayish Blue: hsl(229, 7%, 55%)
- Dark Blue: hsl(228, 56%, 26%)
- Very Dark Blue: hsl(229, 57%, 11%)

## Typography

- Font size: 14px

- Family: [Raleway](https://fonts.google.com/specimen/Raleway)
- Weights: 400, 700

## Thoughts

### Progress Bar

Wasted a ton of time trying to use and style the HTML `progress` element but
could not get it to match the design. Thought about using the HTML `input` form
element which might, in the end be the way to go although you'd have to turn off
it's interactive features; would not want the user to be able to adjust it. In
the end, styled a `div` with nested `span` elements. Bit of a cheat, but it
works for now.

### Desktop Layout

Having real problems with this, think it's due to my width settings; back to the
drawing board. The .fds-Header does not respect the `max-width` setting,
probably because the content size never grows and so doesn't trigger it, so it's
taking up all the extra space when the page grows ☹️

- the `clamp` isn't being respected, why?
  - on`.fds` - it does not grow to its `max-width`, and its contents overflow
- `.fds-Header` `max-width` not respected, why?
  - removed the `min-width` setting and everything is ok in small size but
    component shrinks instead of growing in larger screen size; setting
    `max-width` in the media query has no effect
- opposite problem with `.fds-Indicator`, it doesn't grow at all for larger
  screens, remains fixed

✔️FIX:

- changed `main` layout from `grid` to `flex` - `.fds` now grows
- removed all size settings on `.fds`
- added `flex: 1` to `.fds-Header` and `flex: 2` to `.fds-Indicator`
- removed all width settings on `.fds-Header` and `.fds-Indicator` then set
  `min-height` and `min-width` on both for basic sizing, adding `max-width`
  values to their media queries
- adjusted `padding` on `.fds-Header`

### Afterthoughts

Caused most of the problems on this by getting ahead of myself and trying to be
too cute with layouts and `clamp` -- KISS is always best

References:

- [Min and Max Width/Height in CSS](https://www.ishadeed.com/article/min-max-css/)
