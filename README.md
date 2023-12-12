# Dynamics365-CrmTextParser

[![Join the chat at https://gitter.im/yagasoft/Dynamics365-CrmTextParser](https://badges.gitter.im/yagasoft/Dynamics365-CrmTextParser.svg)](https://gitter.im/yagasoft/Dynamics365-CrmTextParser?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

---

A parser that resolves many challenges that come up in the context of Dynamics 365 dynamic text.

## Features

  + Operations: +, -, *, /, ==, <=, ??, ?:, &&, || ... etc.
  + CRM queries: retrieve row, FetchXML, actions
  + Traversal: columns and relationships
  + Collection functions: sum, min, max, distinct, map, count, filter, ... etc.
  + Date functions: add days, months, ... etc.; output in a custom format ... etc.
  + String functions
    + Functions: length, sub-string, trim, pad, title case, format numbers, encode HTML ... etc.
    + Regex: functions to target part of the input text only
  + Memory: supports variables (store and load of values)

## Install

Install either [Yagasoft.Libraries.Common](https://www.nuget.org/packages/Yagasoft.Libraries.Common/) (DLL installed) or [Yagasoft.Libraries.Common.File](https://www.nuget.org/packages/Yagasoft.Libraries.Common.File/) (the parser class itself is embedded in the project itself) NuGet package, and then reference the CrmParser class.

If configuration entities are required, import the solution at [Dynamics365-YsCommonSolution](https://github.com/yagasoft/Dynamics365-YsCommonSolution).

## Guide

Check the guide in the docs folder.

## Changes
+ Check Releases page for the later changes
#### _v1.3 (2021-10-01)_
+ Added: HTML post-processor, which allows encoding/decoding text as HTML
+ Added: global options (HTML, expression switch, caching)
#### _v1.1 (2021-08-22)_
Initial commit.

---
**Copyright &copy; by Ahmed Elsawalhy ([Yagasoft](https://yagasoft.com))** -- _GPL v3 Licence_
