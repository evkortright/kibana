[Cases Client API Interface](../README.md) / [client](../modules/client.md) / [\_internal\_namespace](../modules/client._internal_namespace.md) / SavedObjectMigrationMap

# Interface: SavedObjectMigrationMap

[client](../modules/client.md).[_internal_namespace](../modules/client._internal_namespace.md).SavedObjectMigrationMap

A map of [migration functions](../modules/client._internal_namespace.md#savedobjectmigrationfn) to be used for a given type.
The map's keys must be valid semver versions, and they cannot exceed the current Kibana version.

For a given document, only migrations with a higher version number than that of the document will be applied.
Migrations are executed in order, starting from the lowest version and ending with the highest one.

**`example`**
```typescript
const migrationsMap: SavedObjectMigrationMap = {
  '1.0.0': migrateToV1,
  '2.1.0': migrateToV21
}
```

## Indexable

▪ [version: `string`]: [`SavedObjectMigrationFn`](../modules/client._internal_namespace.md#savedobjectmigrationfn)<`any`, `any`\>
