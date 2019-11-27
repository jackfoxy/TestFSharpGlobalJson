# F# global.json behavior

1. yarn add webpack-cli@3.1.2 --dev  (one time)
2. .\build

notice project builds successfully with 3.0.100

3. rebuild solution inside Visual Studio 16.3.10

fails with

```
Error   FS0193   The module/namespace 'Encode' from compilation unit 'Thoth.Json' did not contain the 'valValLinkagePartialKey(generateEncoder)'	
```

4. change nuget Thoth.Json 3.4.1 in the paket.dependencies file to nuget Thoth.Json 3.2
5. .\\.paket\paket update Thoth.Json -g Client
6. build will now succeed in both batch and Visual Studio