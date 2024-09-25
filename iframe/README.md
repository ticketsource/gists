[< back](../)

# iframe TicketShop examples

the iframe URL can be customised to alter the listing/display, the structure is as follows:

```
https://www.ticketsource.{domain}/ticketshop/{promoter_id}/{target}/{eventRef}
```

<table>
    <thead>
        <tr>
            <th>parameter</th>
            <th>description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>domain</td>
            <td>The TicketSource territory domain (<code>.co.uk</code>, <code>.eu</code> or <code>.us</code>)</td>
        </tr>
        <tr>
            <td>promoter_id</td>
            <td>The TicketSource promoter id for this ticket shop</td>
        </tr>
        <tr>
            <td>target</td>
            <td>
                The <code>a</code> target attribute set for all links/buttons:
                <table>
                    <thead>
                        <tr>
                            <th>value</th>
                            <th>description</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td><code>_self</code></td>
                            <td>Open links in the iframe itself <em>(default)</em></td>
                        </tr>
                        <tr>
                            <td><code>_blank</code></td>
                            <td>Open links in a new tab/window</td>
                        </tr>
                        <tr>
                            <td><code>_parent</code></td>
                            <td>Open links in the frame above our iframe</td>
                        </tr>
                        <tr>
                            <td><code>_top</code></td>
                            <td>Open links in the top frame (i.e. the current tab/window)</td>
                        </tr>
                    </tbody>
                </table>
            </td>
        </tr>
        <tr>
            <td>eventRef</td>
            <td>filter performances to only those with a matching event reference</td>
        </tr>
    </tbody>
</table>

## Default

```html
<div id="embedTS_E" style="width:100%;"></div>
<script type="text/javascript">
  (function() {
    var el = document.createElement("script");
    el.src = "https://www.ticketsource.co.uk/ticketshop/E";
    var s = document.getElementsByTagName("script")[0];
    s.parentNode.insertBefore(el, s);
  })();
</script>
```

## Target

Always open in a new tab:

```html
<div id="embedTS_E" style="width:100%;"></div>
<script type="text/javascript">
  (function() {
    var el = document.createElement("script");
    el.src = "https://www.ticketsource.co.uk/ticketshop/E/_blank";
    var s = document.getElementsByTagName("script")[0];
    s.parentNode.insertBefore(el, s);
  })();
</script>
```

## Filter to event

Only show events with the `sample` reference:

```html
<div id="embedTS_E" style="width:100%;"></div>
<script type="text/javascript">
  (function() {
    var el = document.createElement("script");
    el.src = "https://www.ticketsource.co.uk/ticketshop/E/_self/sample";
    var s = document.getElementsByTagName("script")[0];
    s.parentNode.insertBefore(el, s);
  })();
</script>
```

*Note:* when specifying a later parameter such as `eventRef` all previous parameters must also be given (e.g. `target` is set to it's default of `_self` in the sample above)
