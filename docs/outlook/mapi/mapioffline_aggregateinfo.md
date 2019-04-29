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
ms.openlocfilehash: 4775de0707eb90549f07525e3aa54ec5842f6050
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438162"
---
# <a name="mapiofflineaggregateinfo"></a>MAPIOFFLINE_AGGREGATEINFO

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Struktur wird mit [HrCreateOfflineObj](hrcreateofflineobj.md)verwendet. 
  
```cpp
typedef struct
{
  ULONG            ulSize;
  IUnknown*          pOuterObj;
  IUnknown*          pRefTrackRoot;
} MAPIOFFLINE_AGGREGATEINFO;
```

## <a name="members"></a>Members

 **ulSize**
  
> Die Größe der Struktur.
    
 **pOuterObj**
  
> Ein Zeiger auf das IUnknown-Objekt, auf das dieses Objekt aggregiert wird. Dadurch können QueryInterface-Aufrufe an das erstellte Objekt weitergeleitet werden.
    
 **pRefTrackRoot**
  
> Muss NULL sein.
    
## <a name="see-also"></a>Siehe auch



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_CREATEINFO](mapioffline_createinfo.md)

