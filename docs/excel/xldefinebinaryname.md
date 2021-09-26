---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- Xldefinebinaryname-Funktion [excel 2007]
ms.localizationpriority: medium
ms.assetid: e3e8f91b-cc31-4f09-9941-f950ae96820a
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 17a28b5fac2e2d92beb19def39174a728df1b188
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611210"
---
# <a name="xldefinebinaryname"></a>xlDefineBinaryName

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wird verwendet, um beständigen Speicher für **xltypeBigData** **XLOPER** /  **XLOPER12** zuzuweisen. Daten mit einem definierten binären Namen werden mit der Arbeitsmappe gespeichert und können jederzeit über den Namen aufgerufen werden. Weitere Informationen finden Sie unter "Einschränkung des Binärnamenbereichs" in [bekannten Problemen in Excel XLL-Entwicklung.](known-issues-in-excel-xll-development.md)
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a>Parameter

 _pxName_ (**xltypeStr**)
  
Eine Zeichenfolge, die den Namen der Daten angibt. Die Zeichenfolge unterliegt denselben Namenseinschränkungen wie definierte Namen.
  
 _pxData_ (**xltypeBigData**)
  
Bigdata-Struktur, die die zu speichernden Daten angibt. Wenn Sie diese Funktion aufrufen, sollte das **lpbData-Element** der **BigData-Struktur** auf die Daten zeigen, für die der Name definiert wird, und das **cbData-Element** sollte die Länge der Daten in Bytes enthalten. 
  
Wenn das  _Argument pxData_ nicht angegeben ist (**xltypeMissing**), wird die durch  _pxName_ angegebene benannte Zuordnung gelöscht. 
  
## <a name="see-also"></a>Siehe auch



[xlGetBinaryName](xlgetbinaryname.md)


[C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Bekannte Probleme in Excel XLL-Entwicklung](known-issues-in-excel-xll-development.md)

