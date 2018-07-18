---
title: IMSProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.Shutdown
api_type:
- COM
ms.assetid: 9ca1861d-9bc9-485a-9807-a598b869e5a2
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 334ec8dd0c683cf9b765f387281c624b20520098
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792675"
---
# <a name="imsprovidershutdown"></a>IMSProvider::Shutdown

  
  
**Betrifft**: Outlook 
  
Schließt einen Anbieter für Nachricht Anmelden in einer bestimmten Reihenfolge.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpulFlags_
  
> [in] Reserviert. Ein Zeiger auf 0 (null) muss sein.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

MAPI-Aufrufen die **IMSProvider::Shutdown** -Methode unmittelbar vor der Freigabe des Message-Speicher-Anbieter-Objekts. MAPI-Freigaben für alle Logon-Objekten für einen Anbieter vor dem **Herunterfahren** für diesen Anbieter aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[IMSProvider : IUnknown](imsprovideriunknown.md)

