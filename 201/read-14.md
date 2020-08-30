## Read 14: Psychological Safety, CSS Transforms, Transitions, and Animations

> **Psychological safety** — a group culture that the Harvard Business School professor Amy Edmondson defines as a ‘‘shared belief held by members of a team that the team is safe for interpersonal risk-taking.’’ Psychological safety is ‘‘a sense of confidence that the team will not embarrass, reject or punish someone for speaking up,’’ Edmondson wrote in a study published in 1999. ‘‘It describes a team climate characterized by interpersonal trust and mutual respect in which people are comfortable being themselves.’’

### CSS Transforms

> `transform` **Property**: General layout techniques with alternative ways to size, position, and change elements.<br>
The transform property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values.

+ Browser support for `transform` isn't always great.  Vendor prefixes are encouraged for the best support.
  + ```
    element {
      -webkit-transform: scale(1.5);
      -moz-transform: scale(1.5);
      -o-transform: scale(1.5);
      transform: scale(1.5);
    }
    ```
    + This includes multiple vendor prefixes.  The last un-prefixed `transform` will overwrite the others if the browser has full support.



[Back to the main page](../README.md) 