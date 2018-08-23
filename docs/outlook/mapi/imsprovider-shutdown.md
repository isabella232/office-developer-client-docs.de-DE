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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 342b87a3a8f0349631e64600e294d4f19ab1099c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589091"
---
# <a name="imsprovidershutdown"></a>IMSProvider::Shutdown

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="remarks"></a>HinwBemerkungeneise

MAPI-Aufrufen die **IMSProvider::Shutdown** -Methode unmittelbar vor der Freigabe des Message-Speicher-Anbieter-Objekts. MAPI-Freigaben für alle Logon-Objekten für einen Anbieter vor dem **Herunterfahren** für diesen Anbieter aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[IMSProvider : IUnknown](imsprovideriunknown.md)

