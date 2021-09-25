---
title: IMAPIOfflineMgrUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIOfflineMgr.Unadvise
api_type:
- COM
ms.assetid: 250b9137-facb-81a2-41b1-96a57366c04e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 29d6b7bf1e8bbb9d9fb1d5a17441fb779d9d67ef
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604866"
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
  
> [in] Flags für das Abbrechen des Rückrufs. Nur der Wert MAPIOFFLINE_UNADVISE_DEFAULT wird unterstützt.
    
 _ulAdviseToken_
  
> [in] Ein Empfehlungstoken, das die Rückrufregistrierung identifiziert, die abgebrochen werden soll. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der Anruf war erfolgreich. Dieser Aufruf muss S_OK zurückgeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Entfernt die Registrierung für den Rückruf, der  *ulAdviseToken*  zugeordnet war, der von einem vorherigen Aufruf von **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** zurückgegeben wurde. Bewirkt, dass das **IMAPIOfflineMgr** -Objekt seinen Verweis auf das **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** -Objekt, das  *ulAdviseToken*  zugeordnet ist, freigibt. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[MAPI-Konstanten](mapi-constants.md)

