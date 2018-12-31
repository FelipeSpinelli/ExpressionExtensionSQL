ExpressionExtensionSQL - is a sample lambda expression to sql converter .NET
========================================

Packages
--------

Nugget feed: https://www.nuget.org/packages/ExpressionExtensionSQL/

| Package | NuGet Stable | NuGet Pre-release | Downloads |
| ------- | ------------ | ----------------- | --------- | 
| [ExpressionExtensionSQL](https://www.nuget.org/packages/ExpressionExtensionSQL/) | [![ExpressionExtensionSQL](https://img.shields.io/nuget/v/ExpressionExtensionSQL.svg)](https://www.nuget.org/packages/ExpressionExtensionSQL/) | [![ExpressionExtensionSQL](https://img.shields.io/nuget/vpre/ExpressionExtensionSQL.svg)](https://www.nuget.org/packages/ExpressionExtensionSQL/) | [![ExpressionExtensionSQL](https://img.shields.io/nuget/dt/ExpressionExtensionSQL.svg)](https://www.nuget.org/packages/ExpressionExtensionSQL/) |
| [ExpressionExtensionSQL.Dapper](https://www.nuget.org/packages/ExpressionExtensionSQL.Dapper/) | [![ExpressionExtensionSQL.Dapper](https://img.shields.io/nuget/v/ExpressionExtensionSQL.Dapper.svg)](https://www.nuget.org/packages/ExpressionExtensionSQL.Dapper/) | [![ExpressionExtensionSQL.Dapper](https://img.shields.io/nuget/vpre/ExpressionExtensionSQL.Dapper.svg)](https://www.nuget.org/packages/ExpressionExtensionSQL.Dapper/) | [![ExpressionExtensionSQL.Dapper](https://img.shields.io/nuget/dt/ExpressionExtensionSQL.Dapper.svg)](https://www.nuget.org/packages/ExpressionExtensionSQL.Dapper/) |

Features
--------
ExpressionExtensionSQL is a [NuGet library](https://www.nuget.org/packages/ExpressionExtensionSQL) which you can add to your project to achieve lambda expression in SQL code. It allows your domain not need to understand SQL language mainly for creating filters. Very suitable for use with [SpecificationPattern](https://en.wikipedia.org/wiki/Specification_pattern).

Samples:

```
Example usage:
```
```csharp
 Expression<Func<Merchant, bool>> expression = x => x.Name == "merchant1" && x.CreatedAt>=DateTime.Now;
 var where = expression.ToSql();
 Console.Write(where.Sql);
 
```
The code return will be:
```
([Merchant].[Name] = @1) AND ([Merchant].[CreatedAt]>=@2)
```

**where.Parameters** contains a list of parameters that can be used in ADO queries.
