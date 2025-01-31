---
title: Alert
weight: 234
description: You will find here Alert definition and its attributes details
---

---

## What is it?

`Alert` class creates a confirmation element.

Alert structure is:

| Attribute | Type                                                | Required | Definition                  |
| :-------- | :-------------------------------------------------- | :------- | :-------------------------- |
| title     | String or [**Binding**]({{< ref path="/api/context#bindings" lang="en" >}}) |          | Box alert title.            |
| message   | String or [**Binding**]({{< ref path="/api/context#bindings" lang="en" >}}) | ✓        | Box alert message.          |
| onPressOk | [**Action**]({{< ref path="/api/actions" lang="en" >}})                     |          | Confirmation button action. |
| labelOk   | String                                              |          | Confirmation button label.  |

## How to use it?

{{< tabs id="T89" >}}
{{% tab name="JSON" %}}

<!-- json-playground:alert.json
{
    "_beagleComponent_": "beagle:container",
    "children": [
      {
        "_beagleComponent_": "beagle:button",
        "text": "Alert Example",
        "onPress": [
          {
            "_beagleAction_": "beagle:alert",
            "title": "My Title",
            "message": "Alert message",
            "labelOk": "Close"
              }
            ]
          }
        ]
      }
-->

{{% playground file="alert.json" language="en" %}}
{{% /tab %}}

{{% tab name="Kotlin DSL" %}}

```kotlin
Container(
          children = listOf(
          Button(
                  text = "Alert Example",
                  onPress = listOf(
                    Alert(
                         title = "My Title",
                         message = "Alert message",
                         labelOk = "Close"
                    )
                 )
              )
           )
        )
```

{{% /tab %}}
{{< /tabs >}}
