---
title: KeyboardShortcuts control reference | Creator Kit
description: Learn about the details and properties of KeyboardShortcuts control in the Creator Kit.
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

# :::no-loc text="KeyboardShortcut"::: control

[This article is pre-release documentation and is subject to change.]

A control used to capture and act on keyboard events.

## Description

This code component registers Key Press event handlers to allow keyboard short cuts to be used inside canvas apps or custom pages. It isn't intended for use in model-driven or portal apps.

> [!NOTE]
> Component source code and more information available at the [Creator kit GitHub repository](https://github.com/microsoft/powercat-creator-kit).

## Limitations

Some keyboard shortcuts are used by Power Apps when using maker studio, and some are used by the browser. For this reason, this component won't work for all keyboard shortcuts until the user places focus inside the app.

This code component can only be used in canvas apps and custom pages.

## Key properties

| Property | Description |
| -------- | ----------- |
| `KeyConfig` | An array of strings indicating which keyboard short cuts to listen for. The string must be serialized using JSON (see below). |
| `OnKey` | The keyboard key code that was detected. |

After adding the `KeyboardShortcuts` code component to the form, configure the `KeyConfig` property with an  array of key combinations.

For example:

```json
["alt + r","alt + a","alt + d","alt + b","alt + p","alt + l","alt + t","alt + k"]
```

For more information about the keyboard combination strings, see [the KeyboardJS library](http://itsgreggreg.github.io/KeyboardJS/).

## Responding to the key press events

When a key combination is used, the `OnChange` event is raised. The `OnKey` property then holds the combination.

You could have an `OnChange` event similar to:

```powerapps-dot
If( Self.OnKey = "alt + a",
    SetFocus(txtTextbox1)
);
If( Self.OnKey = "alt + r",
    UpdateContext({ ctxResizableTextareaEvent:"SetFocus" & Text(Rand()) })
);
If( Self.OnKey = "alt + b",
    SetFocus(txtTextbox2)
);
If( Self.OnKey = "alt + k",
    UpdateContext({ ctxPickerEvent:"SetFocus" & Text(Rand()) })
);
If( Self.OnKey = "alt + d",
    UpdateContext({ ctxDropdownEvent:"SetFocus" & Text(Rand()) })
);
If( Self.OnKey = "alt + l",
    UpdateContext({ ctxTagListEvent:"SetFocus" & Text(Rand()) })
);
If( Self.OnKey = "alt + t", 
    UpdateContext({ ctxTableEvent:"SetFocusOnRow" & Text(Rand()) })
);
```

This event handler sets focus on various controls given the key combination used.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]