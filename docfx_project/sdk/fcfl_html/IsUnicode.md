_IsUnicode_
-----------

**Object and Type**

Object : FCSession

Type : Method

**Prototype**

Public Function IsUnicode(in_str As String) As Boolean

**Description**

This method determines if a supplied string is a unicode (wide varchar) string. If it is (it contains at least one Unicode character), the function returns _True._ Otherwise it returns _False._

#### Parameters
**Parameter Name                Required?             Description                                                                                          **

in_str                                      Yes                         The string to test

**Returns**

A boolean value indicating if the input string contains any Unicode characters.

**Example**

**JavaScript:**

The code in this example is written in JavaScript for inclusion in ASP pages.

The following example checks if a given time zone is valid for the given country using the (short) name of the time zone.

var isUnicode = FCSession.IsUnicode(strString);

          // Only write the data to the string field if

          //  it is not Unicode

if (!isUnicode)

{

   boString("string") = strString;

}