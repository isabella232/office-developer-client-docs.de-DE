---
title: IABProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Shutdown
api_type:
- COM
ms.assetid: 1fbe6dc1-254b-4557-92c8-9fa42a8efd64
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0a93dd44960a01996672a55501a7626d0ff56986
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567888"
---
# <a name="iabprovidershutdown"></a>IABProvider::Shutdown

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Bricht eine Verbindung mit einer aktiven Sitzung ab.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpulFlags_
  
> [In] Reserviert. Ein Zeiger auf 0 (null) muss sein.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Verbindung wurde erfolgreich abgebrochen.
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Führen Sie in der Implementierung der **Shutdown** -Methode jegliches Aufgaben erforderlich werden sollten. MAPI-Aufrufen **Shutdown** -Methode nur, nachdem Sie alle Objekte Ihrer Anmeldung freigegeben haben. 
  
## <a name="see-also"></a>Siehe auch



[IABProvider : IUnknown](iabprovideriunknown.md)

