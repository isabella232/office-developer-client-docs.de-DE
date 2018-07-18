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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b52dcd87c8714ad59db560a5ae4a8300f9cc83ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792254"
---
# <a name="imapiofflinemgrunadvise"></a>IMAPIOfflineMgr::Unadvise

  
  
**Betrifft**: Outlook 
  
Bricht Rückrufe für eine offline-Objekt ab.
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Flags für das Abbrechen Rückruf. Nur der Wert MAPIOFFLINE_UNADVISE_DEFAULT wird unterstützt.
    
 _ulAdviseToken_
  
> [in] Ein Advise-Token, das die Rückruf Registrierung identifiziert, die abgebrochen werden soll. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK
  
> Der Aufruf war erfolgreich. Dieser Aufruf muss S_OK zurück.
    
## <a name="remarks"></a>Bemerkungen

Entfernt die Registrierung des Rückrufs, die mit *UlAdviseToken* zurückgegeben, die von einem vorherigen Aufruf von **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** zugeordnet wurde. Bewirkt, dass das **IMAPIOfflineMgr** -Objekt, das den Verweis auf das zugeordnete *UlAdviseToken* **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** -Objekt freigeben. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[MAPI-Konstanten](mapi-constants.md)

