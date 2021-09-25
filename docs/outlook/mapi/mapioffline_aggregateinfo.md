---
title: MAPIOFFLINE_AGGREGATEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2e502d28-ae09-49d9-a35a-5d77acdcd6f4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: df8b5dd061613b75627e6c1c9208efb81a531cdd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616754"
---
# <a name="mapioffline_aggregateinfo"></a>MAPIOFFLINE_AGGREGATEINFO

  
  
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
  
> Ein Zeiger auf das IUnknown-Objekt, auf dem dieses Objekt aggregiert wird. Dadurch können alle QueryInterface-Aufrufe an das erstellte Objekt übergeben werden.
    
 **pRefTrackRoot**
  
> Muss NULL sein.
    
## <a name="see-also"></a>Siehe auch



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_CREATEINFO](mapioffline_createinfo.md)

