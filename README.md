# Dynamics365-CrmTextParser

[![Join the chat at https://gitter.im/yagasoft/Dynamics365-CrmTextParser](https://badges.gitter.im/yagasoft/Dynamics365-CrmTextParser.svg)](https://gitter.im/yagasoft/Dynamics365-CrmTextParser?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

### Version: 1.1
---

A parser that resolves many challenges that come up in the context of Dynamics 365 dynamic text.

A rework of the YS Common 'AttributeParser' ([DynamicsCrm-Libraries](https://github.com/yagasoft/DynamicsCrm-Libraries)) to avail much more powerful text features.

### Features

  + Unique construct that guarantees it won't occur naturally in any text, which increases the solution's robustness
  + Supports parsing expressions; e.g., x>1&&y<3, which can also be used with column values
  + Constructs:
    + Column: retrieve a column value from CRM
    + Preload: performance improvement by caching from CRM
    + Reference: loads related rows from CRM, or executes a FetchXML or Action
    + Info: displays information related to the current row
    + Template: defines a block of text for reuse to be referenced later in the text
    + Discard: performs an operation and then discards the result
    + Replace: replace a pattern in the text
    + Dictionary: retrieve a value from the key-value table from CRM
    + Common config: retrieve a column value from the Common Configuration table
  + Preprocessors:
    + Store: stores the value so far in the pipeline in memory
    + Read: restores the value from memory
    + Distinct: keeps only unique rows retrieved by the reference-construct
    + Order: orders the rows retrieved by the reference-construct
  + Post-processors:
    + Store and Read
    + String ops
      + Length, Index, Substring, Trim, Pad, Truncate, Upper, Lower, Sentence case, Title case, Extract text, Replace, Split
    + Format:
      + Date and Number
    + Collection:
      + Count, First, Last, Nth, Top, Distinct, Order, Where, Filter

### Install

Import solution found at .
The [Dynamics365-YsCommonSolution](https://github.com/yagasoft/Dynamics365-YsCommonSolution) solution is required for the configuration entities. It can be skipped if the dictionary or configuration constructs are not needed.

Install either [Yagasoft.Libraries.Common](https://www.nuget.org/packages/Yagasoft.Libraries.Common/) (DLL installed) or [Yagasoft.Libraries.Common.File](https://www.nuget.org/packages/Yagasoft.Libraries.Common.File/) (the parser class itself is embedded in the project itself) NuGet package, and then reference the CrmParser class.

### Guide

Check the guide in the docs folder.

## Changes

#### _v1.1 (2021-08-22)_
Initial commit.

---
**Copyright &copy; by Ahmed Elsawalhy ([Yagasoft](https://yagasoft.com))** -- _GPL v3 Licence_
