---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1df2c665f8e9d7a0bd6d47ec59b2adf706bead75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338864"
---
# <a name="upreade"></a>UPREADE

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erweiterte Informationen zum Hochladen des Lesestatus eines Elements während des [Uploadstatus](upload-read-status-state.md).
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a>Elemente

_ulFlags_
  
>  [out]/[in] Flags, um das entsprechende Verhalten während des Uploads zu bestimmen. 
    
  - UPR_ASSOC
    
    - Out Element ist ausgeblendet.
    
  - UPR_READ
    
    - Out Der Lesestatus des Elements wurde geändert.
    
  - UPR_OK
    
    - in Der Upload war erfolgreich. Der Client legt dies nach dem Hochladen von Informationen auf den Server fest.
    
  - UPR_COMMIT
    
    - in Laden Sie jetzt den Lesestatus des Elements hoch, statt auf das Ende des Upload- [Tabellenstatus](upload-table-state.md) zu warten, um mehr als ein Element zu verarbeiten. 
    
_skey_
  
> Out Der Quellschlüssel des Elements.
    
## <a name="see-also"></a>Siehe auch

- [Informationen über die Replikations-API](about-the-replication-api.md)
- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
- [MAPI-Konstanten](mapi-constants.md)
- [UPREAD](upread.md)

