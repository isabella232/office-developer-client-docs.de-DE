---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 869122954ffe3928dfea72b8fc9fb432b9979e42
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303934"
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
  
Das Ereignis, das von der im _pxProcedure_ -Parameter angegebenen Funktion behandelt wird. 
  
Ab Excel 2010 unterstützt Excel die folgenden Ereignisse:
  
|**Event**|**Beschreibung**|
|:-----|:-----|
|**xleventCalculationEnded** <br/> |Wird ausgelöst, wenn Excel eine Berechnung abgeschlossen hat. Sie können alle Ressourcen freigeben, die während der Berechnung nach diesem Ereignis zugeordnet sind.  <br/> |
|**xleventCalculationCanceled** <br/> |Wird ausgelöst, wenn der Benutzer die Berechnung unterbricht. Die XLL sollte alle asynchronen Aktivitäten beenden. Das CalculationEnded-Ereignis wird unmittelbar nach diesem Ereignis ausgelöst.  <br/> |
   
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Wenn der Wert erfolgreich ist, wird **true** (**xltypeBool**) zurückgegeben. Wenn nicht erfolgreich, gibt **false**zurück.
  
## <a name="see-also"></a>Siehe auch



[Asynchrone benutzerdefinierte Funktionen](asynchronous-user-defined-functions.md)

