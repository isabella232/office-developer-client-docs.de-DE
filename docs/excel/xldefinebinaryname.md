---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- XlDefineBinaryName-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: e3e8f91b-cc31-4f09-9941-f950ae96820a
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 14515cc262ea398a9f200c0de3a1f6b64c758b3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790585"
---
# <a name="xldefinebinaryname"></a>xlDefineBinaryName

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Verwendet, um ein beständiger Speicher für eine **XltypeBigData** **XLOPER**verteilen/ **XLOPER12**. Mit einem definierten Namen für die binäre Daten werden mit der Arbeitsmappe gespeichert und namentlich jederzeit zugegriffen werden können. Weitere Informationen finden Sie unter "Binary Namen Bereich Einschränkung" unter [Bekannte Probleme bei der Entwicklung von Excel XLL](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a>Parameter

 _pxName_ (**XltypeStr**)
  
Eine Zeichenfolge zur Angabe der Name der Daten. Die Zeichenfolge ist, gelten die gleichen Einschränkungen wie definierte Namen benennen.
  
 _pxData_ (**XltypeBigData**)
  
Bigdata-Struktur, die die zu speichernden Daten angibt. Wenn Sie diese Funktion aufrufen, sollte das **LpbData** Mitglied der **Bigdata** -Struktur zeigen Sie auf die Daten für die der Namen definiert wird, und der **CbData** Member sollte die Länge der Daten in Bytes enthalten. 
  
Wenn das Argument _PxData_ nicht angegebenen (**XltypeMissing**) ist, wird die benannte Zuweisung von _PxName_ angegebenen gelöscht. 
  
## <a name="see-also"></a>Siehe auch



[xlGetBinaryName](xlgetbinaryname.md)


[C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Bekannte Probleme in Excel XLL-Entwicklung](known-issues-in-excel-xll-development.md)

