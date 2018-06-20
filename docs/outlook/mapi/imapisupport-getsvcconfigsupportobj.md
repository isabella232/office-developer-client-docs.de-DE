---
title: IMAPISupportGetSvcConfigSupportObj
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetSvcConfigSupportObj
api_type:
- COM
ms.assetid: 56c3bdae-a3a8-4334-b6d2-a89c6820d72e
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5d7e3e89f15b1bc08c7ce9faab0d0a6326300e70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792363"
---
# <a name="imapisupportgetsvcconfigsupportobj"></a>IMAPISupport::GetSvcConfigSupportObj

  
  
**Betrifft**: Outlook 
  
Erstellt ein Objekt "Message" Service Support.
  
```cpp
HRESULT GetSvcConfigSupportObj(
  ULONG ulFlags,
  LPMAPISUP FAR * lppSvcSupport
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lppSvcSupport_
  
> [out] Ein Zeiger auf einen Zeiger auf das neue Nachricht Support-Objekt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Support-Konfigurationsobjekt wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::GetSvcConfigSupportObj** -Methode wird für alle Unterstützungsobjekte implementiert. Dienstanbieter anrufen **GetSvcConfigSupportObj** zum Erstellen eines Objekts Konfiguration Unterstützung, um auf eine Nachricht Service Entry Point-Funktion zu übergeben. 
  
Eine Nachricht Service Entry Point-Funktion basiert auf den [MSGSERVICEENTRY](msgserviceentry.md) Prototyp und von Methoden der [IMsgServiceAdmin](imsgserviceadminiunknown.md) -Schnittstelle aufgerufen wird. Eine Nachricht Service Entry Point-Funktion ermöglicht Message Dienste so konfigurieren selbst oder andere Aktionen durchführen, wenn das Profil geändert wird. Nachricht Service-Einstiegspunkt, dass Funktionen konfigurationsänderungen unterstützen können durch Anzeigen eines Eigenschaftenblatts oder über ein Array-Eigenschaft Wert an die [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) -Methode übergeben. 
  
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md)
  
[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[IProfAdmin: IUnknown](iprofadminiunknown.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

