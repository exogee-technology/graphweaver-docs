# Admin UI

## Standard (bundled) Admin UI

TODO standard Admin UI pages...

## User-defined Admin UI

TODO


## Admin UI Components

React.js components

TODO

To make use of these components in your own Admin UI, import them from the `@exogee/admin-ui-components` package.

### Built-in Components

...

#### Filters

The standard Admin UI pages can use a set of Filter components to refine data to be retrieved in the List page. These work by passing search parameters to the Admin UI URL, so that results can be easily shared if required. Not all displayed columns can be filtered.

The following filter types come as standard within the Admin UI Components library.

##### 1. Text Filter
`TextFilter`
Metadata type name: `text`
Provides a drop-down list of available values (for example, Account Name).

##### 2. Enumeration Filter
`EnumFilter`
Metadata type name: `enum`
For fields which have a fixed set of values defined in the schema. This is a drop down list of available values for the enumerated type field (for example, Account Type).

##### 3. Relationship Filter
`RelationshipFilter`
Metadata type name: `relationship`
Where a field defines a relationship to another entity, this filter enables search for records which are associated with a specific entity value. For example, Tenant on Accounts.

##### 4. Date Filter
`DateFilter`
Metadata type name: `date`
At present this filter works by allowing the user to select a single date, and will filter to a set of records which have the corresponding date within a 24-hour period starting at midnight on the selected date.

...
### User-defined Components

TODO Specify how to incorporate user-defined components in a package bundled with GW and how to make them available within a user-specified UI.

...
#### Filter component props
These are the props expected by the Graphweaver frontend:
| name | type | default | description | example |
| ---- | ---- | ------- | ----------- | ------- |
| fieldName | string | - | required | `'name'` |
| entity | string | - | required | `'Account'` |
| entityLinkField | string | - | required for `RelationshipFilter` - 'foreign key' link to relationship from entity | `'tenantId'` |
| labelField | string | - | optional - field containing name of relationship entity | `'summaryField'` |
| value | SelectOption | Set by Admin UI | required, can be undefined. Controlled data field for current filter value | |
| onChange | function(fieldName: string, option?: SelectOption): void | Set by Admin UI | optional. Function used to handle filter setting | |
