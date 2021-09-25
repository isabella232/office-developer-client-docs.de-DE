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
ms.localizationpriority: medium
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 44b065d7360345f3b12b47a0e8cbe957babab916
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601261"
---
# <a name="tempstrconsttempstr12"></a>TempStrConst/TempStr12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Bibliotheksfunktion, die einen temporären **XLOPER/XLOPER12** erstellt, der eine **xltypeStr-Zeichenfolge** enthält, wobei eine Mit Null beendete Quellzeichenfolge als Eingabe verwendet wird. Die Funktion weist einen neuen Speicherpuffer zu und kopiert die übergebene Zeichenfolge in ihn. Die Eingabezeichenfolge wird nicht geändert und daher als **Konstante** deklariert.
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a>Parameter

 _str_
  
Ein Zeiger auf die mit NULL beendete Quellzeichenfolge. Im Fall von **XLOPER** s werden von TempStrConst Zeichenfolgen abgeschnitten, die länger als 255 Bytes sind. Bei **XLOPER12-Zeichen** werden von TempStr12Const Zeichenfolgen abgeschnitten, die länger als 32.767 Unicode-Zeichen sind.
  
## <a name="return-value"></a>Rückgabewert

Gibt eine **xltypeStr-Zeichenfolge** zurück, die eine Kopie des übergebenen Zeichenfolgenpuffers enthält. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Beachten Sie, dass sich die **XLOPER** string Framework-Funktion **TempStr** anders verhält und versucht, das erste Zeichen der angegebenen Zeichenfolge mit der Länge der nachfolgenden Zeichenfolge zu überschreiben. Dies ist nicht immer sicher: Microsoft Excel kann abstürzt, wenn eine schreibgeschützte Zeichenfolge übergeben wird. Diese Methode zum Erstellen temporärer Zeichenfolgen ist jetzt veraltet, was die Funktionsweise von **TempStrConst** und **TempStr12** unterstützt. Daher wird das erste Zeichen der Eingabezeichenfolge als Anfang der Zeichenfolge behandelt, d. h. nicht als Längenzeichen oder als Leerzeichen für ein Längenzeichen. Sie sollten keine Zeichenfolgen übergeben, die zu Beginn ein Längenzeichen codiert haben, da die Folgen unvorhersehbar sein könnten. 
  
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

