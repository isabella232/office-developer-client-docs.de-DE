---
title: UPFLD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da9d6b6-a016-ccef-77da-3e037c30450d
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f25b3fb967f4ed93ac38487f21145f35413764da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795799"
---
# <a name="upfld"></a>UPFLD

**Betrifft**: Outlook 
  
Informationen zum Hochladen eines Ordners während der [Zustand Ordner hochladen](upload-folder-state.md).
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct UPFLD 
{ 
    ULONG ulFlags; 
    LPMAPIFOLDER pfld; 
    FEID feid; 
}; 

```

## <a name="members"></a>Members

_ulFlags_
  
>  [Out] / [in] Flags an, die entsprechende Aktionen für die Uplaod bestimmen. 
    
  - UPF_NEW
    
    - [out] Ordner ist neu.
    
  - UPF_MOD_PARENT
    
    - [out] Ordner wurde verschoben.
    
  - UPF_MOD_PROPS
    
    - [out] Ordnereigenschaften wurden geändert.
    
  - UPF_DEL
    
    - [out] Ordner wurde gelöscht.
    
  - UPF_OK
    
    - [in] Der Upload war erfolgreich. Der Client legt dies nach dem Hochladen der Ordnerinformationen an den Server.
    
_pfld_
  
> [out] Hochladen open Folder-Objekts.
    
_feid_
  
> [out] Die EntryID des Ordners.
    
## <a name="see-also"></a>Siehe auch

- [Über die API-Replikation](about-the-replication-api.md) 
- [Informationen zu den Replikationsstatus Computer](about-the-replication-state-machine.md)
- [MAPI-Konstanten](mapi-constants.md)

