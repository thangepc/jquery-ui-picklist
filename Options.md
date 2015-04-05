# Options #

Although the widget works great right out of the box, there are several things about it that you can customize by passing in an object where each option you want to set is a property, such as this:

```
$("#foobar").pickList(
{
    mainClass:       "foobar",
    sourceListLabel: "Not Added",
    targetListLabel: "Added",
    addAllLabel:     "Add All",
    addLabel:        "Add",
    removeAllLabel:  "Remove All",
    removeLabel:     "Remove",
    sortItems:       false
});
```


## Container Classes ##

The "source" list, the "target" list, and the control buttons are placed in container `<div>` elements. The CSS class names for these elements can be customized:

|<b>Name</b>|<b>Description</b>|<b>Type</b>|<b>Default Value</b>|
|:----------|:-----------------|:----------|:-------------------|
|`mainClass`|The widget's main `<div>` that surrounds all the child elements|string|`pickList`|
|`listContainerClass`|List container `<div>`. It applies to both the source list container `<div>` as well as the target list container `<div>`|string|`pickList_listContainer`|
|`sourceListContainerClass`|The source list container `<div>`|string|`pickList_sourceListContainer`|
|`targetListContainerClass`|The target list container `<div>`|string|`pickList_targetListContainer`|
|`controlsContainerClass`|The button controls container `<div>`|string|`pickList_controlsContainer`|
|`clearClass`|Used on `<div>`s that need to clear any CSS floats|string|`pickList_clear`|


### List Classes ###

The "source" and "target" lists are HTML `<ul>` elements with each list item being a `<li>` element. The CSS class names for these can be customized:

|<b>Name</b>|<b>Description</b>|<b>Type</b>|<b>Default Value</b>|
|:----------|:-----------------|:----------|:-------------------|
|`listClass`|List `<ul>` element. It applies to both the source list and target list `<ul>` elements|string|`pickList_list`|
|`sourceListClass`|Source list `<ul>` element|string|`pickList_sourceList`|
|`targetListClass`|Target list `<ul>` element|string|`pickList_targetList`|
|`listItemClass`|List item `<li>` element|string|`pickList_listItem`|
|`richListItemClass`|List item that contains rich content|string|`pickList_richListItem`|
|`selectedListItemClass`|List item that has been selected by the user|string|`pickList_selectedListItem`|
|`listLabelClass`|List label `<div>`. It applies to the label `<div>` elements for both the source list and the target list|string|`pickList_listLabel`|
|`sourceListLabelClass`|Label `<div>` for the source list|string|`pickList_sourceListLabel`|
|`targetListLabelClass`|Label `<div>` for the target list|string|`pickList_targetListLabel`|


### Control Classes ###

The button controls that allow the user to move a selected item between the source and target lists are regular HTML `<button>` elements. The CSS class names for each of these can be customized:

|<b>Name</b>|<b>Description</b>|<b>Type</b>|<b>Default Value</b>|
|:----------|:-----------------|:----------|:-------------------|
|`addAllClass`|"Add All" button that moves all items in the source list over to the target list|string|`pickList_addAll`|
|`addClass`|"Add" button that moves all selected items in the source list over to the target list|string|`pickList_add`|
|`removeAllClass`|"Remove All" button that moves all items in the target list over to the source list|string|`pickList_removeAll`|
|`removeClass`|"Remove" button that moves all selected items in the target list over to the source list|string|`pickList_remove`|


### List & Button Labels ###

The labels used on the lists and the control buttons can be customized:

|<b>Name</b>|<b>Description</b>|<b>Type</b>|<b>Default Value</b>|
|:----------|:-----------------|:----------|:-------------------|
|`sourceListLabel`|HTML used as the label for the source list (images **are** allowed)|string|`Available`|
|`targetListLabel`|HTML used as the label for the target list (images **are** allowed)|string|`Selected`|
|`addAllLabel`|HTML used as the label for the "Add All" button (images **are** allowed)|string|`&gt;&gt;`|
|`addLabel`|HTML used as the label for the "Add" button (images **are** allowed)|string|`&gt;`|
|`removeAllLabel`|HTML used as the label for the "Remove All" button (images **are** allowed)|string|`&lt;&lt;`|
|`removeLabel`|HTML used as the label for the "Remove" button (images **are** allowed)|string|`&lt;`|


### Behavior ###

As items get moved between the source and target lists, the items may or may not get out of order. Whether or not to handle this can be customized:

|<b>Name</b>|<b>Description</b>|<b>Type</b>|<b>Default Value</b>|
|:----------|:-----------------|:----------|:-------------------|
|`sortItems`|Whether or not to re-sort the lists when items are added or removed|boolean|`true`|
|`sortAttribute`|The element attribute name on which to sort list items (if `sortItems` is `true`)|string|`label`|


### Adding List Items ###

Items can be added programmatically after initialization, or they can be passed in during initialization as options:

|<b>Name</b>|<b>Description</b>|<b>Type</b>|<b>Default Value</b>|
|:----------|:-----------------|:----------|:-------------------|
|`items`|Array of regular [item objects](AddingItems#Item_Object.md) and/or [rich item objects](AddingItems#Adding_Rich_Content_Items.md) to be added as list items|array|(empty array)|

Click **[here](AddingItems.md)** for full documentation on programmatically adding items to the widget.