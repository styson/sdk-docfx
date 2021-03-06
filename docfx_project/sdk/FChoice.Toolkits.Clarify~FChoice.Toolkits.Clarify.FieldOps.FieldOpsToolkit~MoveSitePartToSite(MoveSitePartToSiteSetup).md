﻿### MoveSitePartToSite(MoveSitePartToSiteSetup) Method

Setup object for API invocation.

Move the SitePartToSite from one WipBin to another WipBin. This overload takes a setup object.

#### Syntax

```vbnet
'Declaration

Public Overloads Function MoveSitePartToSite( _
   ByVal _setupParam_ MoveSitePartToSiteSetup _
) As ToolkitResult
```

```csharp
public ToolkitResult MoveSitePartToSite( 
   MoveSitePartToSiteSetup _setupParam_
)
```

#### Parameters

_setupParam_

Setup object for API invocation.

#### Return Value

A [ToolkitResult](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.ToolkitResult.md) instance with no properties set. The properties (Objid, IDNum, etc.) are not relevant to this API.

#### Remarks

The new WipBin must belong to the same user as the first WipBin. The move operation does not change the ownership of the SitePartToSite, nor is an activity log or time bomb generated for the action.

Note: This API allows you to move a queueable object from one WipBin to another, even if the object is currently dispatched. Since WipBins are internal to a user, there really is no reason that you shouldn’t be able to move the interal (to a user) location of the object. This is an enhancement to base Clarify function, which requires that the object not be dispatched to be moved.

[!include[Requirements](../partials/requirements.md)]

#### Reference

[FieldOpsToolkit Class](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.FieldOps.FieldOpsToolkit.md)  
[FieldOpsToolkit Members](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.FieldOps.FieldOpsToolkit_members.md)  
[Overload List](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.FieldOps.FieldOpsToolkit~MoveSitePartToSite.md)  
[MoveSitePartToSiteSetup Class](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.FieldOps.MoveSitePartToSiteSetup.md)