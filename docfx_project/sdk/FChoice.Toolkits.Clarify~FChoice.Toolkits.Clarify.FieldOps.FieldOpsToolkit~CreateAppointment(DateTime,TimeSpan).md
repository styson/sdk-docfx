﻿### CreateAppointment(DateTime,TimeSpan) Method

The DateTime the Appointment starts. If not set, the current time is used.

The length (in seconds) of the appointment. If not specified, it is calculated from the start and end times.

#### Syntax

```vbnet
'Declaration

Public Overloads Function CreateAppointment( _
   ByVal _startDate_ As Date, _
   ByVal _duration_ As TimeSpan _
) As CreateAppointmentResult
```

```csharp
public CreateAppointmentResult CreateAppointment( 
   DateTime _startDate_,
   TimeSpan _duration_
)
```

#### Parameters

_startDate_

The DateTime the Appointment starts. If not set, the current time is used.

_duration_

The length (in seconds) of the appointment. If not specified, it is calculated from the start and end times.

#### Return Value

The following values are populated in the CreateAppointmentResult object returned by the API method:

*   ScheduleObjid \- The Objid of the Schedule.
*   Objid \- The Objid of the Appointment.

[!include[Requirements](../partials/requirements.md)]

#### Reference

[FieldOpsToolkit Class](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.FieldOps.FieldOpsToolkit.md)  
[FieldOpsToolkit Members](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.FieldOps.FieldOpsToolkit_members.md)  
[Overload List](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.FieldOps.FieldOpsToolkit~CreateAppointment.md)