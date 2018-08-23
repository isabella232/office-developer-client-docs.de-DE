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
ms.openlocfilehash: 35dfc7af9852609dcfcc3fcb9d65ec2e4afa9632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579522"
---
# <a name="imapiofflinemgrunadvise"></a>IMAPIOfflineMgr::Unadvise

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="remarks"></a>HinwBemerkungeneise

Entfernt die Registrierung des Rückrufs, die mit *UlAdviseToken* zurückgegeben, die von einem vorherigen Aufruf von **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** zugeordnet wurde. Bewirkt, dass das **IMAPIOfflineMgr** -Objekt, das den Verweis auf das zugeordnete *UlAdviseToken* **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** -Objekt freigeben. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[MAPI-Konstanten](mapi-constants.md)

