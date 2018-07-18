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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6e917991e109ac04a14ea7d93eebcf9cce835845
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792417"
---
# <a name="imapisupportspooleryield"></a>IMAPISupport::SpoolerYield

  
  
**Betrifft**: Outlook 
  
Bietet Kontrolle über die CPU auf die MAPI-Warteschlange, damit sie alle Aufgaben ausführen kann, notwendig hält.
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> Reserviert. NULL muss sein.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Transportdienst veröffentlicht erfolgreich CPU.
    
MAPI_W_CANCEL_MESSAGE 
  
> Weist der Adressbuchhierarchie So beenden Sie die Zustellung der Nachricht an alle Empfänger, die noch nicht erhalten haben.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::SpoolerYield** -Methode wird für Transport Anbieter Unterstützungsobjekte implementiert. Transportanbieter Aufrufen **SpoolerYield** , um die MAPI-Warteschlange, die erforderliche Verarbeitung bezwecken zu ermöglichen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **SpoolerYield** , wenn Sie langer Vorgänge ausführen, die angehalten werden können. Dadurch können Vordergrund während eines langen Vorgangs, wie die Zustellung an eine große Empfängerliste über Datenverkehrsaufkommen ausgeführt werden. 
  
Wenn **SpoolerYield** mit MAPI_W_CANCEL_MESSAGE zurückgibt, wurde die MAPI-Warteschlange festgestellt, dass die Nachricht nicht mehr gesendet werden soll. Geben Sie nach Möglichkeit MAPI_E_USER_CANCEL an die aufrufende Prozess und beenden, zurück. 
  
Weitere Informationen dazu, die MAPI-Warteschlange Zurückhalten finden Sie unter [Interaktion mit der MAPI-Warteschlange](interacting-with-the-mapi-spooler.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport: IUnknown](imapisupportiunknown.md)

