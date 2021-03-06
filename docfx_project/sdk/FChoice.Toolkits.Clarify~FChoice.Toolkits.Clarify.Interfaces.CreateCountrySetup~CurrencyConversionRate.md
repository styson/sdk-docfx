﻿### CurrencyConversionRate Property

Conversion rate for the currency

#### Syntax

```vbnet
'Declaration

<PropertyBitValueAttribute()>
Public Property CurrencyConversionRate As Double
```

```csharp
[PropertyBitValueAttribute()]
public double CurrencyConversionRate {get; set;}
```

#### Remarks

Only used if a new Currency is created by entering a country [Currency](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Interfaces.CreateCountrySetup~Currency.md) name that is not already present.

[!include[Requirements](../partials/requirements.md)]

#### Reference

[CreateCountrySetup Class](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Interfaces.CreateCountrySetup.md)  
[CreateCountrySetup Members](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Interfaces.CreateCountrySetup_members.md)