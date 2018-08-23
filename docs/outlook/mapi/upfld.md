---
title: UPFLD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da9d6b6-a016-ccef-77da-3e037c30450d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 34d6eb0653c3eb550bf03242a2c1b2acc3330a13
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572291"
---
# <a name="upfld"></a>UPFLD

**Betrifft**: Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>Elemente

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

- [Informationen über die Replikations-API](about-the-replication-api.md) 
- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
- [MAPI-Konstanten](mapi-constants.md)

