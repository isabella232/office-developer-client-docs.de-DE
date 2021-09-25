---
title: MAPIOFFLINE_CREATEINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 539aa31d-7dec-4dbb-93f7-fa060c43565a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9e31e4c1f81541bcc04bfc41209f2ac5f8ea4f42
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592102"
---
# <a name="mapioffline_createinfo"></a>MAPIOFFLINE_CREATEINFO

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>Members

 **ulSize**
  
> Die Größe der Struktur.
    
 **ulCreateFlags**
  
> Es muss 0 sein.
    
 **pwszProfileName**
  
> Der Name des Profils.
    
 **ulCapabilities**
  
> Eine Bitmaske der folgenden Funktionsflags.
    
|||
|:-----|:-----|
|MAPIOFFLINE_CAPABILITY_OFFLINE  <br/> |Das Offlineobjekt kann offline geschaltet werden.  <br/> |
|MAPIOFFLINE_CAPABILITY_ONLINE  <br/> |Das Offlineobjekt kann online gehen.  <br/> |
   
 **pGUID**
  
> Zeiger auf eine GUID, die verwendet wird, um diesen Typ von Offlineobjekten aus anderen Offlineobjekten eindeutig zu identifizieren. GUID_GlobalState bezieht sich auf das globale Offlineobjekt, das objekte als übergeordnetes Objekt verwenden können.
    
 **pInstance**
  
> Zeiger auf guid, die dieses Offlineobjekt eindeutig identifiziert. Es wird verwendet, um diese Offlineobjekte von anderen Objekten zu unterscheiden.
    
 **pParent**
  
> Zeiger auf das Offlineobjekt, das das übergeordnete Objekt dieses Offlineobjekts ist und dessen Änderungen dieses Offlineobjekts erben.
    
 **pMAPISupport**
  
>  Identifies the MAPI support object that will use this offline object. Wenn dieses Offlineobjekt beispielsweise verwendet wird, um den Offline- und Onlinestatus eines Stores nachzuverfolgen, ist dies das Store-Supportobjekt. Wenn es sich jedoch um ein Offlineobjekt für ein Objekt ohne Unterstützungsobjekt handelt, kann es NULL sein. 
    
 **pAggregateInfo**
  
> Ein Zeiger auf eine MAPIOFFLINE_AGGREGATEINFO Struktur. Weitere Informationen finden Sie unter [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).
    
 **pConnectInfo**
  
> Muss NULL sein.
    
## <a name="see-also"></a>Siehe auch



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md)

