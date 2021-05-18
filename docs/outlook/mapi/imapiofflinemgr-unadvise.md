---
title: IMAPIOfflineMgrUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Unadvise
api_type:
- COM
ms.assetid: 250b9137-facb-81a2-41b1-96a57366c04e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 800f79179f999ba193d4177abb7341095b8b896d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404855"
---
# <a name="imapiofflinemgrunadvise"></a>IMAPIOfflineMgr::Unadvise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bricht Rückrufe für ein Offlineobjekt ab.
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Flags zum Abbrechen des Rückrufs. Nur der Wert MAPIOFFLINE_UNADVISE_DEFAULT wird unterstützt.
    
 _ulAdviseToken_
  
> [in] Ein Ratentoken, das die Rückrufregistrierung identifiziert, die abgebrochen werden soll. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der Aufruf war erfolgreich. Dieser Aufruf muss eine S_OK.
    
## <a name="remarks"></a>Hinweise

Entfernt die Registrierung für den Rückruf, der *ulAdviseToken* zugeordnet war, die aus einem vorherigen Aufruf von **[IMAPIOfflineMgr::Advise zurückgegeben wurde.](imapiofflinemgr-advise.md)** Bewirkt, **dass das IMAPIOfflineMgr-Objekt** seinen Verweis auf das **[IMAPIOfflineNotify-Objekt](imapiofflinenotifyiunknown.md)** frei gibt, das *ulAdviseToken zugeordnet ist.* 
  
## <a name="see-also"></a>Siehe auch



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[MAPI-Konstanten](mapi-constants.md)

