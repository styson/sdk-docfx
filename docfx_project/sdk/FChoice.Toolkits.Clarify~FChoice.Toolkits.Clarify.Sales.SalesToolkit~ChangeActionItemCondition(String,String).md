﻿### ChangeActionItemCondition(String,String) Method

Action Item Identifier.

The new condition for the Action Item

Used to change the condition and (optionally) a status for the specified Action Item. This overload takes a set of required parameters for the API.

#### Syntax

```vbnet
'Declaration

Public Overloads Function ChangeActionItemCondition( _
   ByVal _actionItemIDNum_ As String, _
   ByVal _newcondition_ As String _
) As ToolkitResult
```

```csharp
public ToolkitResult ChangeActionItemCondition( 
   string _actionItemIDNum_,
   string _newcondition_
)
```

#### Parameters

_actionItemIDNum_

Action Item Identifier.

_newcondition_

The new condition for the Action Item

#### Return Value

The following values are populated in the [ToolkitResult](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.ToolkitResult.md) object returned by the API method:

*   [IDNum](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.ToolkitResult~IDNum.md) \- The IDNum of the ActionItem.
*   [Objid](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.ToolkitResult~Objid.md) \- The Objid of the ActionItem.

#### Remarks

The Action Item ID and the condition is required, but no other data is. The API can also generate a time bomb (for business rule notification).

[!include[Requirements](../partials/requirements.md)]

#### Reference

[SalesToolkit Class](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Sales.SalesToolkit.md)  
[SalesToolkit Members](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Sales.SalesToolkit_members.md)  
[Overload List](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Sales.SalesToolkit~ChangeActionItemCondition.md)