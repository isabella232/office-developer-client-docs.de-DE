---
title: xlfGetName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetname
ms.localizationpriority: medium
ms.assetid: 65780435-aaa2-47af-b44f-07be7aa769ee
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 63c883c480f9db4f0680f368fcbbe1f201bfd0b0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621325"
---
# <a name="xlfgetname"></a>xlfGetName

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt die Definition eines Namens zurück, wie sie in der Spalte **Verweisen** auf des Dialogfelds **Name-Manager** angezeigt wird, das angezeigt wird, wenn Sie auf der Registerkarte **Formeln** im Abschnitt **Definierte** Namen auf den **Namen-Manager** klicken. Wenn die Definition Verweise enthält, werden sie als R1C1-Bezugsart angegeben. Verwenden Sie **xlfGetName,** um den durch einen Namen definierten Wert zu überprüfen. Verwenden Sie [xlfGetDef,](xlfgetdef.md)um den Namen abzurufen, der einer Definition entspricht.
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a>Parameter

_pxNameText_ (**xltypeStr**)
  
Dies kann ein name sein, der auf dem Blatt definiert ist. ein externer Verweis auf einen in der aktiven Arbeitsmappe definierten Namen, z. B. ; oder ein externer Verweis auf einen Namen, der  `"!Sales"` in einer bestimmten geöffneten Arbeitsmappe definiert ist, z.  `"[Book1]SHEET1!Sales"` B. .  _pxNameText_ kann auch ein ausgeblendeter Name sein. 
  
_pxInfoType_ (**xltypeBool**)
  
Gibt den Typ der Informationen an, die zum Namen zurückgegeben werden sollen. Wenn **FALSE** oder nicht angegeben, wird die Definition zurückgegeben. Wenn **TRUE**, **gibt TRUE** zurück, wenn der Name nur für das Blatt definiert ist, **FALSE,** wenn der Name für die gesamte Arbeitsmappe definiert ist. 
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

_pxRes_ (**xltypeStr**, **xltypeBool** oder **xltypeErr**)
  
Gibt abhängig vom für  _pxInfoType_ übergebenen Wert die Definition des angegebenen Namens (**xltypeStr**) oder **TRUE** oder **FALSE** (**xltypeBool**) zurück.
  
## <a name="remarks"></a>Bemerkungen

Wenn das **Kontrollkästchen "Arbeitsblatt schützen" und der Inhalt gesperrter Zellen** im Dialogfeld **"Blatt** schützen" aktiviert wurde, um die Arbeitsmappe zu schützen, die den Namen enthält, gibt **xlfGetName** den  `#N/A` Fehlerwert zurück. Klicken Sie auf der Registerkarte **"Überprüfen"** im Abschnitt **"Änderungen"** auf **"Blatt schützen",** um das Dialogfeld **"Blatt schützen"** anzuzeigen. 
  
In der folgenden Tabelle sind drei Beispiele für die Werte aufgeführt, die von einem Aufruf von **xlfGetDef** mit dem angegebenen  _pxNameText-Argument_ zurückgegeben werden. 
  
|**Definition in Excel**|**_pxNameText_**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Der Name "Vertrieb" auf einem Blatt ist als Die Zahl 523 definiert.  <br/> |"Vertrieb"  <br/> |"=523"  <br/> |
|Der Name Gewinn auf dem aktiven Blatt ist als Formel Sales-Costs definiert.  <br/> |"! Gewinn"  <br/> |"=Verkaufskosten"  <br/> |
|The name Database on the active sheet is defined as the range A1:F500.  <br/> |"! Datenbank"  <br/> |"=R1C1:R500C6"  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [xlfGetDef](xlfgetdef.md)
- [Wichtige und nützliche C-API-XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

