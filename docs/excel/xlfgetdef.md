---
title: xlfGetDef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetdef
localization_priority: Normal
ms.assetid: 68f5edbd-9040-46d3-acd5-dd51ca82f6fa
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 014db553156849d84bd07e0e416f8cb3fefb4e0b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421998"
---
# <a name="xlfgetdef"></a>xlfGetDef

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt den Namen als Text zurück, der für einen bestimmten Bereich, Wert oder eine Formel in einer Arbeitsmappe definiert ist. In Excel wird dieser Wert in der Spalte **Name** des Dialogfelds **Name Manager** angezeigt, das angezeigt wird, wenn Sie auf der Registerkarte **Formeln** im Abschnitt **definierte Namen** auf **Name Manager** klicken. verwenden Sie **xlfGetDef** , um die Name, der einer Definition entspricht. Verwenden Sie [xlfGetName](xlfgetname.md), um die Definition eines Namens abzurufen.
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a>Parameter

_pxDefText_ (**xltypeStr**)
  
Kann alles sein, auf das Sie einen Namen definieren können, auf den verwiesen werden kann, einschließlich eines Verweises, eines Werts, eines Objekts oder einer Formel.
  
Verweise müssen im Z1S1-Format angegeben werden, Beispiels `"R3C5"`Weise. Wenn _pxDefText_ ein Wert oder eine Formel ist, ist es nicht erforderlich, das Gleichheitszeichen einzuschließen, das **** in der Spalte bezieht sich im Dialogfeld **Name Manager** angezeigt wird. Wenn mehrere Namen für _pxDefText_vorhanden sind, gibt **xlfGetDef** den Vornamen zurück. Wenn kein Name mit _pxDefText_überein **** stimmt, gibt `#NAME?` xlfGetDef den Fehlerwert zurück. 
  
_pxDocumentText_ (**xltypeStr**)
  
Gibt das Blatt an, in dem sich _pxDefText_ befindet. Wenn _pxDocumentText_ ausgelassen wird, wird davon ausgegangen, dass es sich um das aktive Blatt handelt. 
  
_pxTypeNum_ (**xltypeNum**)
  
Eine Zahl zwischen 1 und 3, die angibt, welche Typen von Namen zurückgegeben werden.
  
|**_pxTypeNum_**|**gibt zurück**|
|:-----|:-----|
|1 (oder Auslassung)  <br/> |Nur normale Namen.  <br/> |
|2  <br/> |Nur versteckte Namen.  <br/> |
|3  <br/> |Alle Namen.  <br/> |
   
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

 _pxRes_ (**xltypeStr** oder **xltypeErr**)
  
Gibt den Namen zurück, der der angegebenen Definition zugeordnet ist.
  
## <a name="remarks"></a>Bemerkungen

Die folgende Tabelle enthält vier Beispiele für die Werte, die von einem Aufruf von **xlfGetDef** mit den angegebenen Argumenten zurückgegeben werden. 
  
|**In Excel definierter Name**|**_pxDefText_**|**_pxDocumentText_**|**_pxTypeNum_**|**ZurückgeGebener Wert**|
|:-----|:-----|:-----|:-----|:-----|
|Der angegebene Bereich in Sheet4 heißt Sales.  <br/> |"R2C2: R9C6"  <br/> |Sheet4  <br/> |\<weggelassen\>  <br/> |Sales  <br/> |
|Der Wert 100 in Sheet4 ist als Konstante definiert.  <br/> |"100"  <br/> |Sheet4  <br/> |\<weggelassen\>  <br/> |Konstante  <br/> |
|Die angegebene Formel in Sheet4 hat den Namen SumTotal.  <br/> |"SUM (Z1S1: R10C1)"  <br/> |Sheet4  <br/> |\<weggelassen\>  <br/> |SumTotal  <br/> |
|3 wird als ausgeblendeter namens Zähler im aktiven Blatt definiert.  <br/> |3  <br/> |\<weggelassen\>  <br/> |2  <br/> |Zähler  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [xlfGetName](xlfgetname.md)
- [Wichtige und nützliche C-API-XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

