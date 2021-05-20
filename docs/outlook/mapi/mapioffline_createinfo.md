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
ms.openlocfilehash: a9b11b134f5d4a32a5a55008f557821d74b474bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429565"
---
# <a name="mapioffline_createinfo"></a>MAPIOFFLINE_CREATEINFO

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Diese Struktur wird mit [HrCreateOfflineObj verwendet.](hrcreateofflineobj.md)
  
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
  
> Eine Bitmaske der folgenden Funktionskennzeichen.
    
|||
|:-----|:-----|
|MAPIOFFLINE_CAPABILITY_OFFLINE  <br/> |Das Offlineobjekt kann offline gehen.  <br/> |
|MAPIOFFLINE_CAPABILITY_ONLINE  <br/> |Das Offlineobjekt kann online gehen.  <br/> |
   
 **pGUID**
  
> Zeiger auf eine GUID, mit der dieser Typ von Offlineobjekten von anderen Offlineobjekten eindeutig identifiziert wird. GUID_GlobalState bezieht sich auf das globale Offlineobjekt, das Objekte als übergeordnetes Objekt verwenden können.
    
 **pInstance**
  
> Zeiger auf GUID, die dieses Offlineobjekt eindeutig identifiziert. Es wird verwendet, um diese Offlineobjekte von anderen Objekten zu entfernen.
    
 **pParent**
  
> Zeiger auf ein Offlineobjekt, das das übergeordnete Objekt dieses Offlineobjekts ist und dessen Änderungen dieses Offlineobjekt erbt.
    
 **pMAPISupport**
  
>  Identifiziert das MAPI-Supportobjekt, das dieses Offlineobjekt verwendet. Wenn dieses Offlineobjekt beispielsweise verwendet wird, um den Offline- und Onlinestatus eines Speichers nachverfolgt zu werden, ist dies das Speicherunterstützungsobjekt. Wenn es sich jedoch um ein Offlineobjekt für ein Objekt ohne Supportobjekt handelt, kann es NULL sein. 
    
 **pAggregateInfo**
  
> Ein Zeiger auf eine MAPIOFFLINE_AGGREGATEINFO Struktur. Weitere Informationen finden Sie unter [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).
    
 **pConnectInfo**
  
> Muss null sein.
    
## <a name="see-also"></a>Siehe auch



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md)

