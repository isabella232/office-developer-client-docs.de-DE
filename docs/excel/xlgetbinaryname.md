---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- xlgetbinaryname-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6d063213e3f83451e8a072e71f0878174214f73e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412464"
---
# <a name="xlgetbinaryname"></a>xlGetBinaryName

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wird verwendet, um ein Handle für Daten zurück, die von der [xlDefineBinaryName-Funktion gespeichert wurden.](xldefinebinaryname.md) Daten mit einem definierten binären Namen werden mit der Arbeitsmappe gespeichert und können jederzeit über den Namen zugegriffen werden. Weitere Informationen finden Sie unter "Binary name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a>Parameter

_pxRes_ (**xltypeBigData** oder **xltypeErr**)
  
Die Bigdata-Struktur, die die abgerufenen Daten anfordert, oder ein Fehler ist, dass die Daten nicht abgerufen werden konnten oder der Name nicht definiert ist. Wenn die Funktion zurückgegeben wird, enthält **das hdata-Element** der **XLOPER** /  **XLOPER12** ein Handle für die benannten Daten.  _pxRes_ sollte in einem Aufruf von xlFree frei **werden,** wenn dies nicht mehr erforderlich ist. 
  
_pxName_ (**xltypeStr**)
  
Eine Zeichenfolge, die den Namen der Daten an gibt.
  
## <a name="remarks"></a>Hinweise

Microsoft Excel besitzt das in hdata zurückgegebene **Speicherhandle.** In Windows handle es sich um ein globales Speicherhandle (zugewiesen durch die **GlobalAlloc-Funktion).** 
  
## <a name="see-also"></a>Siehe auch

- [xlDefineBinaryName](xldefinebinaryname.md)
- [C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

