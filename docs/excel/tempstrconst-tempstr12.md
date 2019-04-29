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
- tempstr12-Funktion [Excel 2007], TempStrConst-Funktion [Excel 2007]
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
  
Framework-Bibliotheksfunktion, die eine temporäre **XLOPER/XLOPER12** erstellt, die eine **xltypeStr** -Zeichenfolge enthält, wobei eine mit NULL endende Quelle als Eingabe eingegeben wird. Die Funktion weist einen neuen Speicherpuffer zu und kopiert die übergebene Zeichenfolge hinein. Die Eingabezeichenfolge wird nicht geändert und wird daher als **const**deklariert.
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a>Parameter

 _str_
  
Ein Zeiger auf die NULL-terminierte Quellzeichenfolge. Im Fall von **XLOPER**s schneidet TempStrConst Zeichenfolgen ab, die länger als 255 Bytes sind. Im Fall von **XLOPER12**s schneidet TempStr12Const Zeichenfolgen ab, die länger als 32.767 Unicode-Zeichen sind.
  
## <a name="return-value"></a>Rückgabewert

Gibt eine **xltypeStr** -Zeichenfolge mit einer Kopie des übergebenen Zeichenfolgenpuffers zurück. 
  
## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass die **XLOPER** -Zeichenfolgen Framework-Funktion, **TempStr**, sich anders verhält und versucht, das erste Zeichen der angegebenen Zeichenfolge mit der Länge der nachfolgenden Zeichenfolge zu überschreiben. Dies ist nicht immer sicher: Microsoft Excel stürzt möglicherweise ab, wenn eine schreibgeschützte Zeichenfolge übergeben wird. Diese Methode zum Erstellen temporärer Zeichenfolgen ist nun zugunsten der Art und Weise veraltet, in der sowohl **TempStrConst** als auch **TempStr12** funktionieren. Daher wird das erste Zeichen der Eingabezeichenfolge als Anfang der Zeichenfolge behandelt, also nicht als Längenzeichen oder als Leerzeichen für ein Längezeichen. Sie sollten keine Zeichenfolgen mit einem Zeichen vom Typs length, die am Anfang codiert sind, als Folge der Konsequenzen nicht vorhersagen. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird die **TempStr12** -Funktion verwendet, um eine Zeichenfolge für ein Meldungsfeld zu erstellen. 
  
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

