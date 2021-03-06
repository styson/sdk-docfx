﻿### LoadEnvironmentSettings() Method

Retrieves the current configuration values or loads new ones if no current ones are available.

#### Syntax

```vbnet
'Declaration

Public Overloads Shared Function LoadEnvironmentSettings() As NameValueCollection
```

```csharp
public static NameValueCollection LoadEnvironmentSettings()
```

#### Return Value

A [NameValueCollection](ms-help://MS.NETFrameworkSDKv1.1/cpref/html/frlrfSystemCollectionsSpecializedNameValueCollectionMembersTopic.htm) of values produced by loading the environment settings either from the provided collection, from the current application configuration, or a merge of both.

#### Remarks

This method will not force a reload of configuration values and will check for required parameters

[!include[Requirements](../partials/requirements.md)]

#### Reference

[FCConfiguration Class](FChoice.Common~FChoice.Common.FCConfiguration.md)  
[FCConfiguration Members](FChoice.Common~FChoice.Common.FCConfiguration_members.md)  
[Overload List](FChoice.Common~FChoice.Common.FCConfiguration~LoadEnvironmentSettings.md)