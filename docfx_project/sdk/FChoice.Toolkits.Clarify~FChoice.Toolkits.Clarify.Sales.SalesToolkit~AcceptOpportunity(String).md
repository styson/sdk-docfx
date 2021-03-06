﻿### AcceptOpportunity(String) Method

Opportunity Identifier.

Accept the specified Opportunity from the queue in which it is currently dispatched. This overload takes a set of required parameters for the API.

#### Syntax

```vbnet
'Declaration

Public Overloads Function AcceptOpportunity( _
   ByVal _opportunityIDNum_ As String _
) As ToolkitResult
```

```csharp
public ToolkitResult AcceptOpportunity( 
   string _opportunityIDNum_
)
```

#### Parameters

_opportunityIDNum_

Opportunity Identifier.

#### Return Value

A [ToolkitResult](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.ToolkitResult.md) instance with no properties set. The properties (Objid, IDNum, etc.) are not relevant to this API.

#### Remarks

The Opportunity must be currently dispatched to a queue.

[!include[Requirements](../partials/requirements.md)]

#### Reference

[SalesToolkit Class](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Sales.SalesToolkit.md)  
[SalesToolkit Members](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Sales.SalesToolkit_members.md)  
[Overload List](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Sales.SalesToolkit~AcceptOpportunity.md)