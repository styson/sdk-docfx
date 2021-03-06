﻿### GetDBDate Method (DbProvider)

Executes a statement against the database to retrieve the current date/time on the database

#### Syntax

```vbnet
'Declaration

Public MustOverride Function GetDBDate() As Date
```

```csharp
public abstract DateTime GetDBDate()
```

#### Return Value

The current date and time on the database server

#### Remarks

The date and time returned by this method will be in the database's time zone. If the application is configured for a different time zone, conversion must be done manually. For information on performing time zone conversions using **FCFL.NET**, please see the following methods on the [FCSession](fcSDK~FChoice.Foundation.FCSession.md) class: [ChangeDate](fcSDK~FChoice.Foundation.FCSession~ConvertDate.md), [ConvertFromLocalToServerDate](fcSDK~FChoice.Foundation.FCSession~ConvertFromLocalToServerDate.md), and [ConvertFromServerToLocalDate](fcSDK~FChoice.Foundation.FCSession~ConvertFromServerToLocalDate.md).

[!include[Requirements](../partials/requirements.md)]

#### Reference

[DbProvider Class](FChoice.Common~FChoice.Common.Data.DbProvider.md)  
[DbProvider Members](FChoice.Common~FChoice.Common.Data.DbProvider_members.md)  
**FCSession Class**