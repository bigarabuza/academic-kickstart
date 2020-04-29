---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "ADODB"
linktitle: 
toc: true
type: docs
date: 2020-04-28T06:58:27-04:00
lastmod: 2020-04-28T06:58:27-04:00
draft: false
menu:
  vba:
    adodb:
      name:
      weight: 

---
## ADODB Connection

```vbnet
Const connstring As String = "ConnectionString"
On Error GoTo ErrorHandler

Dim conn As ADODB.Connection
Set conn = New ADODB.Connection
conn.Open connstring  

conn.Close

ErrorHandler:
  If Err <> 0 Then
    MsgBox Err.Source & "-->" & Err.Description, , "Error" 
  End If
```

## ADODB Recordset

```vbnet
Const sql As String = "SELECT Field1, Field2 FROM Table1 WHERE Field3 = ?"
Const connstring As String = "ConnectionString"

Dim conn As ADODB.Connection
Dim cmd As ADODB.Command
Dim rs As ADODB.RecordSet

Set conn = New ADODB.Connection
conn.Open connstring

Set cmd = New ADODB.Command
With cmd
  .ActiveConnection = conn
  .CommandType = adCmdText
  .CommandText = sql
  .Parameters.Append .CreateParameter('Name', 'Type', 'Direction', 'Size', 'Value')
  Set rs = .Execute
End With
  
conn.Close
```

