# Shortcodes

 Type these into the main content editor for any page, post or portfolio item on the Super natural site.

## Button - [button]

Displays a button in the theme's style

#### Parameters

* `link` Where the button goes when its clicked. Default: the homepage
* `link_text` The text within the button. Default: "Visit"
* `target` Open link in the same window (\_self), or a new window (\_blank). Default: "\_blank"
* `center` Center this button within the parent element? Default: false

#### Example

    [button link="http://www.vinemasher.com" link_text="Visit Vinemasher" target="_self" center="true"]


## Ghost Button - [ghost-button]

Displays a button in the theme's style, but as a ghost button, so it has a transparent background and a supernatural-pink keyline.

#### Parameters

_Same as [button]_

#### Example

    [ghost-button link="http://www.vinemasher.com" link_text="Visit Vinemasher" target="_self" center="true"]


## Launch Work Button - [launch-work-button]

Displays a button in the theme's style, which when clicked opens a fancybox containing the work in an iframe. For use on portfolio pages mainly, but can be used in blog posts if relevant.

#### Parameters

* `link` The link to the parent page within the webMedia folder on the server. This is the URL that will be loaded into the iframe when the fancybox is launched. Default: none
* `link_text` The text within the button. Default: "View work"
* `center` Center this button within the parent element? Default: false
* `is_flash` Set to true if the work is flash and the button will be hidden if the user doesn't have flash. Default: false

#### Example

    [launch-work-button link="http://www.wearesupernatural.com/webMedia_v2/channel4/utopia2/utopia2Parent.html" link_text="Open the work" center="true" is_flash="true"]


## Vimeo player - [vimeo]

Displays a vimeo player in an iframe. Hint: to get the ID, go to the video you want on vimeo.com and look at the end of url

#### Parameters

* `id` Id of the vimeo video to insert. Default: none
* `width` Width of the video (enter units too, e.g. 500px, 80%, etc). Default: 100%
* `height` Height of the video. Default: 100%

#### Example

    [vimeo id="109836047" width="480px" height="270px"]


## Share links - [share-links]

Displays social sharing icons for twitter and facebook, which launch share windows when clicked, so users can share our pages more easily

#### Parameters

* `share_text` The default text that is pre-filled in the share box. Only appears for twitter, as FB doesn't support this anymore. Default: none
* `alignment` Align left or right of the parent element. Default: "left"
* `hide_twitter` Set to true to hide the twitter icon. Default: false
* `hide_facebook` Set to true to hide the facebook icon. Default: false

#### Example

    [share-links alignment="right" share_text="Check out this great post yaya!" hide_facebook="true"]


## Flash support wrapper - [if-has-flash]

Wrap content in this shortcode to get it to only show if the users browser has flash installed. Useful for writing alternate copy or something like that.

#### Parameters

_None_

#### Example

    [if-has-flash]
      This content and anything before the end tag will only show if the user has flash installed
    [end-if-has-flash]


## Columns

There are a few shortcodes for creating column based layouts. Treat them like divs - so any row or column that is opened needs to be closed at some point. These shortcodes don't take any parameters.

* `row` Start a row. Any columns need to be within a row
* `end-row` End a row.
* `half-column` Start a column that takes up half the container width
* `end-half-column` End the half column
* `third-column` Start a column that takes up a third of the container
* `end-third-column` End the third column

#### Example

With 2 columns:

    [row]
      [half-column]
        Content in the left half!
      [end-half-column]
      [half-column]
        content in the right half!
      [end-half-column]
    [end-row]

With 3 columns:

    [row]
      [third-column]
        Content in the left column!
      [end-third-column]
      [third-column]
        Content in the middle column!
      [end-third-column]
      [third-column]
        Content in the last column!
      [end-third-column]
    [end-row]
