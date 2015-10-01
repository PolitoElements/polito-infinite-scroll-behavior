# polito-infinite-scroll-behavior
Fires notification when the scroll position is near the end of the page

Useful implementing infinite scroll functionality.

```
bower install polito-infinite-scroll-behavior
```
```html
<dom-module id="polito-long-page">
    <style>
       :host {
           height:3000px;
           display: block;
       }
    </style>
    <template>

        <h1>when you get to the end of this page, nearEndOfPage will be invoked and log some stuff to the console!</h1>

    </template>

</dom-module>

<script>
    Polymer({
        is: "polito-long-page",
        behaviors: [Polito.InfiniteScrollBehavior],
        nearEndOfPage: function(){
            console.log("You're dangerously near the end of this page. Maybe you should load more stuff.");
        }
    });
</script>

```
