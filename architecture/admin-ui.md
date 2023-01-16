# Admin UI

The Admin UI is designed to be a lightweight React application which connects to your data sources and allows you to see / edit the data.

As a developer you can customise the Admin UI extensively, adding custom components for dashboards or overriding any data display / edit area with your own components.

The Admin UI is built + packaged with [Vite](https://vitejs.dev/) and can be deployed to any static hosting service such as AWS S3, Vercel, Netlify, Azure Blob storage or your own infrastructure. Simply build the files then deploy the resulting HTML to your static hosting. The Admin UI uses the same GraphWeaver API to talk to your backends as your application uses.

### Schema Information

The Admin UI needs information about your schema in order to know what to show. We decided not to use the [built in introspection query](https://graphql.org/learn/introspection/) for this because that query:

* Divulges information about all operations available in your API, including custom mutations and custom queries. These operations are not required for or used by the Admin area.
* Does not carry all the information we need to show the admin area. We need to know what backend various entities come from and the customisation options you've specified for each field / entity, which is not part of the built in GraphQL schema.

So instead, we built a custom query which we can (optionally) inject into the solution for you. It's accessible under `_graphweaver` and can be used by your own application logic if that's useful, but you shouldn't need to engage with it except to know that that's how the backend communicates to the admin UI the shape of the schema and metadata about it.

You can learn more in [the reference section.](../reference/backend/\_graphweaver-query.md)
