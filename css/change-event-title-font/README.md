To change the event title font on your listings pages add the following to the Custom CSS box under Settings > Ticket Shop in your TicketSource account:

```css
.eventTitle h1 {
    font-family: system-ui, "Segoe UI", Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
}
```

This snippet will change the title to use a device's "system font", i.e. whichever font it uses for standard text display.

The event title on each card when using one of the `Card` views can be modified using the following rule:

```css
.result-card .event-content .event-title {
    font-family: system-ui, "Segoe UI", Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
}
```

you can combine the two rules like this:

```css
.eventTitle h1, .result-card .event-content .event-title {
    font-family: system-ui, "Segoe UI", Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
}
```
