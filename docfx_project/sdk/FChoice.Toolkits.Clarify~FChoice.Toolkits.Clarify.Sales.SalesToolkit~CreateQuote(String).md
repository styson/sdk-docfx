﻿### CreateQuote(String) Method

The title of the Quote.

Used to create a new Quote. This overload takes a set of required parameters for the API.

#### Syntax

```vbnet
'Declaration

Public Overloads Function CreateQuote( _
   ByVal _quoteTitle_ As String _
) As ToolkitResult
```

```csharp
public ToolkitResult CreateQuote( 
   string _quoteTitle_
)
```

#### Parameters

_quoteTitle_

The title of the Quote.

#### Return Value

A [ToolkitResult](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.ToolkitResult.md) instance with no properties set. The properties (Objid, IDNum, etc.) are not relevant to this API.

#### Remarks

This API requires that a valid opportunity exists. This differs a little from the Clarify GUI, which creates the opportunity as part of the create quote. That can be done with the APIs, but there is extra flexibility provided.

 As part of creating the contract record for the quote, these APIs also create the default contract schedule and relates the schedule to the contract.

Additional fields may be set on either the contract or contr_schedule table. To set a field on table_contract, just use the field name. To set a field on the contr_schedule table, place “sched:” before the name of the field. For example, to set the “x_foo” field on the contr_schedule table, use a field name of “sched:x_foo”.

[!include[Requirements](../partials/requirements.md)]

#### Reference

[SalesToolkit Class](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Sales.SalesToolkit.md)  
[SalesToolkit Members](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Sales.SalesToolkit_members.md)  
[Overload List](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Sales.SalesToolkit~CreateQuote.md)