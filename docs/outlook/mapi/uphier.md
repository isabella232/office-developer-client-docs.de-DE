---
title: UPHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a75ca0dd-9c50-2a9f-6c59-1f8020833a01
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a1ec71d7120eab220ee3b11d2a751fba51cee48e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592094"
---
# <a name="uphier"></a>UPHIER
 
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Informationen zum Synchronisieren von einer Ordnerhierarchie während der [Hierarchie Zustand hochladen](upload-hierarchy-state.md).
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a>Elemente

_ulFlags_
  
> [in] Kennzeichen, die das Verhalten bei der Synchronisierung der Ordnerhierarchie ändern.
    
  - UPH_OK
    
    - [in] Der Upload war erfolgreich. Der Client legt dies nach dem Hochladen erfolgreich Informationen an den Server. Beim Anzeigen dieses Flag, löscht Outlook alle internen Protokollinformationen, die laut die Ordnerhierarchie aktualisieren erforderlich. 
    
    - Der Client übergibt das HRESULT, wenn der Hochladevorgang nicht erfolgreich war.
    
_pstmReserved_
  
> [out] Dieser Member wird für die Outlook interne Verwendung reserviert und wird nicht unterstützt.
    
_iEnt_
  
> [out] Index zum Nachverfolgen die Anzahl von *cEnt* angegebenen Ordner zu synchronisieren. 
    
_cEnt_
  
> [out] Anzahl der Ordner, die nicht mehr synchronisiert sind.
    
## <a name="see-also"></a>Siehe auch

- [Informationen über die Replikations-API](about-the-replication-api.md)
- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
- [MAPI-Konstanten](mapi-constants.md)

