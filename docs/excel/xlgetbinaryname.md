---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- Xlgetbinaryname-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: d2332967e798b43a350c0733cd7398e2a921add6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790601"
---
# <a name="xlgetbinaryname"></a>xlGetBinaryName

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Verwendet, um ein Handle für das von der [Funktion "xlDefineBinaryName"](xldefinebinaryname.md)gespeicherte Daten zurückgeben. Mit einem definierten Namen für die binäre Daten werden mit der Arbeitsmappe gespeichert und namentlich jederzeit zugegriffen werden können. Weitere Informationen finden Sie unter "Binär nennen Bereich Einschränkung" unter [Bekannte Probleme bei der Entwicklung von Excel XLL](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a>Parameter

_pxRes_ (**XltypeBigData** oder **XltypeErr**)
  
Bigdata-Struktur, die angibt, dass die abgerufenen Daten oder ein Fehler ist die Daten konnten nicht abgerufen werden, oder der Name ist nicht definiert. Wenn die Funktion zurückgibt, das **Hdata** Mitglied der **XLOPER**/ **XLOPER12** enthält einen Handle für die benannten Daten.  _PxRes_ sollte in einem Aufruf von **XlFree** bei Bedarf nicht mehr freigegeben werden. 
  
_pxName_ (**XltypeStr**)
  
Eine Zeichenfolge zur Angabe der Name der Daten.
  
## <a name="remarks"></a>Hinweise

Microsoft Excel besitzt das Arbeitsspeicher-Handle in **Hdata**zurückgegeben. In Windows ist das Handle einer globalen Arbeitsspeicher Handle (von der Funktion **GlobalAlloc** zugewiesen). 
  
## <a name="see-also"></a>Siehe auch

- [xlDefineBinaryName](xldefinebinaryname.md)
- [C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

