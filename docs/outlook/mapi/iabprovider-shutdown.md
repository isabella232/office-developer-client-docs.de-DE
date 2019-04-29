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
ms.openlocfilehash: 8b2190f77c7575d3d4f5e25fa0863bec844158bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409783"
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
  
> In Reserviert muss ein Zeiger auf NULL sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Verbindung wurde erfolgreich abgebrochen.
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Führen Sie in der Implementierung der **Shutdown** -Methode alle Aufgaben aus, die Sie für erforderlich halten. MAPI Ruft die **Shutdown** -Methode nur auf, nachdem Sie alle Anmeldeobjekte freigegeben haben. 
  
## <a name="see-also"></a>Siehe auch



[IABProvider : IUnknown](iabprovideriunknown.md)

