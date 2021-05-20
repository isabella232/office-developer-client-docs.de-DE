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
ms.openlocfilehash: 77688f8a09c1d990201a247a3c4e3a11ba0963b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438624"
---
# <a name="imsprovidershutdown"></a>IMSProvider::Shutdown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Schließt einen Nachrichtenspeicheranbieter in geordneter Weise.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpulFlags_
  
> [in] Reserviert; muss ein Zeiger auf Null sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
## <a name="remarks"></a>Hinweise

MAPI ruft die **IMSProvider::Shutdown-Methode auf,** kurz bevor das Objekt des Nachrichtenspeicheranbieters veröffentlicht wird. MAPI gibt alle Anmeldeobjekte für einen Anbieter frei, bevor **das Herunterfahren für** den Anbieter aufruft. 
  
## <a name="see-also"></a>Siehe auch



[IMSProvider : IUnknown](imsprovideriunknown.md)

