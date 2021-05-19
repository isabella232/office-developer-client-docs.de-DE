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
  
Gibt dem MAPI-Spooler die Kontrolle über die CPU, sodass er alle für erforderlich erachteten Aufgaben ausführen kann.
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> Reserviert; muss null sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Transportanbieter hat die CPU erfolgreich freigegeben.
    
MAPI_W_CANCEL_MESSAGE 
  
> Der Transportanbieter wird angewiesen, die Zustellung der Nachricht an alle Empfänger zu beenden, die sie noch nicht empfangen haben.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::SpoolerYield-Methode** wird für Unterstützungsobjekte des Transportanbieters implementiert. Transportanbieter rufen **SpoolerYield auf,** damit der MAPI-Spooler alle erforderlichen Verarbeitungsschritte ausführen kann. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen **Sie SpoolerYield auf,** wenn Sie langwierige Vorgänge ausführen, die angehalten werden können. Dadurch können Vordergrundanwendungen während eines langen Vorgangs ausgeführt werden, z. B. die Zustellung an eine große Empfängerliste über ein ausgelastetes Netzwerk. 
  
Wenn **SpoolerYield** mit MAPI_W_CANCEL_MESSAGE zurückgibt, hat der MAPI-Spooler festgestellt, dass die Nachricht nicht mehr gesendet werden soll. Geben MAPI_E_USER_CANCEL Zurück zu Ihrem Anrufprozess zurück, und beenden Sie sie, wenn möglich. 
  
Weitere Informationen zum Nachgeben an den MAPI-Spooler finden Sie unter [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport: IUnknown](imapisupportiunknown.md)

