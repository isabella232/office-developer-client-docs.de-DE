---
title: TempStrConst/TempStr12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr12
- TempStrConst
keywords:
- tempstr12-Funktion [excel 2007],TempStrConst-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d93f9de021c7ba325d9c11af2cede0245ffbbf6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407151"
---
# <a name="tempstrconsttempstr12"></a>TempStrConst/TempStr12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework library function that creates a temporary **XLOPER/XLOPER12** that contains an **xltypeStr** string, taking a null-terminated source string as input. Die Funktion weist einen neuen Speicherpuffer zu und kopiert die übergebene Zeichenfolge in diesen. Die Eingabezeichenfolge wird nicht geändert und daher als const **deklariert.**
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a>Parameter

 _str_
  
Ein Zeiger auf die mit Null beendete Quellzeichenfolge. Bei **XLOPER** s abgeschnitten TempStrConst Zeichenfolgen, die länger als 255 Byte sind. Bei **XLOPER12** s werden Zeichenfolgen, die länger als 32.767 Unicode-Zeichen sind, von TempStr12Const abgeschnitten.
  
## <a name="return-value"></a>Rückgabewert

Gibt eine **xltypeStr-Zeichenfolge** zurück, die eine Kopie des übergebenen Zeichenfolgenpuffers enthält. 
  
## <a name="remarks"></a>Hinweise

Beachten Sie, dass sich die XLOPER-Zeichenfolgenframework-Funktion **TempStr** anders verhält und versucht, das erste Zeichen der angegebenen Zeichenfolge mit der Länge der nachfolgenden Zeichenfolge zu überschreiben.  Dies ist nicht immer sicher: Microsoft Excel kann abstürzen, wenn eine schreibgeschützte Zeichenfolge übergeben wird. Diese Methode zum Erstellen temporärer Zeichenfolgen ist nun veraltet, da **tempStrConst** und **TempStr12 funktionieren.** Daher wird das erste Zeichen der Eingabezeichenfolge als Anfang der Zeichenfolge behandelt, d. h. nicht als Längenzeichen oder als Leerzeichen für ein Längenzeichen. Sie sollten keine Zeichenfolgen übergeben, deren Länge am Anfang codiert ist, da die Folgen unvorhersehbar sein können. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird die **TempStr12-Funktion** verwendet, um eine Zeichenfolge für ein Meldungsfeld zu erstellen. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempStrExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempStr12Const(L"Made it!"));
   return 1;
}
```

## <a name="see-also"></a>Siehe auch



[Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

