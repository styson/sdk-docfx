_IsState_
------
**Object and Type**

Object  : FCApplication

Type     : Method

**Prototype**

```
Public Function IsState(ByVal Country As String, ByVal State As String) As Boolean
```

#### Description

This method returns a boolean indicating if the given state is valid for the given country.  The state and country tables are cached in the FCApplication object, so this method does not cause a database round-trip.

#### Parameters

| Parameter Name | Required? | Description |
|:--- |:--- |:--- |
| Country | Yes | Name of country. |
| State | Yes | Name of state to be validated. |

**Returns**

A boolean indicating if the given state is valid for the given country. 

**Error Codes**

| Value | Meaning |
|:--- |:--- |
| 10011 | Country must not be empty. |
| 10013 | State must not be empty. |

#### Examples

The following example checks is a given state from a posted form is valid for the posted country.

**JavaScript:**
```
var country = Request.Form("country").Item;

var state = Request.Form("state").Item; 

If (FCApp.IsState(country,state)
{
  Response.Write(state + " is a valid state in " + country);
}
else
{
  Response.Write(state + " is NOT a valid state in " + country);
}
```