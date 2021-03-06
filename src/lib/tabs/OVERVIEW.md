The Angular Material tab group helps organize content into separate views where only one view can be
visible at a time. Each tab's label is shown in the tab header and the active
tab's label is designated with the animated ink bar. When the list of tab labels exceeds the width
of the header, pagination controls appear to let the user scroll left and right across the labels.

The active tab may be set using the `selectedIndex` input or when the user selects one of the
tab labels in the header.

<!-- example(tab-overview) -->

### Events

The `selectChange` output event is emitted when the active tab changes.  

The `focusChange` output event is emitted when the user puts focus on any of the tab labels in
the header, usually through keyboard navigation. 

### Labels

If a tab's label is only text then the simple tab-group API can be used.

```html
<md-tab-group>
  <md-tab label="One">
    <h1>Some tab content</h1>
    <p>...</p>
  </md-tab>
  <md-tab label="Two">
    <h1>Some more tab content</h1>
    <p>...</p>
  </md-tab>
</md-tab-group>
```

For more complex labels, add a template with the `md-tab-label` directive inside the `md-tab`.

```html
<md-tab-group>
  <md-tab>
    <template md-tab-label>
      The <em>best</em> pasta
    </template>
    <h1>Best pasta restaurants</h1>
    <p>...</p>
  </md-tab>
  <md-tab>
    <template md-tab-label>
      <md-icon>thumb_down</md-icon> The worst sushi
    </template>
    <h1>Terrible sushi restaurants</h1>
    <p>...</p>
  </md-tab>
</md-tab-group>
```

### Dynamic Height

By default, the tab group will not change its height to the height of the currently active tab. To
change this, set the `dynamicHeight` input to true. The tab body will animate its height according
 to the height of the active tab.