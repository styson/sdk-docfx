﻿### GetConnection() Method

Gets an [IDbConnection](ms-help://MS.NETFrameworkSDKv1.1/cpref/html/frlrfSystemDataIDbConnectionClassTopic.htm) object instance of the correct type for the underlying database (i.e. [SqlConnection](ms-help://MS.NETFrameworkSDKv1.1/cpref/html/frlrfSystemDataSqlClientSqlConnectionClassTopic.htm) for MSSQL) that is prepared to connect to the specified database using the default connection string specified in the application configuration file.

#### Syntax

```vbnet
'Declaration

Public Overloads MustOverride Function GetConnection() As IDbConnection
```

```csharp
public abstract IDbConnection GetConnection()
```

#### Return Value

An [IDbConnection](ms-help://MS.NETFrameworkSDKv1.1/cpref/html/frlrfSystemDataIDbConnectionClassTopic.htm) object instance of the correct type for the underlying database (i.e. [SqlConnection](ms-help://MS.NETFrameworkSDKv1.1/cpref/html/frlrfSystemDataSqlClientSqlConnectionClassTopic.htm) for MSSQL).

#### Remarks

The connection instance is not open by default. In order to open the connection, use the [Open](ms-help://MS.NETFrameworkSDKv1.1/cpref/html/frlrfSystemDataIDbConnectionClassTopic.htm) method on the [IDbConnection](ms-help://MS.NETFrameworkSDKv1.1/cpref/html/frlrfSystemDataIDbConnectionClassTopic.htm) reference returned by this method.

[!include[Requirements](../partials/requirements.md)]

#### Reference

[DbProvider Class](FChoice.Common~FChoice.Common.Data.DbProvider.md)  
[DbProvider Members](FChoice.Common~FChoice.Common.Data.DbProvider_members.md)  
[Overload List](FChoice.Common~FChoice.Common.Data.DbProvider~GetConnection.md)