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
ms.openlocfilehash: fdee0146ae2199097828e98abb96ffe43a64fc80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303885"
---
# <a name="xlfgetname"></a>xlfGetName

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt die Definition eines Namens zurück, wie er in der **Spalte bezieht sich** des Dialogfelds **Name Manager** angezeigt wird, das angezeigt wird, wenn Sie auf der Registerkarte **Formeln** im Abschnitt **definierte Namen** auf **Name Manager** klicken. Wenn die Definition Verweise enthält, werden diese als Z1S1-Verweise angegeben. Verwenden Sie **xlfGetName** , um den durch einen Namen definierten Wert zu überprüfen. Verwenden Sie [xlfGetDef](xlfgetdef.md), um den Namen abzurufen, der einer Definition entspricht.
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a>Parameter

_pxNameText_ (**xltypeStr**)
  
Kann ein auf dem Blatt definierter Name sein. ein externer Verweis auf einen Namen, der in der aktiven Arbeitsmappe definiert ist `"!Sales"`, beispielsweise; oder einen externen Verweis auf einen Namen, der für eine bestimmte geöffnete Arbeitsmappe definiert `"[Book1]SHEET1!Sales"`ist, beispielsweise.  _pxNameText_ kann auch ein ausgeblendeter Name sein. 
  
_pxInfoType_ (**xltypeBool**)
  
Gibt den Typ der Informationen an, die über den Namen zurückgegeben werden sollen. Wenn **false** oder nicht angegeben, wird die Definition zurückgegeben. Wenn **true**, gibt **true** zurück, wenn der Name nur für das Blatt definiert ist, **false** , wenn der Name für die gesamte Arbeitsmappe definiert ist. 
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

_pxRes_ (**xltypeStr**, **xltypeBool**oder **xltypeErr**)
  
Gibt in Abhängigkeit vom für _pxInfoType_übergebenen Wert die Definition des angegebenen Namens (**XltypeStr**) oder **true** oder **false** (**xltypeBool**) zurück.
  
## <a name="remarks"></a>Bemerkungen

Wenn das Kontrollkästchen **Arbeitsblatt und Inhalt gesperrter Zellen schützen** im Dialogfeld **Blatt schützen** ausgewählt wurde, um die Arbeitsmappe mit dem Namen zu schützen, gibt `#N/A` **xlfGetName** den Fehlerwert zurück. Klicken Sie im Abschnitt **Änderungen** der Registerkarte **überprüfen** auf **Blatt schützen** , um das Dialogfeld **Blatt schützen** anzuzeigen. 
  
In der folgenden Tabelle sind drei Beispiele für die Werte aufgeführt, die von einem Aufruf von **xlfGetDef** mit dem angegebenen _pxNameText_ -Argument zurückgegeben werden. 
  
|**Definition in Excel**|**_pxNameText_**|**ZurückgeGebener Wert**|
|:-----|:-----|:-----|
|Der Name Verkäufe auf einem Blatt ist als Nummer 523 definiert.  <br/> |Sales  <br/> |"= 523"  <br/> |
|Der Name Profit des aktiven Blatts ist definiert als Formel = Sales-costs.  <br/> |"! Gewinn  <br/> |"= Verkaufskosten"  <br/> |
|Die Name-Datenbank im aktiven Blatt ist als Range a1: F500 definiert.  <br/> |"! Datenbank  <br/> |"= Z1S1: R500C6"  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [xlfGetDef](xlfgetdef.md)
- [Wichtige und n�tzliche C-API XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

