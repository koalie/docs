---
title: 'deleteTFoot'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, clean-up of MSDN import'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/HTMLTableElement
    href: /dom/HTMLTableElement
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/HTMLTableElement
tags:
  - API_Object_Methods
  - DOM
  - Needs_Summary
uri: dom/HTMLTableElement/deleteTFoot

---
Method of [dom/HTMLTableElement](/dom/HTMLTableElement)[dom/HTMLTableElement](/dom/HTMLTableElement)

## Syntax

``` js
var object = object.deleteTFoot();
```

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

This example uses the **deleteTFoot** method to delete the **tFoot** element from the table.

``` html
document.all.myTable.deleteTFoot()
```

## Notes

### Remarks

If only one **tFoot** element exists in the source, the **deleteTFoot** method deletes the table footer. If multiple **tFoot** elements have been defined, the next **tFoot** element in the source order is promoted as the table footer.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5

## See also

### Related pages

-   table[table](/html/elements/table)
