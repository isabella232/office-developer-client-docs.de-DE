---
title: UPREAD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 568f2336-cb4d-3f2c-a304-d29cdb0bcbcc
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fa3c0b90a64c90a7c854cb22ac75438fa5fca23f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795811"
---
# <a name="upread"></a>UPREAD

  
  
**Betrifft**: Outlook 
  
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

