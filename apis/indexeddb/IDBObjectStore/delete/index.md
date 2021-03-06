---
title: 'delete'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://nparashuram.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Delete%20Data&'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/indexeddb/IDBObjectStore
    href: /apis/indexeddb/IDBObjectStore
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/indexeddb/IDBObjectStore
standardization_status: 'W3C Proposed Recommendation'
summary: 'Removes a record from the specified Object Store.'
tags:
  - API_Object_Methods
  - API
  - IndexedDB
uri: apis/indexeddb/IDBObjectStore/delete

---
## Summary

Removes a record from the specified Object Store.

Method of [apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)[apis/indexeddb/IDBObjectStore](/apis/indexeddb/IDBObjectStore)

## Syntax

``` js
var idbRequest = objectStore.delete(key);
```

## Parameters

### key

 Data-type
:   String

 Key identifying the record to be deleted

## Return Value

Returns an object of type DOM NodeDOM Node

Returns an IDBRequest Object

## Examples

``` js
store = db.createObjectStore("store1", { autoIncrement: true });
store.put("a"); // Will get key 1
store.delete(1);
store.put("b"); // Will get key 2
store.clear();
store.put("c"); // Will get key 3
store.delete(IDBKeyRange.lowerBound(0));
```

[View live example](http://nparashuram.com/trialtool/index.html#example=/IndexedDB/trialtool/moz_indexedDB.html&selected=Delete%20Data&)

## Notes

### Remarks

This method can throw the following [**DOMException**](/dom/DOMException) exceptions:

<table>
<col width="50%" />
<col width="50%" />
<tbody>
<tr class="odd">
<td align="left"><strong>Exception properties</strong></td>
<td align="left"><strong>Description</strong></td>
</tr>
<tr class="even">
<td align="left"><dl>
<p></p>
<dt>
<strong>name</strong>: ReadOnlyError
</dt>
</dl></td>
<td align="left">The associated transaction is read-only.</td>
</tr>
<tr class="odd">
<td align="left"><dl>
<p></p>
<dt>
<strong>name</strong>: TransactionInactiveError
</dt>
</dl></td>
<td align="left">The associated transaction is not active.</td>
</tr>
</tbody>
</table>

## Related specifications

[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation
