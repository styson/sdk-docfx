﻿### ChangeActionItemStatus(String) Method

Action Item Identifier.

Cause the specified Action Item to have its status changed. This overload takes a set of required parameters for the API.

#### Syntax

```vbnet
'Declaration

Public Overloads Function ChangeActionItemStatus( _
   ByVal _actionItemIDNum_ As String _
) As ToolkitResult
```

```csharp
public ToolkitResult ChangeActionItemStatus( 
   string _actionItemIDNum_
)
```

#### Parameters

_actionItemIDNum_

Action Item Identifier.

#### Return Value

A [ToolkitResult](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.ToolkitResult.md) instance with no properties set. The properties (Objid, IDNum, etc.) are not relevant to this API.

#### Remarks

The object may be in any valid condition, but the status selected MUST be valid for the current condition.

[!include[Requirements](../partials/requirements.md)]

#### Reference

[SalesToolkit Class](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Sales.SalesToolkit.md)  
[SalesToolkit Members](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Sales.SalesToolkit_members.md)  
[Overload List](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Sales.SalesToolkit~ChangeActionItemStatus.md)