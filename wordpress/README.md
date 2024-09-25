[< back](../)

# WordPress TicketShop plugin shortcode examples

the shortcode used to inject our WordPress plugin TicketShop iframe into one of your WordPress pages can be customised to alter the listing/display, the structure is as follows:

```
[ticketshop id="E" target="_BLANK" eventref="SAMPLE"]
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
        <td><strong>id</strong><br><em>required</em></td>
        <td>The TicketSource promoter id for this ticket shop</td>
      </tr>
      <tr>
        <td><strong>target</strong><br><em>optional</em></td>
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
        <td><strong>eventref</strong><br><em>optional</em></td>
        <td>filter performances to only those with a matching event reference</td>
      </tr>
    </tbody>
</table>

## Default

```
[ticketshop id="E"]
```

## Target

Always open in a new tab:

```
[ticketshop id="E" target="_BLANK"]
```

## Filter to event

Only show events with the `SAMPLE` reference:

```
[ticketshop id="E" eventref="SAMPLE"]
```

## Combining parameters

You can use the `target` and `eventref` perameters in the same shortcode

```
[ticketshop id="E" target="_BLANK" eventref="SAMPLE"]
```

ordering does not matter, this example is equivalent to the one above:

```
[ticketshop eventref="SAMPLE" target="_BLANK" id="E"]
```
