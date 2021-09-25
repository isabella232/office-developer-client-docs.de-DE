---
title: UPHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a75ca0dd-9c50-2a9f-6c59-1f8020833a01
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d75f072d07b987d2f243d64eda5829348a19c2aa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623943"
---
# <a name="uphier"></a>UPHIER
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Informationen zum Synchronisieren einer Ordnerhierarchie während des [Uploadhierarchiestatus.](upload-hierarchy-state.md)
  
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
  
> [in] Kennzeichen zum Ändern des Verhaltens beim Synchronisieren der Ordnerhierarchie.
    
  - UPH_OK
    
    - [in] Hochladen erfolgreich war. Der Client legt dies nach dem erfolgreichen Hochladen von Informationen auf den Server fest. Wenn dieses Kennzeichen angezeigt wird, löscht Outlook alle internen Buchführungsinformationen, die darauf hindeuteten, dass die Ordnerhierarchie aktualisiert werden muss. 
    
    - Der Client übergibt HRESULT, wenn der Upload nicht erfolgreich war.
    
_pstmReserved_
  
> [out] Dieses Mitglied ist für Outlook interne Verwendung reserviert und wird nicht unterstützt.
    
_iEnt_
  
> [out] Index to track synchronizing the number of folders specified by  *cEnt*  . 
    
_cEnt_
  
> [out] Die Anzahl der Ordner, die nicht synchronisiert sind.
    
## <a name="see-also"></a>Siehe auch

- [Informationen über die Replikations-API](about-the-replication-api.md)
- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
- [MAPI-Konstanten](mapi-constants.md)

