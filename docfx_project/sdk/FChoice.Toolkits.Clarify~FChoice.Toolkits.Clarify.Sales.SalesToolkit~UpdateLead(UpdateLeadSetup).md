﻿### UpdateLead(UpdateLeadSetup) Method

Setup object for API invocation.

Used to update a Lead. This overload takes a setup object.

#### Syntax

```vbnet
'Declaration

Public Overloads Function UpdateLead( _
   ByVal _setupParam_ UpdateLeadSetup _
) As ToolkitResult
```

```csharp
public ToolkitResult UpdateLead( 
   UpdateLeadSetup _setupParam_
)
```

#### Parameters

_setupParam_

Setup object for API invocation.

#### Return Value

The following values are populated in the [ToolkitResult](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.ToolkitResult.md) object returned by the API method:

*   [Objid](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.ToolkitResult~Objid.md) \- The Objid of the Lead.

#### Remarks

The objid of the Lead is required.

For updates, if data is specified it it will be set. If left blank (“”), the current value is retained. If the string “CLEAR” is used for a value, the value is cleared.  A few items (such as lead source and contact role) cannot be cleared.

The user who updated the lead, and the date/time of the update can be specified. The API can also generate a time bomb (for business rules).

[!include[Requirements](../partials/requirements.md)]

#### Reference

[SalesToolkit Class](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Sales.SalesToolkit.md)  
[SalesToolkit Members](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Sales.SalesToolkit_members.md)  
[Overload List](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Sales.SalesToolkit~UpdateLead.md)  
[UpdateLeadSetup Class](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Sales.UpdateLeadSetup.md)