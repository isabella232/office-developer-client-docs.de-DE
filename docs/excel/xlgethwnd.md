---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- XlGetHwnd-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a22365d6c945aaa5995e2c519c757a1a7515655a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790618"
---
# <a name="xlgethwnd"></a>xlGetHwnd

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt den Fensterhandle des Fensters auf oberster Ebene Microsoft Excel zurück.
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Parameter

Diese Funktion hat keine Argumente.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Enthält das Handle des Fensters (**vom Typ XltypeInt**) im Feld **val.w** . 
  
## <a name="remarks"></a>Hinweise

Diese Funktion ist hilfreich für das Schreiben von Code für Windows-API.
  
Wenn Sie diese Funktion mit [Excel4](excel4-excel12.md) oder [Excel4v](excel4v-excel12v.md)aufrufen, wird die zurückgegebene XLOPER ganzzahlige Variable einer signierten 16-Bit-short int Dies ist nur die unteren 16 Bits der 32-Bit-Windows-Handle enthalten kann. Damit oberer Teil ermittelt wird, muss alle geöffneten Fenster Nachrichtensymbol eine Übereinstimmung mit den unteren Teil des Codes durchlaufen. Ab Excel 2007, die ganzzahlige Variable der **XLOPER12** ist eine signierte 32-Bit-Int und aus diesem Grund enthält das gesamte Handle, entfernen alle geöffneten Fenster durchlaufen werden müssen. 
  
### <a name="example"></a>Beispiel

Anzeigen des Codes für die [fShowDialog-Funktion](fshowdialog.md) in `SAMPLES\GENERIC\GENERIC.C`.
  
## <a name="see-also"></a>Siehe auch

- [xlGetInst](xlgetinst.md)
- [C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

