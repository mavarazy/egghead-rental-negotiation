# egghead-rental-negotiation
In this course we'll be building a software for negotiating rental aggreements between Landlord & Tenants, with ability to sign and download final PDF.

## Technologies

Our goal is to compare final project in 4 stacks:
- Next.JS
- Solid.JS
- Svelte
- Astro

We are going to be building this on top of Firebase for simplicity sake.
For css we are going to use TailwindCSS.

## Rental agreement State flow

Rental Aggrement is a document created by the 

```mermaid
stateDiagram-v2
    [*] --> Preview
    Preview --> Negotiation: Tenant found
    Negotiation --> Accepted: Accept,\nno edits needed
    Negotiation --> Edits: Some edits needed
    Approved --> Edits: Additional\nedits needed
    Edits --> Approved: Landlord\naccepted\nchanges
    Edits --> Declined: Landlord\ndeclined
    Declined --> Edits: Renegotiate
    Declined --> Rejected: Reject
    Approved --> Accepted: Accept
    Accepted --> Signed: Signed by tenant
    Signed --> Sealed: Signed by landlord
    Sealed --> [*]
```
