﻿### CurrencyISOCode Property

International Standards Organization code for the Country's currency

#### Syntax

```vbnet
'Declaration

<PropertyBitValueAttribute()>
Public Property CurrencyISOCode As String
```

```csharp
[PropertyBitValueAttribute()]
public string CurrencyISOCode {get; set;}
```

#### Remarks

Only used if a new Currency is created by entering a [Currency](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Interfaces.CreateCountrySetup~Currency.md) name that is not already present.

[!include[Requirements](../partials/requirements.md)]

#### Reference

[CreateCountrySetup Class](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Interfaces.CreateCountrySetup.md)  
[CreateCountrySetup Members](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Interfaces.CreateCountrySetup_members.md)