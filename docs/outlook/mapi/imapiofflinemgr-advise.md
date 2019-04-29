---
title: IMAPIOfflineMgrAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Advise
api_type:
- COM
ms.assetid: 784b6218-548d-817a-caaa-cf9be6bc3d2f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3ca7fdc39da8d3ee8ecf6f0f253284df10a392e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426919"
---
# <a name="imapiofflinemgradvise"></a>IMAPIOfflineMgr::Advise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert einen Client für den Empfang von Rückrufen für ein Offlineobjekt.
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
>  in Kennzeichen, die das Verhalten ändern. Nur der Wert MAPIOFFLINE_ADVISE_DEFAULT wird unterstützt. 
    
 _pAdviseInfo_
  
> in Informationen zum Rückruftyp, zum Empfang eines Rückrufs, eine Rückrufschnittstelle für den Anrufer und weitere Details. Außerdem enthält es ein Clienttoken, das Outlook beim Senden von nachfolgenden Benachrichtigungs Rückrufen an den Client Aufrufer verwendet.
    
 _pulAdviseToken_
  
> Out Ein Advise-Token, das an den Aufrufer des Clients zurückgegeben wird, um den Rückruf für das Objekt abzubrechen.
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der Anruf wurde erfolgreich ausgeführt.
    
E_INVALIDARG
  
> Es wurde ein ungültiger Parameter angegeben.
    
E_NOINTERFACE
  
> Die in *pAdviseInfo* angegebene Rückrufschnittstelle ist ungültig. 
    
## <a name="remarks"></a>Bemerkungen

Beim Öffnen eines Offline Objekts mithilfe von **[HrOpenOfflineObj](hropenofflineobj.md)** Ruft ein Client ein Offlineobjekt ab, das **IMAPIOfflineMgr**unterstützt. Der Client kann die vom Objekt unterstützten Rückruf Typen mithilfe von **[IMAPIOffline:: getCapabilities](imapioffline-getcapabilities.md)** überprüfen. Der Client kann den Typ und weitere Details zu dem gewünschten Rückruf ermitteln und dann **IMAPIOfflineMgr:: Advise** aufrufen, um sich für das empfangen solcher Rückrufe über das Objekt zu registrieren. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)


[MAPI-Konstanten](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

