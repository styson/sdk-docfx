﻿### RemoveEmployeeFromAccount(String,String,String) Method

Username of the Employee to be removed from the Account.

Identifier for the Account the Employee will be removed from.

Employee Role to be removing from the Account

Remove an Employee from an Account. This overload takes a set of required parameters for the API.

#### Syntax

```vbnet
'Declaration

Public Overloads Function RemoveEmployeeFromAccount( _
   ByVal _userName_ As String, _
   ByVal _accountIDNum_ As String, _
   ByVal _roleName_ As String _
) As ToolkitResult
```

```csharp
public ToolkitResult RemoveEmployeeFromAccount( 
   string _userName_,
   string _accountIDNum_,
   string _roleName_
)
```

#### Parameters

_userName_

Username of the Employee to be removed from the Account.

_accountIDNum_

Identifier for the Account the Employee will be removed from.

_roleName_

Employee Role to be removing from the Account

#### Return Value

A [ToolkitResult](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.ToolkitResult.md) instance with no properties set. The properties (Objid, IDNum, etc.) are not relevant to this API.

[!include[Requirements](../partials/requirements.md)]

#### Reference

[InterfacesToolkit Class](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Interfaces.InterfacesToolkit.md)  
[InterfacesToolkit Members](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Interfaces.InterfacesToolkit_members.md)  
[Overload List](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Interfaces.InterfacesToolkit~RemoveEmployeeFromAccount.md)