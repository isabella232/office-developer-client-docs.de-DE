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
  
Registriert einen Client zum Empfangen von Rückrufen für ein Offlineobjekt.
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
>  [in] Flags, die das Verhalten ändern. Nur der Wert MAPIOFFLINE_ADVISE_DEFAULT wird unterstützt. 
    
 _pAdviseInfo_
  
> [in] Informationen zum Typ des Rückrufs, zum Empfang eines Rückrufs, einer Rückrufschnittstelle für den Anrufer und anderen Details. Außerdem enthält es ein Clienttoken, das Outlook beim Senden nachfolgender Benachrichtigungsrückrufe an den Clientaufrufer verwendet wird.
    
 _pulAdviseToken_
  
> [out] Ein an den Clientaufrufer zurückgegebenes Ratschlagtoken zum anschließenden Abbrechen des Rückrufs für das Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der Aufruf war erfolgreich.
    
E_INVALIDARG
  
> Ein ungültiger Parameter wurde angegeben.
    
E_NOINTERFACE
  
> Die in  *pAdviseInfo*  angegebene Rückrufschnittstelle ist ungültig. 
    
## <a name="remarks"></a>Hinweise

Beim Öffnen eines Offlineobjekts mithilfe von **[HrOpenOfflineObj](hropenofflineobj.md)** ruft ein Client ein Offlineobjekt ab, das **IMAPIOfflineMgr unterstützt.** Der Client kann mithilfe von **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** nach den Arten von Rückrufen suchen, die vom Objekt unterstützt werden. Der Client kann den Typ und andere Details zu dem Rückruf bestimmen, den er möchte, und dann **IMAPIOfflineMgr::Advise** aufrufen, sich zu registrieren, um solche Rückrufe für das Objekt zu erhalten. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)


[MAPI-Konstanten](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

