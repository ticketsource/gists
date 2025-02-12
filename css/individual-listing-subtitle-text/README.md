[< back](../)

To add custom text to a specific performance on your listings pages (e.g. to mark a BSL/British Sign Language performance) add the following to the Custom CSS box under Settings > Ticket Shop in your TicketSource account:

```css
.eventRow[data-id="1234567"] .eventTitle a span {
  display: flex;
  flex-direction: column;
}

.eventRow[data-id="1234567"] .eventTitle a span:after,
body[data-pid="1234567"] .heading .eventTitle h1:after {
  content: "(BSL Signed Performance)";
  color: #757575;
}
```

You can find the performance identifier `1234567` using your browsers dev tools on a performance listings page (one that ends in `t-xxxxx`), inspecting the `body` tag and extracting the value of the `data-pid` attribute:

![image](https://github.com/ticketsource/gists/assets/619726/d206b6be-b395-4d57-bb2b-1afb8b0abb74)

![image](https://github.com/ticketsource/gists/assets/619726/160e1ac5-49af-4509-b4a2-0f7b7098a1df)
