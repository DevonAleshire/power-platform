---
title: AutoWidthLabel control reference | Creator Kit
description: Learn about the details and properties of AutoWidthLabel control in the Creator Kit.
author: denisem-msft
manager: devkeydet
ms.component: pa-maker
ms.topic: conceptual
ms.date: 05/16/2022
ms.subservice: guidance
ms.author: demora
ms.reviewer: tapanm
search.audienceType: 
  - maker
search.app: 
  - D365CE
  - PowerApps
  - Powerplatform
contributors:
  - tapanm-msft
  - slaouist
---

# :::no-loc text="AutoWidthLabel"::: control

[This article is pre-release documentation and is subject to change.]

A control used to display data.

:::image type="content" source="media/autowidthlabel.png" alt-text="Auto width label.":::

## Description

This code component acts similar to the standard canvas app label, but will expand dynamically in width to accommodate the text and return the new width. This functionality is currently not supported in canvas apps today.

> [!NOTE]
> Component source code and more information available at the [Creator kit GitHub repository](https://github.com/microsoft/powercat-creator-kit).

## Limitations

This code component can only be used in canvas apps and custom pages.

## Key properties

| Property | Description |
| -------- | ----------- |
| `Text` | Data displayed in the label |
| `AutoWidth` | The new width of the label based on the text |

## Best practices

See [Fluent UI Label control best practices](https://developer.microsoft.com/en-us/fluentui#/controls/web/label).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]