[![Utility.Result](https://img.shields.io/nuget/v/Utility.Result)](https://www.nuget.org/packages/Utility.Result)

# Result (Utility Library)

A utility library with Result type. This type provides a means of returning success or failure and an optional value. Great for avoiding throwing exceptions which are expensive.

## Installation

You can use the NUGET package named **Utility.Result** that is on nuget.org or adding this line to an **ItemGroup** in your csproj file.

```
<PackageReference Include="Utility.Result" Version="*" />
```

## Usage Examples

### Returning a successful result from a function.

```
    public Result ReturnOkResult()
    {
        return OkResult.Ok();
    }
```

### Returning a successful result and value from a function.

```
    public ObjectResult<int> ReturnIntegerResult()
    {
        ObjectResult<int> result = OkObjectResult<int>.Ok(100);
        return result;
    }
```

### Returns a successful result from a task.

```
    public Task<Result> ReturnResultForTask()
    {
        return Task.FromResult<Result>(OkResult.Ok());
    }
```

### Returns a failure from a function

```
    public Result ReturnFailure()
    {
        return ErrorResult.Fail("This function has failed because of...");
    }
```
