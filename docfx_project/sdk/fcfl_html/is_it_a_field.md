_is_it_a_field_
-----------------

**Object and Type**

Object  : FCApp

Type     : Method

**Prototype**

```
Public Function is_it_a_field(tbl_name As String, _
                              field_name As String) As Boolean
``` 

#### Description

This method returns whether a given field name is defined as a field on the specified table. This method also works for fields defined in views.

#### Parameters

| Parameter Name | Required? | Description |
|:--- |:--- |:--- |
| tbl_name | Yes | Name of the table or view |
| field_name | Yes | Name of the field. |

**Returns**

A boolean (true/false) that tells if the field is a valid field in the table.

**Example**

The example shows if "id_number" is a valid field in the case table.

**Visual Basic:**
```
Debug.Print "Is the field 'id_number' in the case table? " & _
      CStr(FCApp.is_it_a_field("case", "id_number"))
```