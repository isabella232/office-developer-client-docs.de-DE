---
title: MAPIOFFLINE_AGGREGATEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2e502d28-ae09-49d9-a35a-5d77acdcd6f4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: eb182d9cc51c196558f9e9192a65352e87372bf0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582518"
---
# <a name="mapiofflineaggregateinfo"></a>MAPIOFFLINE_AGGREGATEINFO

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Die Struktur wird mit [HrCreateOfflineObj](hrcreateofflineobj.md)verwendet. 
  
```cpp
typedef struct
{
  ULONG            ulSize;
  IUnknown*          pOuterObj;
  IUnknown*          pRefTrackRoot;
} MAPIOFFLINE_AGGREGATEINFO;
```

## <a name="members"></a>Elemente

 **ulSize**
  
> Die Größe der Struktur.
    
 **pOuterObj**
  
> Ein Zeiger auf die IUnknown-Objekt, auf dem dieses Objekt gerade zusammengesetzt wird. Dadurch werden alle QueryInterface Anrufe über auf das erstellte Objekt zu übergeben.
    
 **pRefTrackRoot**
  
> NULL muss sein.
    
## <a name="see-also"></a>Siehe auch



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_CREATEINFO](mapioffline_createinfo.md)

