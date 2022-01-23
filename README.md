# Interview Check (C#)
C# project for verifying interview setup

For more information about our interview setup, please refer to the following documentation:
https://github.com/sourceallies/interviews/blob/main/docs/interview-environment.md

### Requirements
 - docker
 - vscode

### Open in dev container
1. Clone this repository
2. Open the directory in VS Code
3. Click the "Open a Remote Window" icon on the bottom-left corner of VS Code
4. Select "Reopen in Container"

## The Problem
There are two failing tests in this project. The tests can be run as follows:

```
$ dotnet test Check.Tests/Check.Tests.csproj
```

## Acceptance Criteria
Make the tests pass. Only update code in the `Generator` class.

When you run the application, you should see `Hello World` printed to the console. Run the application as follows:

```
$ dotnet run -p Check/Check.csproj
```

## Future Enhancements
Update the application so that it receives the name and greeting via command line args.
