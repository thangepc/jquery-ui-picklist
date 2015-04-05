# Introduction #

Items can be added to the widget programmatically by supplying one or more "item object"s. An item object is a JavaScript literal object that describes an item to be added.


## Item Object ##

An example item object:

```
{
   value:    1,
   label:    "Foobar",
   selected: true
}
```

Here is a description of each property:

  * `value` is the value that is POSTed when the form is submitted, if the item has been added to the "target" list. Corresponds to the `value` attribute of a select box `<option>` element.

  * `label` is the value of the item in the list; also used for sorting. Corresponds to the body of a select box `<option>` element.

  * `selected` tells the widget where to insert the item. A `true` value inserts the item into the "target" list; a `false` value inserts the item into the "source" list. Corresponds to the `selected` attribute of a select box `<option>` element.


## Adding Items During Initialization ##

Items can be passed in as an array of item objects thru the `items` option:

```
$("#example").pickList(
{
    items:
    [
        {
            value: 3,
            label: "Test",
            selected: true
        },

        { ... }, { ... }, { ... }    // Multiple objects
    ]
});
```

## Adding Items After Initialization ##

Items can also be added after the widget has been initialized by passing an item object to the `insert` function:

```
$("#example").pickList();

// Do some other stuff.

$("#example").pickList("insert",
{
    value: 3,
    label: "Test",
    selected: true
});
```

**[Here's an example](http://jsfiddle.net/awnry/6QB5f/)** of adding items.

## Adding Rich Content Items ##

Rich content items can be added to the widget just like regular items. To do so, you simply pass a "rich item object" where a regular item object would normally go.

An example rich item object:

```
{
   value:    1,
   label:    "Foobar",
   selected: true,
   element:  $("#foobar")
}
```

As you can see, a rich item object is essentially a regular item object with one extra property:

  * `element` is the actual DOM element to add as the list item. This can be an element that already exists in the DOM, or it can be built on-the-fly.

Rich item objects can be used wherever a regular item object can be used, so you can pass them in with the `items` array during initialization and the `insert` function after initialization, as shown above with regular item objects.

**[Here's an example](http://jsfiddle.net/awnry/XMdPE/)** of adding rich content items.