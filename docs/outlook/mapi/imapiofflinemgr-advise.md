---
title: IMAPIOfflineMgrAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIOfflineMgr.Advise
api_type:
- COM
ms.assetid: 784b6218-548d-817a-caaa-cf9be6bc3d2f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 17d3bd9edb392db85ba8b5845a396fbf41af4525
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596183"
---
# <a name="imapiofflinemgradvise"></a>IMAPIOfflineMgr::Advise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert einen Client, um Rückrufe für ein Offlineobjekt zu empfangen.
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
>  [in] Kennzeichen, die das Verhalten ändern. Nur der Wert MAPIOFFLINE_ADVISE_DEFAULT wird unterstützt. 
    
 _pAdviseInfo_
  
> [in] Informationen zum Typ des Rückrufs, zum Zeitpunkt des Empfangs eines Rückrufs, zu einer Rückrufschnittstelle für den Anrufer und zu weiteren Details. Es enthält auch ein Clienttoken, das Outlook beim Senden nachfolgender Benachrichtigungsrückrufe an den Clientaufrufer verwendet.
    
 _pulAdviseToken_
  
> [out] Ein an den Client-Aufrufer zurückgegebenes Empfehlungstoken zum anschließenden Abbrechen des Rückrufs für das Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der Anruf war erfolgreich.
    
E_INVALIDARG
  
> Ein ungültiger Parameter wurde angegeben.
    
E_NOINTERFACE
  
> Die in  *pAdviseInfo*  angegebene Rückrufschnittstelle ist ungültig. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Beim Öffnen eines Offlineobjekts mit **[HrOpenOfflineObj](hropenofflineobj.md)** ruft ein Client ein Offlineobjekt ab, das **IMAPIOfflineMgr** unterstützt. Der Client kann mithilfe von **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** nach den Arten von Rückrufen suchen, die vom Objekt unterstützt werden. Der Client kann den Typ und andere Details zu dem von ihm benötigten Rückruf ermitteln und dann **IMAPIOfflineMgr::Advise** aufrufen, um sich zu registrieren, um solche Rückrufe über das Objekt zu erhalten. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)


[MAPI-Konstanten](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

