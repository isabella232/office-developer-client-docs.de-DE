---
title: UPREAD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 568f2336-cb4d-3f2c-a304-d29cdb0bcbcc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 844030b69c07196278069a3011f73bf892be996b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623929"
---
# <a name="upread"></a>UPREAD

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Informationen zum Hochladen des Lesestatus von Elementen während des Status des [Uploadlesestatus.](upload-read-status-state.md)
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct UPREAD 
{ 
    PUPREADE pupre; 
    UINT cEnt; 
};
```

## <a name="members"></a>Elemente

 _mitre_
  
>  [out] Vektor von **[UPREADE-Einträgen.](upreade.md)** 
    
 _cEnt_
  
>  [out] Anzahl der **UPREADE-Einträge.** 
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[UPREADE](upreade.md)

