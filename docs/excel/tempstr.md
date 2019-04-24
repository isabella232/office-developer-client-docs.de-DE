---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- TempStr-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 4ccb6f3c764371c35bac12c8c78fede54234a7d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310318"
---
# <a name="tempstr"></a>TempStr

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
VerAltete Framework-Bibliotheksfunktion, die eine temporäre **XLOPER** mit einer **xltypeStr** -Byte Zeichenfolge erstellt. Als Eingabe wird eine nullterminierte Quellzeichenfolge verwendet. Es wird versucht, das erste Zeichen der angegebenen Zeichenfolge mit der Länge der nachfolgenden Zeichenfolge zu überschreiben. Dies ist nicht immer sicher: Microsoft Excel stürzt möglicherweise ab, wenn eine schreibgeschützte Zeichenfolge übergeben wird. 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a>Parameter

 _str_
  
Ein Zeiger auf die NULL-terminierte Quellzeichenfolge. **TempStr** schneidet Zeichenfolgen ab, die länger als 255 Bytes sind. 
  
## <a name="return-value"></a>Rückgabewert

Gibt eine **xltypeStr** -Zeichenfolge zurück, die einen Zeiger auf den übergebenen Zeichenfolgenpuffer enthält. 
  
## <a name="remarks"></a>Bemerkungen

Diese Methode zum Erstellen temporärer Zeichenfolgen ist nun zugunsten der Art und Weise veraltet, in der sowohl TempStrConst als auch [TempStr12](tempstrconst-tempstr12.md) funktionieren. Diese Funktionen weisen einen neuen Speicherpuffer zu und kopieren die übergebene Zeichenfolge hinein. Die Eingabezeichenfolgen für **TempStrConst** und **TempStr12** werden nicht geändert und werden daher als **const**deklariert. Im Gegensatz dazu wird die Eingabezeichenfolge zu **TempStr** geändert und kann daher nicht als **const**deklariert werden. Das erste Zeichen der Eingabezeichenfolge wird als Platz für ein Längenzeichen behandelt und von dieser Funktion überschrieben.
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

