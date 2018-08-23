---
title: UPREAD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 568f2336-cb4d-3f2c-a304-d29cdb0bcbcc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 887c66277b54e2e14c7f67c76b8e9dd4fa8bc719
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589231"
---
# <a name="upread"></a>UPREAD

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Informationen zum Hochladen von Elementen Zustand "gelesen" während der [Upload lesen Status Zustand](upload-read-status-state.md).
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct UPREAD 
{ 
    PUPREADE pupre; 
    UINT cEnt; 
};
```

## <a name="members"></a>Elemente

 _pupre_
  
>  [out] Vektor **[UPREADE](upreade.md)** Einträge. 
    
 _cEnt_
  
>  [out] Anzahl der Einträge **UPREADE** . 
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[UPREADE](upreade.md)

