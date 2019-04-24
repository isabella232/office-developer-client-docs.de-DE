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
- tempbool-Funktion [Excel 2007], TempBool12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: c8c917f0004fe091413ea670f1cc562f1d701fa0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310353"
---
# <a name="tempbooltempbool12"></a>TempBool/TempBool12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Bibliotheksfunktion, die ein temporäres **XLOPER**/ **XLOPER12** mit dem booleschen **Wert** **true** oder **false**erstellt.
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a>Parameter

 _b_ (**int**)
  
Verwenden Sie 0, um **false**zurückzugeben; Verwenden Sie einen anderen Wert, um **true**zurückzugeben.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Gibt einen **xltypeBool** **** -booleschen Wert zurück, der den in übergebenen Logical value enthält. 
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird die **TempBool12** -Funktion verwendet, um die Statusleiste zu löschen. Temporärer Arbeitsspeicher wird freigegeben, wenn die [Excel/Excel12f-](excel-excel12f.md) Funktion aufgerufen wird. 
  
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

