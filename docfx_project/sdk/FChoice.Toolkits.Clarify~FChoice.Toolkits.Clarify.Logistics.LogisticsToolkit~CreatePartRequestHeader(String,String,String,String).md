﻿### CreatePartRequestHeader(String,String,String,String) Method

Contact's first name.

Contact's last name.

Contact's phone number.

Identifier of the Site where this Part Request should be shipped

Used to create a new part request header.

This overload takes a set of required parameters for the API.

#### Syntax

```vbnet
'Declaration

Public Overloads Function CreatePartRequestHeader( _
   ByVal _contactFirstName_ As String, _
   ByVal _contactLastName_ As String, _
   ByVal _contactPhone_ As String, _
   ByVal _shipToSiteIDNum_ As String _
) As ToolkitResult
```

```csharp
public ToolkitResult CreatePartRequestHeader( 
   string _contactFirstName_,
   string _contactLastName_,
   string _contactPhone_,
   string _shipToSiteIDNum_
)
```

#### Parameters

_contactFirstName_

Contact's first name.

_contactLastName_

Contact's last name.

_contactPhone_

Contact's phone number.

_shipToSiteIDNum_

Identifier of the Site where this Part Request should be shipped

#### Return Value

The following values are populated in the [ToolkitResult](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.ToolkitResult.md) object returned by the API method:

*   [Objid](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.ToolkitResult~Objid.md) \- The Objid of the Header.
*   [IDNum](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.ToolkitResult~IDNum.md) \- The IDNum of the Header.

#### Remarks

If using the [CreatePartRequestHeaderSetup](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Logistics.CreatePartRequestHeaderSetup.md) variant of this API, and if the [CaseIDNum](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Logistics.CreatePartRequestHeaderSetup~CaseIDNum.md) property on the [CreatePartRequestHeaderSetup](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Logistics.CreatePartRequestHeaderSetup.md) object is set to a value, and there is a dash ("-") in the identifier, it will be assumed that it is a subcase identifier. Otherwise, it will be treated as a case identifier.

To create a Part Request Header for a case or subcase, without respect for dashes ("-") in the case/subcase identifier, see the [CreatePartRequestHeaderCase](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Logistics.LogisticsToolkit~CreatePartRequestHeaderCase.md) or the [CreatePartRequestHeaderSubcase](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Logistics.LogisticsToolkit~CreatePartRequestHeaderSubcase.md) APIs respectively.

**NOTE**: If you have one or more dashes ("-") in your case identifier numbering scheme, you **MUST** use one of the two CreatePartRequestHeaderCase/Subcase variants. Do not use this API (CreatePartRequestHeader) as it will mistakenly identify every case identifier as a subcase.

**NOTE**: The [ContractObjId](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Logistics.CreatePartRequestHeaderSetup~ContractObjid.md) property on the [CreatePartRequestHeaderSetup](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Logistics.CreatePartRequestHeaderSetup.md) object should not be set (left as default) unless you need this functionality AND have installed the First Choice ClearCallCenter for ClearLogistics product and schema changes. If you do not have this product and wish to use this functionality, please contact First Choice Software.

[!include[Requirements](../partials/requirements.md)]

#### Reference

[LogisticsToolkit Class](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Logistics.LogisticsToolkit.md)  
[LogisticsToolkit Members](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Logistics.LogisticsToolkit_members.md)  
[Overload List](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Logistics.LogisticsToolkit~CreatePartRequestHeader.md)