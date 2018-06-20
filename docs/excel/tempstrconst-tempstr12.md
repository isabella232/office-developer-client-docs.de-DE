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
- tempstr12-Funktion [excel 2007], TempStrConst-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 321c41aa87a3bfa0edc1d77ecc8fbe4b6a6a4730
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790581"
---
# <a name="tempstrconsttempstr12"></a>TempStrConst/TempStr12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Bibliothek-Funktion, die eine temporäre **XLOPER/XLOPER12** erstellt eine **XltypeStr** Zeichenfolge enthält, übernimmt eine mit Null endende Quellzeichenfolge als Eingabe. Die Funktion weist einen neuen Speicherpuffer für und kopiert die übergebene Zeichenfolge hinein. Die eingegebene Zeichenfolge wird nicht geändert und wird daher als **Konstante**deklariert.
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a>Parameter

 _Str_
  
Ein Zeiger auf die mit Null endende Quellzeichenfolge. Im Fall von **XLOPER**s schneidet TempStrConst Zeichenfolgen, die länger als 255 Byte sind. Im Fall von **XLOPER12**s schneidet TempStr12Const Zeichenfolgen, die länger als 32.767 Unicode-Zeichen sind.
  
## <a name="return-value"></a>R�ckgabewert

Gibt eine **XltypeStr** -Zeichenfolge, die eine Kopie des Puffers übergebene Zeichenfolge enthält. 
  
## <a name="remarks"></a>Hinweise

Beachten Sie, dass die Zeichenfolge **XLOPER** Framework-Funktion, **TempStr**, verhält sich anders und versucht, das erste Zeichen der angegebenen Zeichenfolge mit den nachfolgenden Zeichenfolgenlänge zu überschreiben. Dies ist es nicht immer eine sichere: Microsoft Excel schlagen fehl, wenn eine nur-Lese-Zeichenfolge übergeben. Auf diese Weise über das Erstellen der temporärer Zeichenfolgen ist durch die Möglichkeit, in denen **TempStrConst** und **TempStr12** jetzt veraltet. Aus diesem Grund wird das erste Zeichen der Eingabe Zeichenfolge als den Anfang der Zeichenfolge, d. h., nicht als ein Zeichen Länge oder als Leerzeichen für ein Zeichen Länge behandelt. Sie sollten keine Zeichenfolgen übergeben, die ein zu Beginn, codierte Länge Zeichen aufweisen wie die Folgen unvorhersehbar konnte. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird die **TempStr12** -Funktion zum Erstellen einer Zeichenfolge für ein Meldungsfeld verwendet. 
  
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

