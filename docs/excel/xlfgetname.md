---
title: xlfGetName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetname
localization_priority: Normal
ms.assetid: 65780435-aaa2-47af-b44f-07be7aa769ee
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fdee0146ae2199097828e98abb96ffe43a64fc80
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436629"
---
# <a name="xlfgetname"></a>xlfGetName

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt die Definition eines Namens zurück, wie sie in der Spalte **Verweist** auf des Dialogfelds  **Name Manager** angezeigt wird, die angezeigt wird, wenn Sie im Abschnitt Definierte Namen auf der Registerkarte **Formeln** auf **Name Manager** klicken. Wenn die Definition Verweise enthält, werden sie als R1C1-Verweise angegeben. Verwenden **Sie xlfGetName,** um den durch einen Namen definierten Wert zu überprüfen. Verwenden Sie [xlfGetDef,](xlfgetdef.md)um den Namen zu erhalten, der einer Definition entspricht.
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a>Parameter

_pxNameText_ (**xltypeStr**)
  
Kann ein auf dem Blatt definierter Name sein. ein externer Verweis auf einen namen, der in der aktiven Arbeitsmappe definiert ist, z. B. ; oder ein externer Verweis auf einen Namen, der für eine bestimmte geöffnete Arbeitsmappe definiert ist, z. B.  `"!Sales"`  `"[Book1]SHEET1!Sales"` .  _pxNameText_ kann auch ein ausgeblendeter Name sein. 
  
_pxInfoType_ (**xltypeBool**)
  
Gibt den Typ der Informationen an, die über den Namen zurückgeben werden. Wenn **FALSE** oder nicht angegeben wird, wird die Definition zurückgegeben. Wenn **TRUE**, gibt **TRUE zurück,** wenn der Name nur für das Blatt definiert ist, **FALSE,** wenn der Name für die gesamte Arbeitsmappe definiert ist. 
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

_pxRes_ (**xltypeStr**, **xltypeBool** oder **xltypeErr**)
  
Gibt abhängig vom für  _pxInfoType_ übergebenen Wert die Definition des angegebenen Namens (**xltypeStr**) oder **TRUE** oder **FALSE** (**xltypeBool**) zurück.
  
## <a name="remarks"></a>Hinweise

Wenn das **Kontrollkästchen Arbeitsblatt und** Inhalt gesperrter  Zellen schützen im Dialogfeld Blatt schützen aktiviert wurde, um die Arbeitsmappe zu schützen, die den Namen enthält, gibt **xlfGetName** den `#N/A` Fehlerwert zurück. Klicken Sie im Abschnitt Änderungen  **auf** der  Registerkarte Überprüfen auf Blatt schützen, um das Dialogfeld Blatt schützen **anzuzeigen.** 
  
In der folgenden Tabelle sind drei Beispiele für die Werte aufgeführt, die von einem Aufruf von **xlfGetDef** mit dem angegebenen  _Argument pxNameText zurückgegeben_ werden. 
  
|**Definition in Excel**|**_pxNameText_**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Der Name Sales auf einem Blatt wird als die Zahl 523 definiert.  <br/> |"Sales"  <br/> |"=523"  <br/> |
|Der Name Profit im aktiven Blatt wird als Formel =Sales-Costs definiert.  <br/> |"! Profit"  <br/> |"=Sales-Costs"  <br/> |
|Der Name Database auf dem aktiven Blatt wird als Bereich A1:F500 definiert.  <br/> |"! Database"  <br/> |"=R1C1:R500C6"  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [xlfGetDef](xlfgetdef.md)
- [Wichtige und nützliche C-API-XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

