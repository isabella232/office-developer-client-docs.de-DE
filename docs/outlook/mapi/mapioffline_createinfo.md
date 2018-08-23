---
title: MAPIOFFLINE_CREATEINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 539aa31d-7dec-4dbb-93f7-fa060c43565a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ffac4328401b8afbc07eb650ea6c08da5f9c51b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594495"
---
# <a name="mapiofflinecreateinfo"></a>MAPIOFFLINE_CREATEINFO

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Diese Struktur wird mit [HrCreateOfflineObj](hrcreateofflineobj.md)verwendet.
  
```cpp
typedef struct
{
  ULONG      ulSize;
  ULONG      ulCreateFlags;
  LPCWSTR      pwszProfileName;
  ULONG      ulCapabilities;
  const GUID*      pGUID;
  const GUID*      pInstance;
  IMAPIOfflineMgr*    pParent;
  IUnknown*      pMAPISupport;
  MAPIOFFLINE_AGGREGATEINFO*  pAggregateInfo;
  MAPIOFFLINE_CONNECTINFO*  pConnectInfo;
} MAPIOFFLINE_CREATEINFO;
```

## <a name="members"></a>Elemente

 **ulSize**
  
> Die Größe der Struktur.
    
 **ulCreateFlags**
  
> Es muss 0 sein.
    
 **pwszProfileName**
  
> Der Name des Profils.
    
 **ulCapabilities**
  
> Eine Bitmaske der folgenden Funktion Flags.
    
|||
|:-----|:-----|
|MAPIOFFLINE_CAPABILITY_OFFLINE  <br/> |Das offline-Objekt kann Wechsel in den Offlinemodus.  <br/> |
|MAPIOFFLINE_CAPABILITY_ONLINE  <br/> |Das offline-Objekt kann den Onlinemodus wechseln.  <br/> |
   
 **pGUID**
  
> Zeiger auf eine GUID, die verwendet wird, um diese Art von offline-Objekt aus anderen offline-Objekten eindeutig zu identifizieren. GUID_GlobalState bezieht sich auf das globale offline-Objekt, das als ein übergeordnetes Objekt Objekte verwenden können.
    
 **pInstance**
  
> Zeiger auf die GUID, die dieses offline-Objekt eindeutig identifiziert. Es wird verwendet, um diese offline Objekte aus anderen Objekten zu unterscheiden.
    
 **pParent**
  
> Zeiger auf offline-Objekt, das das übergeordnete Element dieses Objekt offline und deren ist dieses offline-Objekt erbt die Änderungen.
    
 **pMAPISupport**
  
>  Gibt das MAPI-Support-Objekt, die dieses offline-Objekt verwendet werden. Wenn dieses Objekt offline um eines Speichers an offline verwendet wird und Onlinestatus, dies wird unterstützt die Speicher Objekt. Jedoch ist dies ein offline-Objekt für ein Objekt ohne Unterstützung-Objekt kann es NULL sein. 
    
 **pAggregateInfo**
  
> Ein Zeiger auf eine MAPIOFFLINE_AGGREGATEINFO-Struktur. Weitere Informationen finden Sie unter [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).
    
 **pConnectInfo**
  
> Muss null sein.
    
## <a name="see-also"></a>Siehe auch



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md)

