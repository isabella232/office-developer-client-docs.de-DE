---
title: IMAPISupportSpoolerYield
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SpoolerYield
api_type:
- COM
ms.assetid: f5c6ba8f-4ef5-4d60-b4e6-5b9160ec4e99
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f6cdebf82d8b84ada3d029865867c5192af90b0d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409909"
---
# <a name="imapisupportspooleryield"></a>IMAPISupport::SpoolerYield

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die CPU-Steuerung für den MAPI-Spooler an, sodass Sie alle für erforderlich erachteten Aufgaben ausführen kann.
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> Reserviert muss NULL sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Transportanbieter hat die CPU erfolgreich veröffentlicht.
    
MAPI_W_CANCEL_MESSAGE 
  
> Weist den Transportanbieter an, die Übermittlung der Nachricht an Empfänger zu beenden, die Sie noch nicht erhalten haben.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: SpoolerYield** -Methode wird für Support Objekte des Transportanbieters implementiert. Transport Anbieter rufen **SpoolerYield** auf, damit der MAPI-Spooler alle erforderlichen Verarbeitungsschritte ausführen kann. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **SpoolerYield** auf, wenn Sie längere Vorgänge ausführen, die angehalten werden können. Auf diese Weise können vordergrundanwendungen während eines langen Betriebs ausgeführt werden, beispielsweise die Übertragung an eine große Empfängerliste in einem belebten Netzwerk. 
  
Wenn **SpoolerYield** mit MAPI_W_CANCEL_MESSAGE zurückgibt, hat der MAPI-Spooler festgestellt, dass die Nachricht nicht mehr gesendet werden soll. Geben Sie MAPI_E_USER_CANCEL an den Anruf Prozess zurück, und beenden Sie, wenn möglich. 
  
Weitere Informationen zur Angabe des MAPI-Spoolers finden Sie unter [interagieren mit dem MAPI](interacting-with-the-mapi-spooler.md)-Spooler.
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport: IUnknown](imapisupportiunknown.md)

