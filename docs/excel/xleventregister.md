---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c5236a2859b69a45481b4eedd587b923dbe0776e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631489"
---
# <a name="xleventregister"></a>xlEventRegister

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wird zum Registrieren eines Ereignishandlers verwendet. Eingeführt in Excel 2010.
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a>Parameter

 _pxProcedure_ (**xltypeStr**)
  
Der Name der Ereignishandlerfunktion, wie er im DLL-Code angezeigt wird.
  
 _pxEvent_ (**xltypeInt**)
  
Das Ereignis, das von der im  _pxProcedure-Parameter angegebenen_ Funktion behandelt wird. 
  
Ab Excel 2010 unterstützt Excel die folgenden Ereignisse:
  
|Document.SelectionChanged **-Ereignis**|**Beschreibung**|
|:-----|:-----|
|**xleventCalculationEnded** <br/> |Wird ausgelöst, wenn Excel eine Berechnung abgeschlossen hat. Sie können alle Ressourcen freigeben, die während der Berechnung nach diesem Ereignis zugewiesen wurden.  <br/> |
|**xleventCalculationCanceled** <br/> |Wird ausgelöst, wenn der Benutzer die Berechnung unterbricht. Die XLL sollte asynchrone Aktivitäten beenden. Das CalculationEnded-Ereignis wird unmittelbar nach diesem Ereignis ausgelöst.  <br/> |
   
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Bei erfolgreicher Ausführung hat pxRes (**xltypeInt**) den Wert > 0. Wenn nicht erfolgreich, pxRes ==0.
  
## <a name="see-also"></a>Siehe auch



[Asynchrone benutzerdefinierte Funktionen](asynchronous-user-defined-functions.md)

