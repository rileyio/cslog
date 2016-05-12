cslog
===

### How to use:
1. Download the latest cslog.dll
2. In your project, add the DLL reference, in the project: `using cslog;`
3. Set your log file/location (if no leading path is set, it will default to the running dir)
`Logger.LogFile = "<filename>.log";`
4. There are 3 options available for logging, see Logging methods section.


### Logging methods
**Logging a standard string message**
```cs
Logger.Log(string message, ErrorLevel level = ErrorLevel.Info);
```

**Serialize an object (Make sure `[Serializable]` is set) and log (Default format = JSON)**
```cs
Object<T>(T obj, ErrorLevel level = ErrorLevel.Info);
```

**Exception**
```cs
Exception(Exception ex);
```

### License
MIT
