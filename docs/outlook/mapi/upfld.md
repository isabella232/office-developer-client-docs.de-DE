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
ms.openlocfilehash: c8f7bdc5864c049d8db6f38e92a69c97b6f9dc73
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431358"
---
# <a name="upfld"></a>UPFLD

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Informationen zum Hochladen eines Ordners während des [Upload-Ordner Status](upload-folder-state.md).
  
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
  
>  [out]/[in] Flags, um geeignete Aktionen für das Uplaod zu bestimmen. 
    
  - UPF_NEW
    
    - Out Folder ist neu.
    
  - UPF_MOD_PARENT
    
    - Out Der Ordner wurde verschoben.
    
  - UPF_MOD_PROPS
    
    - Out Die Ordner Eigenschaften wurden geändert.
    
  - UPF_DEL
    
    - Out Der Ordner wurde gelöscht.
    
  - UPF_OK
    
    - in Der Upload war erfolgreich. Der Client legt dies nach dem Hochladen von Ordnerinformationen auf den Server fest.
    
_pfld_
  
> Out Das geöffnete Folder-Objekt, das hochgeladen werden soll.
    
_feid_
  
> [out] Eintrags-ID des Ordners.
    
## <a name="see-also"></a>Siehe auch

- [Informationen über die Replikations-API](about-the-replication-api.md) 
- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
- [MAPI-Konstanten](mapi-constants.md)

