# Overview #

A jQuery-based widget that turns a regular multiple option select box into a side-by-side pick list, as shown here:

![https://jquery-ui-picklist.googlecode.com/svn/trunk/examples/images/screenshot.png](https://jquery-ui-picklist.googlecode.com/svn/trunk/examples/images/screenshot.png)

The widget uses the original select box to store its state, so regular HTTP form submissions will continue working as normal.

**[Click here for live demos.](Demos.md)**

# Features #
  * Fully customizable button & list labels and CSS class names
  * Support for [items with rich HTML content](AddingItems#Adding_Rich_Content_Items.md)
  * [Several event hooks](CallbackEvents.md) available for customization and integration
  * CTRL + click selects multiple items
  * SHIFT + click selects a range of items
  * Double-clicking moves items
  * Compatible with ordinary form submission
  * Works in all major browsers (IE, FF, Chrome, Opera, and Safari)
  * Works with very large lists
  * Many options for [customization](Options.md)
  * **No longer requires jQuery UI!**

# Usage #

## JavaScript ##
```
$(function()
{
    $("#foobar").pickList();
});
```

## HTML ##
```
<select id="foobar" name="foobar" multiple="multiple">
    <option value="1">Option 1</option>
    <option value="2" selected="selected">Option 2</option>
    <option value="3">Option 3</option>
    <option value="4" selected="selected">Option 4</option>
    <option value="5">Option 5</option>
</select>
```