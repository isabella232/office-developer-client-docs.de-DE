---
title: IMAPISupportGetSvcConfigSupportObj
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.GetSvcConfigSupportObj
api_type:
- COM
ms.assetid: 56c3bdae-a3a8-4334-b6d2-a89c6820d72e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a7ed092639c7a0e7a6c1b1d39c01006ec87fdb85
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567445"
---
# <a name="imapisupportgetsvcconfigsupportobj"></a>IMAPISupport::GetSvcConfigSupportObj

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt ein Nachrichtendienst-Supportobjekt.
  
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
  
> [out] Ein Zeiger auf einen Zeiger auf das neue Nachrichtendienst-Supportobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Konfigurationsunterstützungsobjekt wurde erfolgreich erstellt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::GetSvcConfigSupportObj-Methode** wird für alle Unterstützungsobjekte implementiert. Dienstanbieter rufen **GetSvcConfigSupportObj** auf, um ein Konfigurationsunterstützungsobjekt zu erstellen, das an eine Nachrichtendienst-Einstiegspunktfunktion übergeben wird. 
  
Eine Nachrichtendienst-Einstiegspunktfunktion basiert auf dem [MSGSERVICEENTRY-Prototyp](msgserviceentry.md) und wird von Methoden der [IMsgServiceAdmin-Schnittstelle](imsgserviceadminiunknown.md) aufgerufen. Mit einer Nachrichtendienst-Einstiegspunktfunktion können Nachrichtendienste sich selbst konfigurieren oder andere Aktionen ausführen, wenn das Profil geändert wird. Nachrichtendienst-Einstiegspunktfunktionen können Konfigurationsänderungen unterstützen, indem ein Eigenschaftenblatt oder ein Eigenschaftswertarray angezeigt wird, das an die [IMsgServiceAdmin::ConfigureMsgService-Methode](imsgserviceadmin-configuremsgservice.md) übergeben wird. 
  
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

