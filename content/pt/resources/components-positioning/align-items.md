---
title: Align Items
weight: 64
description: >-
  Nesta seção, você encontra mais informações sobre a propriedade Align Items
  utilizada para posicionar elementos em tela.
---

---

## Align Items

Essa propriedade define como os itens são distribuídos ao longo do eixo transversal do container e tem os seguintes atributos: **`flex-start, flex-end, center, baseline e stretch.`**

### **Stretch**

Os itens serão expandidos para preencher toda a dimensão do eixo transversal \(altura ou largura\) da tela:

![](https://lh3.googleusercontent.com/fk8LZ2eCe2pOmsuFaGdG4yjPJ06MxNKiVjQXwPBdvGkyJi5vKyeI_eU9iwTZiMMoHI6oXkiEG9NZDcd78DSfMgyEquxvEwbrJxMvKZeHXbmDZ0bg5mvYTFgzJ2ACHTp-wuEEvbQw)

{{< tabs id="T32" >}}
{{% tab name="Kotlin" %}}

```kotlin
 private fun screen() :Widget{
        return Container(
            children = listOf(
                createText(backgroundColor = "#142850", text = "texto 1"),
                createText(backgroundColor = "#dd7631", text = "texto 2"),
                createText(backgroundColor = "#649d66", text = "texto 3")
            )
        ).setFlex {
              grow = 1.0
              justifyContent = JustifyContent.SPACE_EVENLY
              alignItems = AlignItems.STRETCH
          }
    }
```

{{% /tab %}}

{{% tab name="Swift" %}}

```swift
private func screen() -> Screen {
        return
            Screen(
                navigationBar: NavigationBar(title: "Flex"),
                child:
                Container(children: [
                    createText(backgroundColor: "#142850",text: "1"),
                    createText(backgroundColor: "#dd7631",text: "2"),
                    createText(backgroundColor: "#649d66",text: "3"),
                    ],widgetProperties: WidgetProperties(
                        flex: Flex()
                            .grow(1)
                            .justifyContent(.spaceEvenly)
                            .alignItems(.stretch)
                        )
                )
        )
    }
```

{{% /tab %}}
{{< /tabs >}}

### **Flex Start**

Os itens são deslocadas para o início do eixo transversal:

![](https://lh3.googleusercontent.com/hc87ybAOzlA0XmhJtLHLFC3gLn9ZgSBlNJ3AXcUUp7rQOU7BPz4-JRQWafg7V6sc8ACL93B9qTyxjDKcIkv5F0ZQZ-lxYlTa-Fw-eH2-Ca7Ny4ng_DM--mppkPLciRrvMcG_QdY9)

{{< tabs id="T33" >}}
{{% tab name="Kotlin" %}}

```kotlin
 private fun screen() :Widget{
        return Container(
            children = listOf(
                createText(backgroundText = "#142850", text = "1")
                      .setStyle {
                                size = Size.box(width = 300, height = 100)
                      },
                  createText(backgroundText = "#dd7631", text = "2")
                      .setStyle {
                          size = Size.box(width = 200, height = 100)
                      },
                  createText(backgroundText = "#649d66", text = "3")
                      .setStyle {
                          size = Size.box(width = 150, height = 100)
                      }
              )
          ).setFlex {
              grow = 1.0
              justifyContent = JustifyContent.SPACE_EVENLY
              alignItems = AlignItems.FLEX_START
          }
    }
```

{{% /tab %}}

{{% tab name="Swift" %}}

```swift
private func screen() -> Screen {
        return
            Screen(
                navigationBar: NavigationBar(title: "Flex"),
                child:
                Container(children: [
                    createText(backgroundColor: "#142850",text: "1").applyFlex(
                        Flex().size(Size().width(300).height(100))),
                    createText(backgroundColor: "#dd7631",text: "2").applyFlex(
                        Flex().size(Size().width(200).height(100))),
                    createText(backgroundColor: "#649d66",text: "3").applyFlex(
                        Flex().size(Size().width(150).height(100))),
                    ],widgetProperties: WidgetProperties(
                        flex: Flex()
                            .grow(1)
                            .justifyContent(.spaceEvenly)
                            .alignItems(.flexStart)
                        )
                )
        )
    }
```

{{% /tab %}}
{{< /tabs >}}

### **Flex End**

Os itens são deslocadas para o final do eixo transversal:

![](https://lh5.googleusercontent.com/Nhe7LKmP1-r_bbEn0iyvVRjIWfHfuJ6m8S5ITDrCaXM3JR05eSNYQndKox3FndB_skkRaAuJJVCpU9gYkyWCm4cUlLKTn_jaY8bWWmprYkB6_fYvaOourOJqT_bgUQflkSCZLZqK)

{{< tabs id="T34" >}}
{{% tab name="Kotlin" %}}

```kotlin
 private fun screen() :Widget{
        return Container(
            children = listOf(
                createText(backgroundText = "#142850", text = "1")
                      .setStyle {
                                size = Size.box(width = 300, height = 100)
                      },
                  createText(backgroundText = "#dd7631", text = "2")
                      .setStyle {
                          size = Size.box(width = 200, height = 100)
                      },
                  createText(backgroundText = "#649d66", text = "3")
                      .setStyle {
                          size = Size.box(width = 150, height = 100)
                      }
              )
          ).setFlex {
              grow = 1.0
              justifyContent = JustifyContent.SPACE_EVENLY
              alignItems = AlignItems.FLEX_END
          }
    }
```

{{% /tab %}}

{{% tab name="Swift" %}}

```swift
private func screen() -> Screen {
        return
            Screen(
                navigationBar: NavigationBar(title: "Flex"),
                child:
                Container(children: [
                    createText(backgroundColor: "#142850",text: "1").applyFlex(
                        Flex().size(Size().width(300).height(100))),
                    createText(backgroundColor: "#dd7631",text: "2").applyFlex(
                        Flex().size(Size().width(200).height(100))),
                    createText(backgroundColor: "#649d66",text: "3").applyFlex(
                        Flex().size(Size().width(150).height(100))),
                     ],widgetProperties: WidgetProperties(
                         flex: Flex()
                            .grow(1)
                            .justifyContent(.spaceEvenly)
                            .alignItems(.flexEnd)
                        )
                )
        )
    }
```

{{% /tab %}}
{{< /tabs >}}

### **Center**

Os itens são centralizados no eixo transversal:

![](https://lh5.googleusercontent.com/ruy-mtlJQlJ9eCag6xAN5C_wOm3Bh0x4UgcHGQKX642J20IBdS49ZFlDbbVgIZGfzFS8NELAC3D1ebU73hThf5E6fYw5KLIJ4BHYl0ouTuph0TepM9m4_oHQy29CFf94-aoolfc1)

{{< tabs id="T35" >}}
{{% tab name="Kotlin" %}}

```kotlin
 private fun screen() :Widget{
        return Container(
            children = listOf(
                createText(backgroundText = "#142850", text = "1")
                      .setStyle {
                                size = Size.box(width = 300, height = 100)
                      },
                  createText(backgroundText = "#dd7631", text = "2")
                      .setStyle {
                          size = Size.box(width = 200, height = 100)
                      },
                  createText(backgroundText = "#649d66", text = "3")
                      .setStyle {
                          size = Size.box(width = 150, height = 100)
                      }
              )
          ).setFlex {
              grow = 1.0
              justifyContent = JustifyContent.SPACE_EVENLY
              alignItems = AlignItems.CENTER
          }
    }
```

{{% /tab %}}

{{% tab name="Swift" %}}

```swift
 private func screen() -> Screen {
        return
            Screen(
                navigationBar: NavigationBar(title: "Flex"),
                child:
                Container(children: [
                    createText(backgroundColor: "#142850",text: "1").applyFlex(
                        Flex().size(Size().width(300).height(100))),
                    createText(backgroundColor: "#dd7631",text: "2").applyFlex(
                        Flex().size(Size().width(200).height(100))),
                    createText(backgroundColor: "#649d66",text: "3").applyFlex(
                        Flex().size(Size().width(150).height(100))),
                    ],widgetProperties: WidgetProperties(
                        flex: Flex()
                            .grow(1)
                            .justifyContent(.spaceEvenly)
                            .alignItems(.center)
                        )
                )
        )
    }
```

{{% /tab %}}
{{< /tabs >}}

### **Baseline**

Os itens são alinhados a partir da base da primeira linha de texto de cada um:

![](/shared/captura-de-tela-2020-06-04-a-s-10.55.47.png)

{{< tabs id="T36" >}}
{{% tab name="Kotlin" %}}

```kotlin
 private fun screen() :Widget{
        return Container(
            children = listOf(
                createText(backgroundText = "#142850", text = "1")
                      .setStyle {
                                size = Size.box(width = 300, height = 100)
                      },
                  createText(backgroundText = "#dd7631", text = "2")
                      .setStyle {
                          size = Size.box(width = 200, height = 100)
                      },
                  createText(backgroundText = "#649d66", text = "3")
                      .setStyle {
                          size = Size.box(width = 150, height = 100)
                      }
              )
          ).setFlex {
              grow = 1.0
              justifyContent = JustifyContent.SPACE_EVENLY
              alignItems = AlignItems.BASELINE
          }
    }
```

{{% /tab %}}

{{% tab name="Swift" %}}

```swift
 private func screen() -> Screen {
        return
            Screen(
                navigationBar: NavigationBar(title: "Flex"),
                child:
                Container(children: [
                    createText(backgroundColor: "#142850",text: "1").applyFlex(
                        Flex().size(Size().width(70).height(100))),
                    createText(backgroundColor: "#dd7631",text: "2").applyFlex(
                        Flex().size(Size().width(40).height(100))),
                    createText(backgroundColor: "#649d66",text: "3").applyFlex(
                        Flex().size(Size().width(100).height(100))),
                    ],widgetProperties: WidgetProperties(
                        flex: Flex()
                            .flexDirection(.row)
                            .grow(1)
                            .justifyContent(.spaceEvenly)
                            .alignItems(.baseline)
                        )
                )
        )
    }
```

{{% /tab %}}
{{< /tabs >}}

{{% alert color="info" %}}
Para saber mais sobre o Align Items, acesse [**a documentação no Yoga Layout.**](https://yogalayout.com/pt/align-items/)
{{% /alert %}}
