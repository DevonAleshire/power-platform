---
title: ResizableTextArea control reference | Creator Kit
description: Learn about the details and properties of ResizableTextArea control in the Creator Kit.
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
# :::no-loc text="ResizableTextArea"::: control

[This article is pre-release documentation and is subject to change.]

A component for user input.

:::image type="content" source="media/resizable-textarea.png" alt-text="Resizable text area control.":::

## Description

Text areas give people a way to enter and edit text. They're used in forms, modal dialogs, tables, and other surfaces where text input is required.

This component allows the user to resize the text area for convenience.

> [!NOTE]
> Component source code and more information available at the [Creator kit GitHub repository](https://github.com/microsoft/powercat-creator-kit).

## Limitations

This code component can only be used in canvas apps, custom pages and model-driven apps.

## Key properties

| Property | Description |
| -------- | ----------- |
| `Text` | Text value currently populating the control |
| `Default` | Initial text value of the control |
| `Default height` | Initial height of the control |
| `Default width` | Initial width of the control |
| `Allow resize` | Determines if resize is available and has options for direction (horizontal, vertical) |

## Additional properties

| Property | Description |
| -------- | ----------- |
| `Resized height` | The current value of the control |
| `Resized width` | The current width of the control |
| `Min height` | Min height the user is allowed to resize |
| `Max height` | Max height the user is allowed to resize |
| `Min width` | Min width the user is allowed to resize |
| `Max width` | Max width the user is allowed to resize |
| `Left padding adjustment` | Compensates for padding on the right |

Other properties are the same as the standard [text input control](/power-apps/maker/canvas-apps/controls/control-text-input).

## Best practices

See [Fluent UI text field control best practices](https://developer.microsoft.com/fluentui#/controls/web/textfield).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]