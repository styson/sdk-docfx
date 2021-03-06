﻿### GetCaseTimeAndExpenses(String) Method

Case Identifier.

Captures all the summed times (such as phone log time, billable and non-billable expense, etc) for a Case about to be closed. This overload takes a set of required parameters for the API.

#### Syntax

```vbnet
'Declaration

Public Overloads Function GetCaseTimeAndExpenses( _
   ByVal _caseIDNum_ As String _
) As GetCaseTimeAndExpensesResult
```

```csharp
public GetCaseTimeAndExpensesResult GetCaseTimeAndExpenses( 
   string _caseIDNum_
)
```

#### Parameters

_caseIDNum_

Case Identifier.

#### Return Value

The following values are populated in the GetCaseTimeAndExpensesResult object returned by the API method:

*   CaseTimeAndExpenses \- Contains the sums and totals of time and expenses calculated before closing a Case.

#### Remarks

There are a number of bugs with the default Clarify close Case summation on the form. There are not sufficient fields defined in the close_case record for the graphical fields they show. Hence, the data doesn't always make sense. For example, the total phone time captured should be the total of the phone time captured for the Case and for all general subcases. But the GUI form points that field to the total for the phone logs captured for the Case (not showing the Subcase). Hence, this API defines the data as captured from the real data.

[!include[Requirements](../partials/requirements.md)]

#### Reference

[SupportToolkit Class](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Support.SupportToolkit.md)  
[SupportToolkit Members](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Support.SupportToolkit_members.md)  
[Overload List](FChoice.Toolkits.Clarify~FChoice.Toolkits.Clarify.Support.SupportToolkit~GetCaseTimeAndExpenses.md)