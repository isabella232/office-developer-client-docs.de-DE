---
title: IMAPISupportSpoolerYield
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.SpoolerYield
api_type:
- COM
ms.assetid: f5c6ba8f-4ef5-4d60-b4e6-5b9160ec4e99
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6cc11912b721a624b065c6d21169056843ceac0e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575729"
---
# <a name="imapisupportspooleryield"></a>IMAPISupport::SpoolerYield

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Steuerung der CPU an den MAPI-Spooler weiter, damit alle aufgaben ausgeführt werden können, die er für erforderlich hält.
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> Reserviert; muss Null sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Transportanbieter hat die CPU erfolgreich freigegeben.
    
MAPI_W_CANCEL_MESSAGE 
  
> Weist den Transportanbieter an, die Zustellung der Nachricht an empfänger zu beenden, die sie noch nicht erhalten haben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::SpoolerYield-Methode** wird für Supportobjekte des Transportanbieters implementiert. Transportanbieter rufen **SpoolerYield** auf, damit der MAPI-Spooler alle erforderlichen Verarbeitungen ausführen kann. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **SpoolerYield** auf, wenn Sie lange Vorgänge ausführen, die angehalten werden können. Dadurch können Vordergrundanwendungen während eines langen Vorgangs ausgeführt werden, z. B. bei der Übermittlung an eine große Empfängerliste über ein besetztes Netzwerk. 
  
Wenn **SpoolerYield** mit MAPI_W_CANCEL_MESSAGE zurückgegeben wird, hat der MAPI-Spooler festgestellt, dass die Nachricht nicht mehr gesendet werden soll. Kehren Sie MAPI_E_USER_CANCEL zu Ihrem Anrufvorgang zurück, und beenden Sie, wenn möglich. 
  
Weitere Informationen zum Bereitstellen des MAPI-Spoolers finden Sie unter [Interagieren mit dem MAPI-Spooler.](interacting-with-the-mapi-spooler.md)
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport: IUnknown](imapisupportiunknown.md)

