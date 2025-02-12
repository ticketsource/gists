[< back](../)

To add custom text to a specific performance on your listings pages (e.g. to mark a BSL/British Sign Language performance) add the following to the Custom CSS box under Settings > Ticket Shop in your TicketSource account:

```css
.eventRow[data-id="1234567"] .eventTitle span,
.eventRow[data-id="1234567"] .event-title span {
  display: flex;
  flex-direction: column;
}

.eventRow[data-id="1234567"] .eventTitle span:after,
.eventRow[data-id="1234567"] .event-title span:after,
body[data-pid="1234567"] .heading .eventTitle h1:after {
  content: "(BSL Signed Performance)";
  color: #757575;
}
```

You can find the performance identifier `1234567` using your browsers dev tools on a performance listings page (one that ends in `t-xxxxx`), inspecting the `body` tag and extracting the value of the `data-pid` attribute:

![image](https://github.com/user-attachments/assets/ee2587df-677a-4b67-a01c-53efd48fac21)

![image](https://github.com/user-attachments/assets/a589496a-fef3-479f-950f-c47b7ec97b93)

