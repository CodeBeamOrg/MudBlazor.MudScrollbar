# MudBlazor.MudScrollbar
A MudBlazor extension package that styles the scrollbars throughout the application.

## Usage
Use the MudScrollbar as a component:

```
<MudScrollbar />
```

It doesn't matter where you use the component. You can place it start, end or whatever else. It overrides the native scrollbar.

## Selector
MudScrollbar communicates with `Selector` parameter. If you set it null or empty, it means all scrollbars will affect in the application (while the razor page is loaded,
so its better to place it in Layout page to use between pages).
<br /><br />
Selector both supports id and class selectors in CSS. So both usage is valid (be sure that id selector starts with "#" and class selector starts with "."):

```
<MudScrollbar Selector="#id1" />
<div id="id1" />
```

```
<MudScrollbar Selector=".id2" />
<div class="id2" />
```
As you see, MudScrollbar affects all scrollbars which container's id or class match the selector.
<br /><br />
With `Selector` property, multiple custom scrollbars in a single page is supported.

## Supported Browsers
The parameters works with webkit based browsers like Edge, Chrome, Opera and Safari.
<br /><br />
Firefox has different scrollbar mechanism, so the parameters doesn't work for firefox. MudScrollbar has `FirefoxStyle` parameter to adding styles manually.

## Example
This video shows some parameters that how to change scrollbar's width, color and thumb styles.


https://user-images.githubusercontent.com/78308169/193427540-d85b595d-defb-4312-885d-392179f91344.mp4

## How to set MudSelect and MudAutocomplete's scrollbar styles?
You need to add class to `ListClass` parameter. It should like this:

```
<MudScrollbar Selector=".id1" />
<MudSelect ListClass="id1" />
```
