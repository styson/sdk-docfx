﻿### SendEmail Property (LogSubcaseEmailSetup)

Specifies if a timebomb be added to Clarify that will cause Rule Manager (if running) to send the email.

#### Syntax

```vbnet
'Declaration

<PropertyBitValueAttribute()>
Public Property SendEmail As Boolean
```

```csharp
[PropertyBitValueAttribute()]
public bool SendEmail {get; set;}
```

#### Remarks

If you set the send_email argument to True, the API will add a row to Clarify that will cause the rule manager (which must be running) to send the email. This is just like logging it via the Log Email GUI in Clarify. The downside of this is that rulemanager sends the email from the server, which means that the recipient(s) cannot hit "reply", and have the email come back to you.

[!include[Requirements](../partials/requirements.md)]

#### Reference

[LogSubcaseEmailSetup Class](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Support.LogSubcaseEmailSetup.md)  
[LogSubcaseEmailSetup Members](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Support.LogSubcaseEmailSetup_members.md)