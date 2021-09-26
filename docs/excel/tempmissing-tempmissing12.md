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
- tempmissing function [excel 2007],TempMissing12 function [Excel 2007]
ms.localizationpriority: medium
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2ef271941e7ae594bbb0baa88e7a7e197966d2a5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611231"
---
# <a name="tempmissingtempmissing12"></a>TempMissing/TempMissing12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Bibliotheksfunktion, die eine temporäre **XLOPER** /  **XLOPER12** vom Typ **xltypeMissing** erstellt.
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion verwendet keine Parameter.
  
## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf eine **xltypeMissing** **XLOPER** /  **XLOPER12** zurück.
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird **TempMissing12** verwendet, um drei fehlende Argumente für **xlcWorkspace** bereitzustellen, gefolgt von einem **booleschen** **FALSE-Wert,** um die Anzeige von Bildlaufleisten des Arbeitsblatts zu unterdrücken. Die ersten drei Argumente entsprechen anderen Arbeitsbereichseinstellungen, die nicht betroffen sind. 
  
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

