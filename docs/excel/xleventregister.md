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
  
Wird zum Registrieren eines Ereignishandlers verwendet. In Excel 2010 eingeführt.
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a>Parameter

 _pxProcedure_ (**xltypeStr**)
  
Der Name der Ereignis Handlerfunktion, wie er im DLL-Code angezeigt wird.
  
 _pxEvent_ (**xltypeInt**)
  
Das Ereignis, das von der im _pxProcedure_ -Parameter festgelegten Funktion behandelt wird. 
  
Beginnend mit Excel 2010 unterstützt Excel die folgenden Ereignisse:
  
|**Event**|**Beschreibung**|
|:-----|:-----|
|**xleventCalculationEnded** <br/> |Wird ausgelöst, wenn Excel eine Berechnung abgeschlossen hat. Sie können alle während der Berechnung zugeordneten Ressourcen nach diesem Ereignis freigeben.  <br/> |
|**xleventCalculationCanceled** <br/> |Wird ausgelöst, wenn der Benutzer die Berechnung unterbricht. Die XLL sollte alle asynchronen Aktivitäten beenden. Das CalculationEnded-Ereignis wird unmittelbar nach diesem Ereignis ausgelöst.  <br/> |
   
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Wenn die Methode erfolgreich verläuft, hat pxRes (**xltypeInt**) einen Wert > 0. Wenn nicht erfolgreich, pxRes = = 0.
  
## <a name="see-also"></a>Siehe auch



[Asynchrone benutzerdefinierte Funktionen](asynchronous-user-defined-functions.md)

