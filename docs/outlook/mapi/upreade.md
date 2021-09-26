---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d096c9f50efa4590dc6a6f4fb0fd2f79329e6189
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629459"
---
# <a name="upreade"></a>UPREADE

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erweiterte Informationen zum Hochladen des Lesestatus eines Elements während des Status des [Uploadlesestatus.](upload-read-status-state.md)
  
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
    
    - [out] Element ist ausgeblendet.
    
  - UPR_READ
    
    - [out] Der Lesestatus des Elements wurde geändert.
    
  - UPR_OK
    
    - [in] Hochladen erfolgreich war. Der Client legt dies nach dem Hochladen von Informationen auf den Server fest.
    
  - UPR_COMMIT
    
    - [in] Hochladen den Lesestatus des Elements ab, anstatt bis zum Ende des [Uploadtabellenstatus](upload-table-state.md) zu warten, um mehrere Elemente im Batchprozess zu verarbeiten. 
    
_skey_
  
> [out] Quellschlüssel des Elements.
    
## <a name="see-also"></a>Siehe auch

- [Informationen über die Replikations-API](about-the-replication-api.md)
- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
- [MAPI-Konstanten](mapi-constants.md)
- [UPREAD](upread.md)

