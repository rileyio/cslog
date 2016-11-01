cslog
===
[![AppVeyor branch](https://img.shields.io/appveyor/ci/TheJaydox/cslog/master.svg?style=flat-square)](https://ci.appveyor.com/project/TheJaydox/cslog)
[![NuGet](https://img.shields.io/nuget/v/cslog.svg?style=flat-square)](https://www.nuget.org/packages/cslog/1.0.0)

NuGet> `Install-Package cslog`

## How to use:
1. Download/Install
2. In your project, add the reference, in the project: `using cslog;`
3. Set your log file/location (if no leading path is set, it will default to the running dir)
`Logger.LogFile = "<filename>.log";`
4. There are 3 options available for logging, see Logging methods section.


## Logging methods
**Logging a standard string message**
```cs
Logger.Log(string message, ErrorLevel level = ErrorLevel.Info);
```

**Serialize an object (Make sure `[Serializable]` is set) and log (Default format = JSON)**
```cs
Logger.Object<T>(T obj, ErrorLevel level = ErrorLevel.Info);
```

**Exception**
```cs
Logger.Exception(Exception ex);
```

## License
MIT
