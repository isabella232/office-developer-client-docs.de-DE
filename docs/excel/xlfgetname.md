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
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 63bfc6e94950a621c2367b2d35d25e3de48b344f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790594"
---
# <a name="xlfgetname"></a>xlfGetName

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt die Definition eines Namens zurück, wie er in der Spalte **bezieht sich auf** das Dialogfeld **Namens-Manager** angezeigt, die angezeigt wird wird, wenn Sie **Namens-Manager** im Abschnitt **Definierte Namen** auf der Registerkarte **Formeln** klicken. Wenn die Definition Verweise enthält, werden sie als Z1S1-Bezügen angegeben. Verwenden Sie **XlfGetName** , überprüfen Sie den Wert durch einen Namen definiert. Verwenden Sie zum Abrufen des Namens, die eine Definition entspricht, [XlfGetDef](xlfgetdef.md).
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a>Parameter

_pxNameText_ (**XltypeStr**)
  
Ein Namen kann für das Blatt definiert werden; ein externer Verweis auf einen Namen in der aktiven Arbeitsmappe definiert `"!Sales"`; oder ein externer Verweis auf einen Namen für einen bestimmten geöffnete Arbeitsmappe, beispielsweise definierte `"[Book1]SHEET1!Sales"`.  _PxNameText_ kann auch ausgeblendeter Name sein. 
  
_pxInfoType_ (**XltypeBool**)
  
Gibt den Typ der Informationen, die über den Namen des zurückgegeben. Wenn **FALSE** oder weggelassen wird, wird die Definition zurückgegeben. Wenn **TRUE**, gibt **TRUE** zurück, wenn der Name für lediglich das Arbeitsblatt, **FALSE** definiert ist, wenn der Name für die gesamte Arbeitsmappe definiert ist. 
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

_pxRes_ (**XltypeStr**, **XltypeBool**oder **XltypeErr**)
  
Abhängig vom Wert für _PxInfoType_übergeben gibt die Definition des angegebenen Namen (**XltypeStr**) oder **TRUE** oder **FALSE** (**XltypeBool**).
  
## <a name="remarks"></a>Hinweise

Wenn das Kontrollkästchen **Arbeitsblatt und Inhalt gesperrter Zellen schützen** im Dialogfeld **Blatt schützen** ausgewählt wurde um die Arbeitsmappe mit dem Namen zu schützen, **XlfGetName** gibt die `#N/A` Fehlerwert. Um das Dialogfeld **Blatt schützen** angezeigt wird, klicken Sie auf **Blatt schützen** im Abschnitt **Änderungen** von der Registerkarte **Überprüfen** . 
  
Die folgende Tabelle enthält drei Beispiele für die Werte durch einen Aufruf von **XlfGetDef** mit dem Argument angegebenen _PxNameText_ zurückgegeben. 
  
|**Definition in Excel**|**_pxNameText_**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Den Namen Umsatz auf einem Blatt ist als die Anzahl 523 definiert.  <br/> |"Sales"  <br/> |"= 523"  <br/> |
|Der Name der Gewinn im aktiven Blatt festgelegt wie die Formel = Sales-Kosten.  <br/> |"! Gewinn"  <br/> |"Sales-Kosten ="  <br/> |
|Der Name-Datenbank auf dem aktiven Blatt ist wie der Bereich A1:F500 definiert.  <br/> |"! Datenbank"  <br/> |"R1C1:R500C6 ="  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [xlfGetDef](xlfgetdef.md)
- [Wichtige und n�tzliche C-API XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

