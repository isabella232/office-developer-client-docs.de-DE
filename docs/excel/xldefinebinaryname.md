---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- xlDefineBinaryName-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: e3e8f91b-cc31-4f09-9941-f950ae96820a
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3c7fc4f6b6fc7179c1ca84043895273b2781f8b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430252"
---
# <a name="xldefinebinaryname"></a>xlDefineBinaryName

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wird verwendet, um persistenten Speicher für ein **xltypeBigData** **XLOPER**/ -**XLOPER12**zu reservieren. Daten mit einem definierten binären Namen werden mit der Arbeitsmappe gespeichert und können jederzeit über den Namen aufgerufen werden. Weitere Informationen finden Sie unter "Beschränkung des binären Namensbereichs" in [bekannte Probleme in Excel XLL Development](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a>Parameter

 _pxName_ (**xltypeStr**)
  
Eine Zeichenfolge, die den Namen der Daten angibt. Die Zeichenfolge unterliegt denselben Benennungseinschränkungen wie definierte Namen.
  
 _pxData_ (**xltypeBigData**)
  
Eine Struktur, die die zu speichernden Daten angibt. Wenn Sie diese Funktion aufrufen, sollte das **lpbData** -Element der Struktur von **gdata** auf die Daten verweisen, für die der Name definiert wird, und das **cbData** -Element sollte die Länge der Daten in Byte enthalten. 
  
Wenn das _pxData_ -Argument nicht angegeben wird (**xltypeMissing**), wird die durch _pxName_ angegebene benannte Zuordnung gelöscht. 
  
## <a name="see-also"></a>Siehe auch



[xlGetBinaryName](xlgetbinaryname.md)


[C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Bekannte Probleme in Excel XLL-Entwicklung](known-issues-in-excel-xll-development.md)

