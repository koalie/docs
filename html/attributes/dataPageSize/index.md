---
title: 'dataPageSize'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: dataPageSize
  topic: html
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup_Attributes
  - HTML
  - Needs_Summary
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/methods/firstPage
    - dom/methods/lastPage
    - dom/methods/previousPage
uri: html/attributes/dataPageSize

---
<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
 ?

</td>
</tr>
</table>
## Examples

In this example, a text box is bound to the customer\_name field supplied by a data source object with an ID of customer. Because the text box is located within a data-bound [**table**](/html/elements/table), the text box is repeated to display each of the records in the data source. The **DATAPAGESIZE** attribute on the **table** limits the display to 10 records.

``` html
<table datasrc="#customer" datapagesize=10>
   <tr><td><input type=texbox datafld="customer_name"></td></tr>
</table>
```

## Notes

### Remarks

The [**firstPage**](/w/index.php?title=dom/methods/firstPage&action=edit&redlink=1) and [**lastPage**](/w/index.php?title=dom/methods/lastPage&action=edit&redlink=1) methods are used to navigate directly to the first and last pages of a databound table, respectively. The **nextPage** and [**previousPage**](/w/index.php?title=dom/methods/previousPage&action=edit&redlink=1) methods are used to navigate sequentially through the pages of a databound table.

### Syntax

## See also

### Related pages

-   table[table](/html/elements/table)
-   `Reference`
-   firstPage[firstPage](/w/index.php?title=dom/methods/firstPage&action=edit&redlink=1)
-   lastPage[lastPage](/w/index.php?title=dom/methods/lastPage&action=edit&redlink=1)
-   `nextPage`
-   previousPage[previousPage](/w/index.php?title=dom/methods/previousPage&action=edit&redlink=1)
-   `Conceptual`
-   `Introduction to Data Binding`
