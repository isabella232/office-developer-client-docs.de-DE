---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 00c222efce6925c3f691eb2b799adf687c22082c
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160279"
---
# <a name="xleventregister"></a>xlEventRegister

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wird zum Registrieren eines Ereignishandlers verwendet. Eingeführt in Excel 2010.
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a>Parameter

 _pxProcedure_ (**xltypeStr**)
  
Der Name des Ereignishandlers funktioniert so, wie er im DLL-Code angezeigt wird.
  
 _pxEvent_ (**xltypeInt**)
  
Das Ereignis, das von der im  _Parameter pxProcedure_ festgelegten Funktion verarbeitet wird. 
  
Ab Excel 2010 unterstützt Excel die folgenden Ereignisse:
  
|**Event**|**Beschreibung**|
|:-----|:-----|
|**xleventCalculationEnded** <br/> |Wird ausgelöst, Excel eine Berechnung abgeschlossen ist. Sie können alle Ressourcen frei, die während der Berechnung nach diesem Ereignis zugewiesen wurden.  <br/> |
|**xleventCalculationCanceled** <br/> |Wird ausgelöst, wenn der Benutzer die Berechnung unterbricht. Die XLL sollte alle asynchronen Aktivitäten beenden. Das CalculationEnded-Ereignis wird unmittelbar nach diesem Ereignis ausgelöst.  <br/> |
   
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Wenn dies erfolgreich ist, hat pxRes (**xltypeInt**) den Wert > 0. Wenn dies nicht erfolgreich ist, ist pxRes ==0.
  
## <a name="see-also"></a>Siehe auch



[Asynchrone benutzerdefinierte Funktionen](asynchronous-user-defined-functions.md)

