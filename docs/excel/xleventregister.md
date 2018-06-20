---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: d837d87c479f70f0184a7cf1612dea5ab8c99e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790598"
---
# <a name="xleventregister"></a>xlEventRegister

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Verwendet, um einen Ereignishandler registrieren. In Excel 2010 eingeführt.
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a>Parameter

 _pxProcedure_ (**XltypeStr**)
  
Der Name des der Ereignishandlerfunktion, wie er in der DLL-Code wird angezeigt.
  
 _pxEvent_ (**vom Typ XltypeInt**)
  
Das Ereignis behandelt, indem die Funktion, die im Parameter _PxProcedure_ angegeben. 
  
Starten in Excel 2010, unterstützt Excel die folgenden Ereignisse:
  
|Document.SelectionChanged **-Ereignis**|**Beschreibung**|
|:-----|:-----|
|**xleventCalculationEnded** <br/> |Wird ausgelöst, wenn Excel eine Berechnung abgeschlossen ist. Sie können während der Berechnung nach diesem Ereignis reservierten Ressourcen frei.  <br/> |
|**xleventCalculationCanceled** <br/> |Wird ausgelöst, wenn der Benutzer die Berechnung unterbrochen wird. Die XLL sollten alle asynchronen Aktivitäten beenden. Das CalculationEnded-Ereignis wird unmittelbar nach diesem Ereignis ausgelöst.  <br/> |
   
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Wenn erfolgreich ist, gibt **"true"** (**XltypeBool**). Wenn nicht erfolgreich ist, gibt **FALSE**zurück.
  
## <a name="see-also"></a>Siehe auch



[Asynchrone benutzerdefinierte Funktionen](asynchronous-user-defined-functions.md)

