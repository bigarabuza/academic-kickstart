---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Pivot Tables"
linktitle: 
toc: true
type: docs
date: 2020-05-31
lastmod: 2020-06-01
draft: false
menu:
  vba:
    pivottable:
      name:
      weight: 2

---
## Create a Pivot Table

```vbnet
Dim PC As PivotCache
Set PC = ThisWorkbook.PivotCaches.Create( _
            SourceType:='xlDatabase', 'xlConsolidation', 'xlExternal'
            SourceData:='Range'
          )     

Dim PT As PivotTable
Set PT = PC.CreatePivotTable( _
            TableDestination:='Range'
            TableName:='TableName'
            ) 

PT.AddFields _ 
    'RowFields', _
    'ColumnFields', _
    'PageFields' 'NB: if there are multiple items, place in Array('Field', 'Field')

PT.AddDataField PT.PivotFields('FieldName', , 'Function' )
```
