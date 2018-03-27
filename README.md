# Repro steps

1. Open Solution in VS
2. Right-click "NewHotness.Web.csproj" > Edit csproj
3. Delete lines 9-11 and 21-23 (the `None` and `TypeScriptCompile` Items for `ScriptyGoodness.ts`)

Expected behavior: No changes, the files stay removed

Actual behavior: After a few seconds, the lines are re-added to the project.

This doesn't repro in a standard .NET Core project, only a Web one. Note the presence of `TypeScriptCompileBlocked` property which is expected to disable TypeScript compilation for this project.

Video: https://gfycat.com/ThunderousYoungHake
