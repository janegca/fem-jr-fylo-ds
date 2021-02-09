# Frontend Mentor Jr Challenge - Fylo Data Storage Component

[Challenge Files](https://www.frontendmentor.io/challenges/fylo-data-storage-component-1dZPRbV5n)

## Criteria

Your users should be able to:

- View the optimal layout for the site depending on their device's screen size

## Visual Components

| Class         | Description            | Tag     | Element(s)                 |
| ------------- | ---------------------- | ------- | -------------------------- |
| wrapper       | generic                | div     | .fds .attribution          |
| fds           | namespace              | main    | .fds-Header .fds-Indicator |
| fds-Header    | page header            | header  | img .icons                 |
| fds-Indicator | data storage indicator | article | ??                         |

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

References:
