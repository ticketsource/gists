To display events in list view but as a "card" with the image above the title when viewing on a mobile device (< 40em) paste the following into the Custom CSS box 
under Settings > Ticket Shop in your TicketSource account:

```css
@media print, screen and (max-width: 40em) {
    .eventsTable .eventRow .event-image, .eventsTable .eventRow .eventBanner {
        display: block;
    }

    .grid-x.eventRow {
        flex-flow: column wrap;
        padding: 0;
    }

    .eventsTable .eventRow .event-image {
        justify-content: center;
        width: 100%;
        margin-bottom: 1rem;
    }

    .eventsTable .eventRow .event-image .eventBanner img {
        min-width: auto;
        max-width: unset;
        width: 100%;
    }

    .eventsTable .eventRow .eventCol.left {
        padding: 0 1rem;
    }
}
```
