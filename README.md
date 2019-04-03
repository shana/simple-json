# SimpleJson

This is a fork of SimpleJson with support for:
- Serializing structs
- (De)Serializing DateTime and DateTimeOffset with multiple ISO formats
- Extension methods ToJson and FromJson with casing choices
- Serializing only public or public and private methods and fields
- NPath (https://github.com/shana/niceio)
- Fine-grained (de)serialization control via custom serialization strategy classes or overrideable methods (see `JsonSerializationStrategy` class for an example)
- Unity (https://unity3d.com) type support by deferring to Unity's json serializer for Unity types

Small and fast JSON library for .NET 2.0+/SL4+/WP7+/Windows Store Apps/Portable Class Library and powershell.
Includes support for dynamic in .NET 4.0+/SL4+/Windows Store Apps. Also includes support for DataContract and DataMember. 

# Using SimpleJson

SimpleJson is not distributed as a compiled binary .dll file but rather as a single .cs file or a powershell module .psm1.

**Use nuget to add SimpleJson.cs file to your project.**

```powershell
Install-Package SimpleJson
```

## Supported Platforms
* .NET 2.0
* .NET 3.0
* .NET 3.5 (Client Profile and Full Profile)
* .NET 4.0 (Client Profile and Full Profile)
* .NET 4.5+
* .NET Core, .NET Standard, .NET Whatever Comes Next
* Windows 8 Store Apps
* Silverlight 4
* Silverlight 5
* Windows Phone 7.0
* Windows Phone 7.1 (Mango)
* Windows Phone 8
* Portable Class Libraries (PCL)
* Unity

**Note:** By default SimpleJson expects `System.Linq`. If you are targeting older version of .NET framework (.net < 3.0 or WP7.0) you will need to add `#define SIMPLE_JSON_NO_LINQ_EXPRESSION`.

If you want to use `[DataContract]`, `[DataMember(Name = "name")]` or `[IgnoreDataMember]` make sure to add `#define SIMPLE_JSON_DATACONTRACT`.

If you want to use `IReadOnlyCollection<T>` and `IReadOnlyList<T>` make sure to add `#define SIMPLE_JSON_READONLY_COLLECTIONS`.
