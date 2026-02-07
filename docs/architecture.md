## Product Choice

I chose [Wildberries](https://www.wildberries.ru/).

[Wildberries](https://www.wildberries.ru/) is a popular russian marketplace where one can buy anything. It allows to order stuff using a `postpaid` option.

## Main components

![asdfsad](./../docs/diagrams/out/wildberries/architecture-component/)

> [!NOTE]
>
> According to the [`C4 model`](https://c4model.com/abstractions/component), a *component* is a grouping of related functionality encapsulated behind a well-defined interface.

> [!IMPORTANT]
> Use paths relative to your file.
>
> Replace space in the path with `%20` (see [URL encoding](https://en.wikipedia.org/wiki/Percent-encoding)).
>

1. Embed the product's `Component Diagram.svg`.

   Example: `![Telegram Component Diagram](../../../docs/diagrams/out/telegram/component-diagram/Component%20Diagram.svg)`

   <details><summary>Rendered image (click to open)</summary>

   ![Telegram Component Diagram](../../../docs/diagrams/out/telegram/component-diagram/Component%20Diagram.svg)

   </details>

2. Provide a link to the `PlantUML` code for that [component diagram](../../appendix/architectural-views.md#component-diagram).
  
   Example: [Telegram Component Diagram Code](../../../docs/diagrams/src/telegram/component-diagram.puml)

3. Select at least 5 components of the product from the component diagram.

4. For each selected component, explain in 1-2 sentences what it does (as you think).

## Data flow

1. Embed the product's `Sequence Diagram.svg`.
2. Provide a link to the `PlantUML` code for that [sequence diagram](../../appendix/architectural-views.md#sequence-diagram).
3. Choose a group of actions (a box in the diagram, `group` or `Flow` in the `PlantUML` code).
4. Describe what happens in that group of steps.
5. Mention which components talk to each other and what data they exchange.

## Deployment

1. Embed the product's `Deployment Diagram.svg`.
2. Provide a link to the `PlantUML` code for that [deployment diagram](../../appendix/architectural-views.md#deployment-diagram).
3. Briefly describe where the components are deployed.

## Assumptions

List two or more assumptions you made while describing the architecture. Examples:

- Yandex Go: *"I assume the pricing service handles surge pricing calculations based on demand and supply in real-time."*
- Telegram: *"I assume the cloud storage system implements deduplication to optimize storage costs for shared media files."*
- Wildberries: *"I assume the Logistics & Routing service integrates with multiple delivery partners to optimize shipping costs and delivery times"*

## Open questions

List two or more questions that you couldn't answer based on the openly available information. Examples:

- Yandex Go: *"How does the actual load balancing mechanism work between the microservices in production?"*
- Telegram: *"How does the data flow look like in secret chats?"*
- Wildberries: *"What specific caching strategies are used to handle high traffic during sales events?"*
