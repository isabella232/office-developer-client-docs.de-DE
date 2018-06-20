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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 53fa6bd49190bb88daeb0438dc0112e34322383e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792248"
---
# <a name="imapiofflinemgradvise"></a>IMAPIOfflineMgr::Advise

  
  
**Betrifft**: Outlook 
  
Registriert einen Client für Rückrufe für eine offline-Objekt zu erhalten.
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
>  [in] Kennzeichen, die Verhalten zu ändern. Nur der Wert MAPIOFFLINE_ADVISE_DEFAULT wird unterstützt. 
    
 _pAdviseInfo_
  
> [in] Informationen zu den Typ des Rückrufs, wann ein Rückruf, eine Callback-Schnittstelle für den Anrufer sowie andere Details zu erhalten. Sie enthält außerdem eine Clienttoken, die Outlook verwendet, nachfolgende Benachrichtigung Rückrufe an den Client Anrufer senden.
    
 _pulAdviseToken_
  
> [out] Ein Advise-Token an den Clientaufrufer für anschließend stornieren Rückruf für das Objekt zurückgegeben.
    
## <a name="return-value"></a>R�ckgabewert

S_OK
  
> Der Aufruf war erfolgreich.
    
E_INVALIDARG
  
> Ein ungültiger Parameter es wurde angegeben.
    
E_NOINTERFACE
  
> Die Callback-Schnittstelle in *pAdviseInfo* angegebenen ist ungültig. 
    
## <a name="remarks"></a>Hinweise

Beim Öffnen einer offline-Objekts mithilfe von **[HrOpenOfflineObj](hropenofflineobj.md)**, erhält ein Client eine offline-Objekt, das **IMAPIOfflineMgr**unterstützt. Der Client kann für die Arten von mithilfe von **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** durch das Objekt unterstützt Rückrufe überprüfen. Der Client kann bestimmen, den Typ sowie andere Details zu den Rückruf es möchte, und rufen Sie dann **IMAPIOfflineMgr::Advise** registrieren, um eine solche Rückrufe zum Objekt empfangen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)


[MAPI-Konstanten](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

