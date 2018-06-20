---
title: TempMissing/TempMissing12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempMissing
- TempMissing12
keywords:
- Tempmissing-Funktion [excel 2007], TempMissing12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a6db2e1f2917ecd9361043577f4bf203b3267a5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790576"
---
# <a name="tempmissingtempmissing12"></a>TempMissing/TempMissing12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Bibliothek-Funktion, die eine temporäre **XLOPER**erstellt/ **XLOPER12** des Typs **XltypeMissing**.
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion verwendet keine Parameter.
  
## <a name="return-value"></a>R�ckgabewert

Gibt einen Zeiger auf eine **XLOPER** **XltypeMissing** / **XLOPER12**.
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird **TempMissing12** drei Fehlende Argumente für **XlcWorkspace** gefolgt von einem **booleschen** **FALSE** unterdrückt die Anzeige der Bildlaufleisten Arbeitsblatt bereitstellen. Die ersten drei Argumente entsprechen andere Workspace-Einstellungen nicht betroffen sind. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempMissingExample(void)
{
   XLOPER12 xBool;
   xBool.xltype = xltypeBool;
   xBool.val.xbool = 0;
   Excel12f(xlcWorkspace, 0, 4, TempMissing12(), TempMissing12(),
      TempMissing12(), (LPXLOPER12)&xBool);
   return 1;
}
```

## <a name="see-also"></a>Siehe auch



[Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

