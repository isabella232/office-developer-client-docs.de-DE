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
localization_priority: Normal
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4ccb6f3c764371c35bac12c8c78fede54234a7d6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418043"
---
# <a name="tempstr"></a>TempStr

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Veraltete Framework-Bibliotheksfunktion, die eine temporäre **XLOPER mit** einer **xltypeStr-Bytezeichenfolge** erstellt. Es wird eine mit Null beendete Quellzeichenfolge als Eingabe verwendet. Es wird versucht, das erste Zeichen der angegebenen Zeichenfolge mit der Länge der nachfolgenden Zeichenfolge zu überschreiben. Dies ist nicht immer eine sichere Sache: Microsoft Excel kann abstürzen, wenn eine schreibgeschützte Zeichenfolge übergeben wird. 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a>Parameter

 _str_
  
Ein Zeiger auf die mit Null beendete Quellzeichenfolge. **TempStr** kürzt Zeichenfolgen, die länger als 255 Byte sind. 
  
## <a name="return-value"></a>Rückgabewert

Gibt eine **xltypeStr-Zeichenfolge** zurück, die einen Zeiger auf den übergebenen Zeichenfolgenpuffer enthält. 
  
## <a name="remarks"></a>Hinweise

Diese Methode zum Erstellen temporärer Zeichenfolgen ist nun veraltet, da [tempStrConst und TempStr12 funktionieren.](tempstrconst-tempstr12.md) Diese Funktionen weisen einen neuen Speicherpuffer zu und kopieren die übergebene Zeichenfolge in diesen. Die Eingabezeichenfolgen **für TempStrConst** und **TempStr12** werden nicht geändert und werden daher als **const deklariert.** Im Gegensatz dazu wird die Eingabezeichenfolge zu **TempStr** geändert und kann daher nicht als const deklariert **werden.** Das erste Zeichen der Eingabezeichenfolge wird als Leerzeichen für ein Längenzeichen behandelt und von dieser Funktion überschrieben.
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

