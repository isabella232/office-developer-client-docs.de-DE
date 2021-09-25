---
title: IABProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABProvider.Shutdown
api_type:
- COM
ms.assetid: 1fbe6dc1-254b-4557-92c8-9fa42a8efd64
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ba11186c21562b14ff61d7128d9cf70028bb2201
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584479"
---
# <a name="iabprovidershutdown"></a>IABProvider::Shutdown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bricht eine Verbindung mit einer aktiven Sitzung ab.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpulFlags_
  
> [In] Reserviert; muss ein Zeiger auf Null sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Verbindung wurde erfolgreich abgebrochen.
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Führen Sie bei der Implementierung der **Shutdown-Methode** die von Ihnen für erforderlich erachteten Aufgaben aus. MAPI ruft die **Shutdown-Methode** erst auf, nachdem Sie alle Anmeldeobjekte freigegeben haben. 
  
## <a name="see-also"></a>Siehe auch



[IABProvider : IUnknown](iabprovideriunknown.md)

