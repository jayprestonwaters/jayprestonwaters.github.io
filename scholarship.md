---
layout: default
title: Scholarship Project
permalink: /scholarship/
---

# Scholarship Application Update

Using the commands below which install and run the [.NET Upgrade Assistant](https://dotnet.microsoft.com/en-us/platform/upgrade-assistant), I was able to rapidly upgrade the project from .NET 2.0 to .NET 6.0, allowing my team to begin working and adding more necessary changes in the most up-to-date version of the .NET Entity Framework.

```
dotnet tool install -g upgrade-assistant

upgrade-assistant analyze <Path to csproj or sln to upgrade>
```
