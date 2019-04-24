---
title: UPDEL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b23291d-3355-d772-4647-d4bbd64b0b53
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c9d2ec7f1970e3d1cadb65ab9af360b5c01c6844
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360487"
---
# <a name="updel"></a>UPDEL

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Informationen zu Elementen, die in einem lokalen Speicher gelöscht wurden. Diese Informationen werden während des Status Status des [Uploads gelöscht](upload-delete-status-state.md).
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a>Elemente

 _pupde_
  
>  Out Vektor der [UPdele](updele.md) -Einträge. 
    
 _Prozent_
  
> Out Anzahl der Einträge in *pupde* . 
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[MAPI-Konstanten](mapi-constants.md)

