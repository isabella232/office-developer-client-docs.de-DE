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
- Tempbool-Funktion [excel 2007], TempBool12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 30874e7b918d8cd780bef60b4b02de1319f0f9ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790569"
---
# <a name="tempbooltempbool12"></a>TempBool/TempBool12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Bibliothek-Funktion, die eine temporäre **XLOPER**erstellt/ **XLOPER12** mit **booleschen Wert** **TRUE** oder **FALSE**.
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a>Parameter

 _b_ (**Int**)
  
Verwenden Sie 0 **FALSE**zurückgegeben. Verwenden Sie einen anderen Wert **TRUE**zurückgibt.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Gibt ein **XltypeBool** **Boolean** mit den logischen übergebenen Wert zurück. 
  
## <a name="example"></a>Beispiel

Im folgende Beispiel wird mithilfe die Funktion **TempBool12** die Statusleiste gelöscht. Temporärer Speicher freigegeben wird, wenn die [Excel/Excel12f](excel-excel12f.md) -Funktion aufgerufen wird. 
  
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

