﻿### AssignCase(String) Method

Case Identifier.

Assign the Case to a new user. This overload takes a set of required parameters for the API.

#### Syntax

```vbnet
'Declaration

Public Overloads Function AssignCase( _
   ByVal _caseIDNum_ As String _
) As ToolkitResult
```

```csharp
public ToolkitResult AssignCase( 
   string _caseIDNum_
)
```

#### Parameters

_caseIDNum_

Case Identifier.

#### Return Value

A [ToolkitResult](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.ToolkitResult.md) instance with no properties set. The properties (Objid, IDNum, etc.) are not relevant to this API.

#### Remarks

The Case must be in the Open condition, and the user assigning the Case does not have to be the owner of the Case. In base Clarify, the assigner of a Case must be the owner. If either user name is not specified, the “current” user is used. The date/time of the assignment, and the WipBin to place the Case in can also be specified. Allowing a WipBin other than the default one is also an augmentation from base Clarify.

[!include[Requirements](../partials/requirements.md)]

#### Reference

[SupportToolkit Class](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Support.SupportToolkit.md)  
[SupportToolkit Members](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Support.SupportToolkit_members.md)  
[Overload List](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Support.SupportToolkit~AssignCase.md)