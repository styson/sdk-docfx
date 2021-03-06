﻿### SetPartStockingLevelSetup Constructor

The names of the restocking location/bin

The queue to which the reorder part request will be dispatched

Part number for the Part

Part revision of the Part

Part domain of the Part

Minimum quantity of parts allowed in this inventory location

Maximum quantity of parts allowed in this inventory location

The quantity of parts that will trigger a reorder Part Request to be created for this inventory location

Quantity of parts to be reordered for this inventory location when reorder level is reached

Initializes a new instance of the SetPartStockingLevelSetup class.

#### Syntax

```vbnet
'Declaration

<ConstructorIndexAttribute()>
Public Function New( _
   ByVal _location_ As Location, _
   ByVal _queue_ As String, _
   ByVal _partNumber_ As String, _
   ByVal _partRevision_ As String, _
   ByVal _partDomain_ As String, _
   ByVal _partMinimum_ As Short, _
   ByVal _partMaximum_ As Short, _
   ByVal _partReorderLevel_ As Short, _
   ByVal _partReorderQuantity_ As Short _
)
```

```csharp
[ConstructorIndexAttribute()]
public SetPartStockingLevelSetup( 
   Location _location_,
   string _queue_,
   string _partNumber_,
   string _partRevision_,
   string _partDomain_,
   short _partMinimum_,
   short _partMaximum_,
   short _partReorderLevel_,
   short _partReorderQuantity_
)
```

#### Parameters

_location_

The names of the restocking location/bin

_queue_

The queue to which the reorder part request will be dispatched

_partNumber_

Part number for the Part

_partRevision_

Part revision of the Part

_partDomain_

Part domain of the Part

_partMinimum_

Minimum quantity of parts allowed in this inventory location

_partMaximum_

Maximum quantity of parts allowed in this inventory location

_partReorderLevel_

The quantity of parts that will trigger a reorder Part Request to be created for this inventory location

_partReorderQuantity_

Quantity of parts to be reordered for this inventory location when reorder level is reached

[!include[Requirements](../partials/requirements.md)]

#### Reference

[SetPartStockingLevelSetup Class](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Logistics.SetPartStockingLevelSetup.md)  
[SetPartStockingLevelSetup Members](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Logistics.SetPartStockingLevelSetup_members.md)