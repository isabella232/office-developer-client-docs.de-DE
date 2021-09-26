---
title: xlfGetDef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetdef
ms.localizationpriority: medium
ms.assetid: 68f5edbd-9040-46d3-acd5-dd51ca82f6fa
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c6f3f8de3fc3a4fcc3c6ade8d3378e578f4fb193
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611196"
---
# <a name="xlfgetdef"></a>xlfGetDef

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt den Namen als Text zurück, der für einen bestimmten Bereich, Wert oder eine bestimmte Formel in einer Arbeitsmappe definiert ist. In Excel wird dieser Wert in der Spalte Name des Dialogfelds **Name** Manager angezeigt, das angezeigt wird, wenn Sie im Abschnitt **Definierte Namen** auf der Registerkarte  **Formeln** auf den **Namen-Manager** klicken. Verwenden Sie **xlfGetDef,** um den Namen abzurufen, der einer Definition entspricht. Verwenden Sie [xlfGetName,](xlfgetname.md)um die Definition eines Namens abzurufen.
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a>Parameter

_pxDefText_ (**xltypeStr**)
  
Dies kann alles sein, auf das Sie einen Namen verweisen können, einschließlich eines Verweises, eines Werts, eines Objekts oder einer Formel.
  
Verweise müssen im R1C1-Format angegeben werden,  `"R3C5"` z. B. . Wenn  _pxDefText_ ein Wert oder eine Formel ist, ist es nicht erforderlich, das Gleichheitszeichen einzuschließen, das in der Spalte **Verweist auf** im Dialogfeld **Name** Manager angezeigt wird. Wenn für  _pxDefText_ mehrere Namen vorhanden sind, gibt **xlfGetDef** den Vornamen zurück. Wenn kein Name  _mit pxDefText_ übereinstimmt, gibt **xlfGetDef** den  `#NAME?` Fehlerwert zurück. 
  
_pxDocumentText_ (**xltypeStr**)
  
Gibt das Blatt an, auf dem  _sich pxDefText_ befindet. Wenn  _pxDocumentText_ ausgelassen wird, wird davon ausgegangen, dass es sich um das aktive Blatt handelt. 
  
_pxTypeNum_ (**xltypeNum**)
  
Eine Zahl zwischen 1 und 3, die angibt, welche Typen von Namen zurückgegeben werden.
  
|**_pxTypeNum_**|**gibt zurück**|
|:-----|:-----|
|1 (oder Auslassung)  <br/> |Nur normale Namen.  <br/> |
|2  <br/> |Nur ausgeblendete Namen.  <br/> |
|3  <br/> |Alle Namen.  <br/> |
   
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

 _pxRes_ (**xltypeStr** oder **xltypeErr**)
  
Gibt den Namen zurück, der der angegebenen Definition zugeordnet ist.
  
## <a name="remarks"></a>Bemerkungen

In der folgenden Tabelle sind vier Beispiele für die Werte aufgeführt, die von einem Aufruf von **xlfGetDef** mit den angegebenen Argumenten zurückgegeben werden. 
  
|**In Excel definierter Name**|**_pxDefText_**|**_pxDocumentText_**|**_pxTypeNum_**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|:-----|:-----|
|Der angegebene Bereich in Sheet4 heißt "Sales".  <br/> |"R2C2:R9C6"  <br/> |"Sheet4"  <br/> |\<omitted\>  <br/> |"Vertrieb"  <br/> |
|Der Wert 100 in Sheet4 ist als Konstante definiert.  <br/> |"100"  <br/> |"Sheet4"  <br/> |\<omitted\>  <br/> |"Konstante"  <br/> |
|Die angegebene Formel in Sheet4 heißt "SumTotal".  <br/> |"SUM(R1C1:R10C1)"  <br/> |"Sheet4"  <br/> |\<omitted\>  <br/> |"SumTotal"  <br/> |
|3 ist als ausgeblendeter Namenszähler im aktiven Blatt definiert.  <br/> |"3"  <br/> |\<omitted\>  <br/> |2  <br/> |"Counter"  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [xlfGetName](xlfgetname.md)
- [Wichtige und nützliche C-API-XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

