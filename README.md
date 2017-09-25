# \<isw-snackbar\>

Material Design Polymer 2.0 Snackbar / Toast, stacking context safe with remote-control.

Place your snackbar somewhere save from stacking-context issues, and access it over a remote element in your view.

An open call to an allready opened snackbar closes and opens it again, multiple calls are queued.

Only one snackbar is needed, e.g. placed in the app.

```html
<isw-snackbar device="tablet"></isw-snackbar>
```

It can be accessed from multiple remotes. 

```html
<isw-snackbar-remote
    id="firstSnackbar"
    message="My First Snackbar"
    duration="5000">
</isw-snackbar-remote>
<isw-snackbar-remote
    id="secondSnackbar"
    message="My Second Snackbar"
    duration="2000">
</isw-snackbar-remote>
```

```javascript
openFirstSnackbar() {
  this.$.firstSnackbar.open();
}
openSecondSnackbar() {
  this.$.secondSnackbar.open();
}
```

The element uses the isw-responsive-behavior, so its appearance can be controlled by setting the device attribute...

```html
<isw-snackbar device="mobile"></isw-snackbar>
```

```html
<isw-snackbar device="tablet"></isw-snackbar>
```

... or get responsive by combining with <isw-responsive>

```html
<isw-responsive
    device="{{device}}">
</isw-responsive>

<isw-snackbar device="[[device]]"></isw-snackbar>
```