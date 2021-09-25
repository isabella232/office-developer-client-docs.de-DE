---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- tempstr-Funktion [excel 2007]
ms.localizationpriority: medium
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 49c4ccdd3b386fb7d573748ab81e833f34e8a0e5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576667"
---
# <a name="tempstr"></a>TempStr

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Veraltete Framework-Bibliotheksfunktion, die einen temporären **XLOPER** erstellt, der eine **XltypeStr-Bytezeichenfolge** enthält. Als Eingabe wird eine mit NULL beendete Quellzeichenfolge verwendet. Es wird versucht, das erste Zeichen der angegebenen Zeichenfolge mit der Länge der nachfolgenden Zeichenfolge zu überschreiben. Dies ist nicht immer sicher: Microsoft Excel kann abstürzt, wenn eine schreibgeschützte Zeichenfolge übergeben wird. 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a>Parameter

 _str_
  
Ein Zeiger auf die mit NULL beendete Quellzeichenfolge. **TempStr** truncates strings that are longer than 255 bytes. 
  
## <a name="return-value"></a>Rückgabewert

Gibt eine **xltypeStr-Zeichenfolge** zurück, die einen Zeiger auf den übergebenen Zeichenfolgenpuffer enthält. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Diese Methode zum Erstellen temporärer Zeichenfolgen ist jetzt veraltet, was die Funktionsweise von [TempStrConst und TempStr12](tempstrconst-tempstr12.md) unterstützt. Diese Funktionen weisen einen neuen Speicherpuffer zu und kopieren die übergebene Zeichenfolge darin. Die Eingabezeichenfolgen für **TempStrConst** und **TempStr12** werden nicht geändert und daher als **Konstante** deklariert. Im Gegensatz dazu wird die Eingabezeichenfolge in **TempStr** geändert und kann daher nicht als **Konstante** deklariert werden. Das erste Zeichen der Eingabezeichenfolge wird als Leerzeichen für ein Längenzeichen behandelt und von dieser Funktion überschrieben.
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

