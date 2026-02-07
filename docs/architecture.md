## Product Choice

I chose [Wildberries](https://www.wildberries.ru/).

[Wildberries](https://www.wildberries.ru/) is a popular russian marketplace where one can buy anything. It allows to order stuff using a `postpaid` option.

## Main components

<details>

<summary>Rendered image (click to open)</summary>

![Wildberries Component Diagram](./diagrams/out/wildberries/architecture-component/Component%20Diagram.svg)

</details>

[Wildberries Component Diagram Code](./diagrams/src/wildberries/architecture-component.puml)

### Customer Mobile App

The Customer Mobile App is probably a native (I hope so) mobile application aimed at customers. By "native" I mean an application that was written using Kotlin for Android and Swift for iOS. Despite React Native using native widgets for each corresponding platform, I do not believe that React Native can be called a native tech stack due to having JS interops.

### Customer Website (SSR)

The Customer Website (SSR) is a website aimed at customers. Judging by the name, it uses a Server-Sider Rendering technique (present in Next.js, Nuxt, SvelteKit, etc.)

### WB Partners App (Seller)

The WB Partners App (Seller) seems to be an application aimed at WB partners, i.e., sellers.

### PVZ Software (Pickup Point)

<details>
Plants vs. Zombies
</details>

The PVZ software is a software that probably allows to interact with the pickup point.

### Warehouse Terminals

Since this component is in the client layer, Warehouse Terminals must be related to end users.

## Data flow

![Wildberries Sequence Diagram](./diagrams/out/wildberries/architecture-sequence/Sequence%20Diagram.svg)

[A Sequence Diagram PlantUML code](../lab/appendix/architectural-views.md#sequence-diagram)

### Payment Callback & Finalization

They attach a webhook to handle successful payments.

After the success, a callback is triggered to handle the database update.

Then they publish an `OrderPaid` event.

The Checkout and Warehouse Fulfillment groups of actions depend on this group (Payment Callback & Finalization).

## Deployment

![Wildberries Deployment Diagram](./diagrams/out/wildberries/architecture-deployment/Deployment%20Diagram.svg)

[A Deployment Diagram PlantUML code](../lab/appendix/architectural-views.md#deployment-diagram)

These components are deployed in various places, e.g., hosted servers or CDNs.

## Assumptions

I assume:

- the customer website uses Server-Side Rendering to decrease the loading times for users;
- the customer mobile app uses React Native or Flutter to decrease the cost for maintaining the application on Android and iOS.

## Open questions

I wonder:

- if Wildberries uses Redis for the caching part;
- if Wildberries uses Nix to manage the servers in a declarative and reproducible way.
