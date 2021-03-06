﻿### BackorderPartRequestSetup Constructor(String,DateTime,Int32)

Part Request Detail Identifier

The DateTime the Part Request backordered parts are expected to arrive. If not set, the current time is used.

The number of parts being backordered for this Part Request

Initializes a new instance of the BackorderPartRequestSetup class. This overload takes a set of required parameters for the API.

#### Syntax

```vbnet
'Declaration
 
<ConstructorIndexAttribute()>
Public Function New( _
   ByVal _partRequestDetailIDNum_ As String, _
   ByVal _expectedDate_ As Date, _
   ByVal _quantity_ As Integer _
)
```

```csharp
[ConstructorIndexAttribute()]
public BackorderPartRequestSetup( 
   string _partRequestDetailIDNum_,
   DateTime _expectedDate_,
   int _quantity_
)
```

#### Parameters

_partRequestDetailIDNum_

Part Request Detail Identifier

_expectedDate_

The DateTime the Part Request backordered parts are expected to arrive. If not set, the current time is used.

_quantity_

The number of parts being backordered for this Part Request

[!include[Requirements](../partials/requirements.md)]

#### Reference

[BackorderPartRequestSetup Class](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Logistics.BackorderPartRequestSetup.md)  
[BackorderPartRequestSetup Members](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Logistics.BackorderPartRequestSetup_members.md)  
[Overload List](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Logistics.BackorderPartRequestSetup~_ctor.md)