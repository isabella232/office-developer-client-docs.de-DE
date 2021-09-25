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
ms.localizationpriority: medium
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 84581705359442ce9366d1602920195c63c36375
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596792"
---
# <a name="xlgetbinaryname"></a>xlGetBinaryName

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wird verwendet, um ein Handle für Daten zurückzugeben, die von der [XlDefineBinaryName -Funktion](xldefinebinaryname.md)gespeichert werden. Daten mit einem definierten binären Namen werden mit der Arbeitsmappe gespeichert und können jederzeit mithilfe des Namens aufgerufen werden. Weitere Informationen finden Sie unter "Einschränkung des Binärnamenbereichs" in [bekannten Problemen in Excel XLL-Entwicklung.](known-issues-in-excel-xll-development.md)
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a>Parameter

_pxRes_ (**xltypeBigData** oder **xltypeErr**)
  
Bigdata-Struktur, die die abgerufenen Daten angibt, oder ein Fehler ist, dass die Daten nicht abgerufen werden konnten oder der Name nicht definiert ist. Wenn die Funktion zurückgegeben wird, enthält das **hdata-Element** von **XLOPER** /  **XLOPER12** ein Handle für die benannten Daten.  _pxRes_ sollte in einem **XlFree-Aufruf** freigegeben werden, wenn er nicht mehr erforderlich ist. 
  
_pxName_ (**xltypeStr**)
  
Eine Zeichenfolge, die den Namen der Daten angibt.
  
## <a name="remarks"></a>HinwBemerkungeneise

Microsoft Excel besitzt das in **hdata** zurückgegebene Speicherhandle. In Windows handelt es sich bei dem Handle um ein globales Speicherhandle (das von der **GlobalAlloc-Funktion** zugewiesen wird). 
  
## <a name="see-also"></a>Siehe auch

- [xlDefineBinaryName](xldefinebinaryname.md)
- [C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

