---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- Tempstr-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: ce9399168d5b94d10481d2d0b5b69dd2e1d1d2e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790578"
---
# <a name="tempstr"></a>TempStr

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Veraltete Framework Bibliothek-Funktion, die eine temporäre **XLOPER** mit einer **XltypeStr** Byte-Zeichenfolge erstellt. Es wird eine mit Null endende Quellzeichenfolge als Eingabe verwendet. Er versucht, das erste Zeichen der angegebenen Zeichenfolge mit den nachfolgenden Zeichenfolgenlänge zu überschreiben. Dies ist es nicht immer eine sichere: Microsoft Excel schlagen fehl, wenn eine nur-Lese-Zeichenfolge übergeben. 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a>Parameter

 _Str_
  
Ein Zeiger auf die mit Null endende Quellzeichenfolge. **TempStr** kürzt Zeichenfolgen, die länger als 255 Byte sind. 
  
## <a name="return-value"></a>R�ckgabewert

Eine **XltypeStr** Zeichenfolge enthält einen Zeiger auf den Puffer übergebene Zeichenfolge zurückgegeben. 
  
## <a name="remarks"></a>Hinweise

Auf diese Weise über das Erstellen der temporärer Zeichenfolgen ist durch die Möglichkeit, in denen sowohl [TempStrConst und TempStr12](tempstrconst-tempstr12.md) jetzt veraltet. Diese Funktionen ein neuer Speicher Puffer und kopieren Sie die übergebene Zeichenfolge hinein. Die Zeichenfolgen für **TempStrConst** und **TempStr12** nicht geändert werden und werden daher als **Konstante**deklariert. Im Gegensatz dazu die input-Zeichenfolge, die **TempStr** wird geändert und kann nicht als **Konstante**deklariert werden. Das erste Zeichen der input-Zeichenfolge wird als Speicherplatz für ein Länge Zeichen behandelt und wird durch diese Funktion überschrieben.
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

