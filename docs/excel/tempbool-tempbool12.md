---
title: TempBool/TempBool12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempBool
- TempBool12
keywords:
- tempbool function [excel 2007],TempBool12 function [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 47c86ac41c49ae1e3de9a5f065294215f95822db
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576674"
---
# <a name="tempbooltempbool12"></a>TempBool/TempBool12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Bibliotheksfunktion, die einen temporären **XLOPER** /  **XLOPER12** erstellt, der **boolesche** **TRUE** oder FALSE **enthält.**
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a>Parameter

 _b_ (**int**)
  
Verwenden Sie 0, um **FALSE** zurückzugeben; verwenden Sie einen beliebigen anderen Wert, um **TRUE** zurückzugeben.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Gibt einen **xltypeBool** **Boolean-Wert** zurück, der den übergebenen Wahrheitswert enthält. 
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird die **TempBool12-Funktion** verwendet, um die Statusleiste zu löschen. Temporärer Speicher wird freigegeben, wenn die [Excel/Excel12f-Funktion](excel-excel12f.md) aufgerufen wird. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short int WINAPI TempBoolExample(void)
{
    Excel12f(xlcMessage, 0, 1, TempBool12(0));
    return 1;
}
```

## <a name="see-also"></a>Siehe auch



[Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

