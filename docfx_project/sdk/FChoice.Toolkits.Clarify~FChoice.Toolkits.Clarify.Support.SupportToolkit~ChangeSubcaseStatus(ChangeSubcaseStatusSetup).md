﻿### ChangeSubcaseStatus(ChangeSubcaseStatusSetup) Method

Setup object for API invocation.

Changes the status of a Subcase. This overload takes a setup object.

#### Syntax

```vbnet
'Declaration

Public Overloads Function ChangeSubcaseStatus( _
   ByVal _setupParam_ ChangeSubcaseStatusSetup _
) As ToolkitResult
```

```csharp
public ToolkitResult ChangeSubcaseStatus( 
   ChangeSubcaseStatusSetup _setupParam_
)
```

#### Parameters

_setupParam_

Setup object for API invocation.

#### Return Value

A [ToolkitResult](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.ToolkitResult.md) instance with no properties set. The properties (Objid, IDNum, etc.) are not relevant to this API.

#### Remarks

The Subcase may be opened or closed, but the status selected must be valid for the current condition. In other words, you cannot assign a Closed condition status to a Subcase that is currently Open.

[!include[Requirements](../partials/requirements.md)]

#### Reference

[SupportToolkit Class](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Support.SupportToolkit.md)  
[SupportToolkit Members](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Support.SupportToolkit_members.md)  
[Overload List](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Support.SupportToolkit~ChangeSubcaseStatus.md)  
[ChangeSubcaseStatusSetup Class](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Support.ChangeSubcaseStatusSetup.md)