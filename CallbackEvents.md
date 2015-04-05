# Introduction #

Several callback events were added to the widget to facilitate extending or altering the functionality without having to directly modify the widget's source code. This page documents what events are exposed and how to use them.

[Here is a demo](http://jsfiddle.net/awnry/MJunV/) of hooking into callback events.


# Events #

Click on an event name to view more information.

|<b>Name</b>|<b>Type</b>|<b>Gets Triggered...</b>|
|:----------|:----------|:-----------------------|
|[beforeBuild](#beforeBuild.md)|pickListbeforeBuild|Just before the picklist is initially built|
|[afterBuild](#afterBuild.md)|pickListafterBuild|Just after the picklist is initially built|
|[beforePopulate](#beforePopulate.md)|pickListbeforePopulate|Just before the "source" and "target" lists are initially populated|
|[afterPopulate](#afterPopulate.md)|pickListafterPopulate|Just after the "source" and "target" lists are initially populated|
|[beforeAddAll](#beforeAddAll.md)|pickListbeforeAddAll|Before any items have been moved (when the "Add All" button gets invoked)|
|[afterAddAll](#afterAddAll.md)|pickListafterAddAll|After the items have been moved (when the "Add All" button gets invoked)|
|[beforeAdd](#beforeAdd.md)|pickListbeforeAdd|Before any items have been moved (when the "Add" button gets invoked)|
|[afterAdd](#afterAdd.md)|pickListafterAdd|After the items have been moved (when the "Add" button gets invoked)|
|[beforeRemove](#beforeRemove.md)|pickListbeforeRemove|Before any items have been moved (when the "Remove" button gets invoked)|
|[afterRemove](#afterRemove.md)|pickListafterRemove|After the items have been moved (when the "Remove" button gets invoked)|
|[beforeRemoveAll](#beforeRemoveAll.md)|pickListbeforeRemoveAll|Before any items have been moved (when the "Remove All" button gets invoked)|
|[afterRemoveAll](#afterRemoveAll.md)|pickListafterRemoveAll|After the items have been moved (when the "Remove All" button gets invoked)|
|[onChange](#onChange.md)|pickListonChange|Whenever one or more items are added to, or removed from, the "target" list|
|[beforeRefresh](#beforeRefresh.md)|pickListbeforeRefresh|Just before the widget is refreshed|
|[afterRefresh](#afterRefresh.md)|pickListafterRefresh|Just after the widget is refreshed|
|[beforeRefreshControls](#beforeRefreshControls.md)|pickListbeforeRefreshControls|Just before the widget's control buttons are refreshed|
|[afterRefreshControls](#afterRefreshControls.md)|pickListafterRefreshControls|Just after the widget's control buttons are refreshed|
|[onDestroy](#onDestroy.md)|pickListonDestroy|When the widget is destroyed|


---


## beforeBuild ##

This event is triggered just before the picklist widget is initially built. This happens only once, when the widget is first initialized.

#### Code Example ####

Supply a callback function to handle the `beforeBuild` event as an init option.

```
$(".selector").pickList({
    beforeBuild: function() { ... }
});
```

Bind to the `beforeBuild` event by type: `picklistbeforebuild`

```
$(".selector").bind("picklistbeforebuild", function() {
    ...
});
```


---


## afterBuild ##

This event is triggered just after the picklist widget is initially built. This happens only once, when the widget is first initialized.

#### Code Example ####

Supply a callback function to handle the `afterBuild` event as an init option.

```
$(".selector").pickList({
    afterBuild: function() { ... }
});
```

Bind to the `afterBuild` event by type: `picklistafterbuild`

```
$(".selector").bind("picklistafterbuild", function() {
    ...
});
```


---


## beforePopulate ##

This event is triggered just before the "source" and "target" lists are initially populated with items. This happens only once, when the widget is first initialized.

#### Code Example ####

Supply a callback function to handle the `beforePopulate` event as an init option.

```
$(".selector").pickList({
    beforePopulate: function() { ... }
});
```

Bind to the `beforePopulate` event by type: `picklistbeforepopulate`

```
$(".selector").bind("picklistbeforepopulate", function() {
    ...
});
```


---


## afterPopulate ##

This event is triggered just after the "source" and "target" lists are initially populated with items. This happens only once, when the widget is first initialized.

#### Code Example ####

Supply a callback function to handle the `afterPopulate` event as an init option.

```
$(".selector").pickList({
    afterPopulate: function() { ... }
});
```

Bind to the `afterPopulate` event by type: `picklistafterpopulate`

```
$(".selector").bind("picklistafterpopulate", function() {
    ...
});
```


---


## beforeAddAll ##

This event is triggered whenever the "Add All" button is invoked, before any of the items are moved from the "source" list to the "target" list.

#### Code Example ####

Supply a callback function to handle the `beforeAddAll` event as an init option.

```
$(".selector").pickList({
    beforeAddAll: function() { ... }
});
```

Bind to the `beforeAddAll` event by type: `picklistbeforeaddall`

```
$(".selector").bind("picklistbeforeaddall", function() {
    ...
});
```


---


## afterAddAll ##

This event is triggered whenever the "Add All" button is invoked, after all of the items are moved from the "source" list to the "target" list.

#### Code Example ####

Supply a callback function to handle the `afterAddAll` event as an init option.

```
$(".selector").pickList({
    afterAddAll: function() { ... }
});
```

Bind to the `afterAddAll` event by type: `picklistafteraddall`

```
$(".selector").bind("picklistafteraddall", function() {
    ...
});
```


---


## beforeAdd ##

This event is triggered whenever the "Add" button is invoked, before any of the selected items are moved from the "source" list to the "target" list.

#### Code Example ####

Supply a callback function to handle the `beforeAdd` event as an init option.

```
$(".selector").pickList({
    beforeAdd: function() { ... }
});
```

Bind to the `beforeAdd` event by type: `picklistbeforeadd`

```
$(".selector").bind("picklistbeforeadd", function() {
    ...
});
```


---


## afterAdd ##

This event is triggered whenever the "Add" button is invoked, after all of the selected items are moved from the "source" list to the "target" list.

#### Code Example ####

Supply a callback function to handle the `afterAdd` event as an init option.

```
$(".selector").pickList({
    afterAdd: function() { ... }
});
```

Bind to the `afterAdd` event by type: `picklistafteradd`

```
$(".selector").bind("picklistafteradd", function() {
    ...
});
```


---


## beforeRemove ##

This event is triggered whenever the "Remove" button is invoked, before any of the selected items are moved from the "target" list to the "source" list.

#### Code Example ####

Supply a callback function to handle the `beforeRemove` event as an init option.

```
$(".selector").pickList({
    beforeRemove: function() { ... }
});
```

Bind to the `beforeRemove` event by type: `picklistbeforeremove`

```
$(".selector").bind("picklistbeforeremove", function() {
    ...
});
```


---


## afterRemove ##

This event is triggered whenever the "Remove" button is invoked, after all of the selected items are moved from the "target" list to the "source" list.

#### Code Example ####

Supply a callback function to handle the `afterRemove` event as an init option.

```
$(".selector").pickList({
    afterRemove: function() { ... }
});
```

Bind to the `afterRemove` event by type: `picklistafterremove`

```
$(".selector").bind("picklistafterremove", function() {
    ...
});
```


---


## beforeRemoveAll ##

This event is triggered whenever the "Remove All" button is invoked, before any of the items are moved from the "target" list to the "source" list.

#### Code Example ####

Supply a callback function to handle the `beforeRemoveAll` event as an init option.

```
$(".selector").pickList({
    beforeRemoveAll: function() { ... }
});
```

Bind to the `beforeRemoveAll` event by type: `picklistbeforeremoveall`

```
$(".selector").bind("picklistbeforeremoveall", function() {
    ...
});
```


---


## afterRemoveAll ##

This event is triggered whenever the "Remove All" button is invoked, after all of the items are moved from the "target" list to the "source" list.

#### Code Example ####

Supply a callback function to handle the `afterRemoveAll` event as an init option.

```
$(".selector").pickList({
    afterRemoveAll: function() { ... }
});
```

Bind to the `afterRemoveAll` event by type: `picklistafterremoveall`

```
$(".selector").bind("picklistafterremoveall", function() {
    ...
});
```


---


## onChange ##

This event is triggered whenever one or more items are added to, or removed from, the "target" list, i.e. when the pickList's selection changes. It's essentially the pickList equivalent of a `<select>` element's `onChange` event.

#### Code Example ####

Supply a callback function to handle the `onChange` event as an init option.

```
$(".selector").pickList({
    onChange: function() { ... }
});
```

Bind to the `onChange` event by type: `picklistonchange`

```
$(".selector").bind("picklistonchange", function() {
    ...
});
```


---


## beforeRefresh ##

This event is triggered just before the widget is refreshed.

#### Code Example ####

Supply a callback function to handle the `beforeRefresh` event as an init option.

```
$(".selector").pickList({
    beforeRefresh: function() { ... }
});
```

Bind to the `beforeRefresh` event by type: `picklistbeforerefresh`

```
$(".selector").bind("picklistbeforerefresh", function() {
    ...
});
```


---


## afterRefresh ##

This event is triggered just after the widget is refreshed.

#### Code Example ####

Supply a callback function to handle the `afterRefresh` event as an init option.

```
$(".selector").pickList({
    afterRefresh: function() { ... }
});
```

Bind to the `afterRefresh` event by type: `picklistafterrefresh`

```
$(".selector").bind("picklistafterrefresh", function() {
    ...
});
```


---


## beforeRefreshControls ##

This event is triggered just before the widget's control buttons are refreshed.

#### Code Example ####

Supply a callback function to handle the `beforeRefreshControls` event as an init option.

```
$(".selector").pickList({
    beforeRefreshControls: function() { ... }
});
```

Bind to the `beforeRefreshControls` event by type: `picklistbeforerefreshcontrols`

```
$(".selector").bind("picklistbeforerefreshcontrols", function() {
    ...
});
```


---


## afterRefreshControls ##

This event is triggered just after the widget's control buttons are refreshed.

#### Code Example ####

Supply a callback function to handle the `afterRefreshControls` event as an init option.

```
$(".selector").pickList({
    afterRefreshControls: function() { ... }
});
```

Bind to the `afterRefreshControls` event by type: `picklistafterrefreshcontrols`

```
$(".selector").bind("picklistafterrefreshcontrols", function() {
    ...
});
```


---


## onDestroy ##

This event is triggered when the widget gets destroyed.

#### Code Example ####

Supply a callback function to handle the `onDestroy` event as an init option.

```
$(".selector").pickList({
    onDestroy: function() { ... }
});
```

Bind to the `onDestroy` event by type: `picklistondestroy`

```
$(".selector").bind("picklistondestroy", function() {
    ...
});
```