﻿### FromLocation Property (FulfillPartRequestSetup)

The inventory location and bin containing the parts used to fulfill this Part Request

#### Syntax

```vbnet
'Declaration

<PropertyBitValueAttribute()>
Public Property FromLocation As Location
```

```csharp
[PropertyBitValueAttribute()]
public Location FromLocation {get; set;}
```

#### Remarks

To use a primary bin suggestion/recommendation that has been previously configured, use the [special constructor](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Location~_ctor(String,Boolean).md) for the Location object and set the _isPrimaryBinSuggestion_ parameter to true.

[!include[Requirements](../partials/requirements.md)]

#### Reference

[FulfillPartRequestSetup Class](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Logistics.FulfillPartRequestSetup.md)  
[FulfillPartRequestSetup Members](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Logistics.FulfillPartRequestSetup_members.md)