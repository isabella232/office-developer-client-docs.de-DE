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
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 030c4e501e8a9eb4b6ce29d7fe0e171324b50b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790615"
---
# <a name="xlfgetdef"></a>xlfGetDef

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt den Namen als Text, der für einen bestimmten Bereich, Wert oder eine Formel in einer Arbeitsmappe definiert ist. In Excel-dieser Wert wird angezeigt, in der Spalte **Name** des Dialogfelds **Namens-Manager** angezeigt wird, wenn Sie im Abschnitt **Definierte Namen** auf der Registerkarte **Formeln** verwenden **XlfGetDef** **Namens-Manager** zum Abrufen klicken Sie auf der Namen, die eine Definition entspricht. Wenn Sie die Definition eines Namens erhalten möchten, verwenden Sie [XlfGetName](xlfgetname.md).
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a>Parameter

_pxDefText_ (**XltypeStr**)
  
Kann sein Suchzeichenfolge Sie verweisen auf, einen Namen definieren können, einschließlich einen Verweis, einen Wert, ein Objekt oder eine Formel.
  
Verweise müssen wie in Z1S1-Bezugsart angegeben werden `"R3C5"`. Wenn _PxDefText_ einen Wert oder eine Formel ist, ist es nicht erforderlich, Gleichheitszeichen enthalten, das in der Spalte **Bezieht sich auf** das Dialogfeld **Namens-Manager** angezeigt wird. Wenn mehr als einen Namen für die _PxDefText_vorhanden ist, gibt **XlfGetDef** den Vornamen zurück. Wenn kein Name eines _PxDefText_entspricht, gibt **XlfGetDef** die `#NAME?` Fehlerwert. 
  
_pxDocumentText_ (**XltypeStr**)
  
Gibt das Blatt an diesem _PxDefText_ ist auf. Wenn _PxDocumentText_ ausgelassen wird, wird angenommen, dass das aktive Blatt sein. 
  
_pxTypeNum_ (**XltypeNum**)
  
Eine Zahl zwischen 1 und 3 angeben, welche Arten von Namen zurückgegeben werden.
  
|**_pxTypeNum_**|**gibt zurück**|
|:-----|:-----|
|1 (oder Auslassung)  <br/> |Normale Namen.  <br/> |
|2  <br/> |Ausgeblendete Namen.  <br/> |
|3  <br/> |Alle Namen.  <br/> |
   
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

 _pxRes_ (**XltypeStr** oder **XltypeErr**)
  
Gibt den Namen der angegebenen Rollendefinition zugeordnet.
  
## <a name="remarks"></a>Hinweise

Die folgende Tabelle enthält Beispiele für vier durch einen Aufruf von **XlfGetDef** mit den angegebenen Argumenten zurückgegebenen Werte sind. 
  
|**In Excel definierten Namen**|**_pxDefText_**|**_pxDocumentText_**|**_pxTypeNum_**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|:-----|:-----|
|Im angegebene Bereich Tabelle4 heißt Sales.  <br/> |"R2C2:R9C6"  <br/> |"Sheet4"  <br/> |\<ausgelassen\>  <br/> |"Sales"  <br/> |
|Der Wert 100 in Tabelle4 wird als Konstante definiert.  <br/> |"100"  <br/> |"Sheet4"  <br/> |\<ausgelassen\>  <br/> |"Constant"  <br/> |
|Die angegebene Formel in Tabelle4 heißt SumTotal.  <br/> |"SUM(R1C1:R10C1)"  <br/> |"Sheet4"  <br/> |\<ausgelassen\>  <br/> |"SumTotal"  <br/> |
|3 ist definiert als die ausgeblendeten Namen Leistungsindikator im aktiven Blatt.  <br/> |"3"  <br/> |\<ausgelassen\>  <br/> |2  <br/> |"Counter"  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [xlfGetName](xlfgetname.md)
- [Wichtige und n�tzliche C-API XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

