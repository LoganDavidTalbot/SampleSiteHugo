---
title: Example
weight: 2
prev: /docs/getting-started
#next: /docs/
sidebar:
  open: true
---

## Example

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

{{% steps %}}

### Step 1

This is the first step.

### Step 2

This is the second step.

{{% /steps %}}

{{< tabs items="JSON,YAML,TOML" >}}

  {{< tab >}}**JSON**: JavaScript Object Notation (JSON) is a standard text-based format for representing structured data based on JavaScript object syntax.{{< /tab >}}
  {{< tab >}}**YAML**: YAML is a human-readable data serialization language.{{< /tab >}}
  {{< tab >}}**TOML**: TOML aims to be a minimal configuration file format that's easy to read due to obvious semantics.{{< /tab >}}

{{< /tabs >}}

{{< tabs items="JSON,YAML,TOML" >}}

  {{< tab >}}
  ```json
  { "hello": "world" }
  ```
  {{< /tab >}}

  ... add other tabs similarly

{{< /tabs >}}


```c#  {filename="Example.cs",linenos=table,linenostart=42, hl_lines=[2,4]}

public class Example
{
    public string Name { get; set; }
}
```