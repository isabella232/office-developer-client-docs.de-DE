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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6de0fed4df9d23e67c3520ffb019a961b890f988
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411309"
---
# <a name="imapisupportgetsvcconfigsupportobj"></a>IMAPISupport::GetSvcConfigSupportObj

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt ein Support Objekt für den Nachrichtendienst.
  
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
  
> Out Ein Zeiger auf einen Zeiger auf das Support Objekt des neuen Nachrichtendiensts.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Konfigurations Unterstützungsobjekt wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: GetSvcConfigSupportObj** -Methode wird für alle Support-Objekte implementiert. Dienstanbieter rufen **GetSvcConfigSupportObj** auf, um ein Konfigurations Unterstützungsobjekt zu erstellen, das an eine Nachrichtendienst-Einstiegspunktfunktion weitergegeben wird. 
  
Eine Nachrichtendienst-Einstiegspunktfunktion basiert auf dem [MSGSERVICEENTRY](msgserviceentry.md) -Prototyp und wird von Methoden der [IMsgServiceAdmin](imsgserviceadminiunknown.md) -Schnittstelle aufgerufen. Eine Nachrichtendienst-Einstiegspunktfunktion ermöglicht es Nachrichtendiensten, sich selbst zu konfigurieren oder andere Aktionen auszuführen, wenn das Profil geändert wird. Einstiegspunktfunktionen für den Nachrichtendienst können Konfigurationsänderungen unterstützen, indem ein Eigenschaftenblatt oder ein Eigenschafts Wertarray angezeigt wird, das an die [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) -Methode übergeben wird. 
  
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

