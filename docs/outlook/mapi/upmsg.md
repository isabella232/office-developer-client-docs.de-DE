---
title: UPMSG
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5fe3956b-819a-3edf-0e49-7a44bcfbabcd
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e281907931a493e82c44913a7c26f6df55876e70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795816"
---
# <a name="upmsg"></a>UPMSG

**Betrifft**: Outlook 
  
Informationen zum Hochladen eines Outlook-Elements während der [Nachrichtenstatus hochladen](upload-message-state.md).
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct UPMSG 
{ 
    ULONG ulFlags; 
    LPMESSAGE pmsg; 
    MEID meid; 
    SBinary binReserved1; 
    SBinary binReserved2; 
    FEID feid; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeySrc; 
};
```

## <a name="members"></a>Elemente

 _ulFlags_
  
> [Out] / [in] Flags, die entsprechende Verhalten beim Hochladen zu bestimmen. 
    
  - UPM_ASSOC
    
    - [out] Element ist verknüpft.
    
  - UPM_NEW
    
    - [out] Neues Element. 
    
  - UPM_MOV
    
    - [out] Element wurde hier verschoben.
    
  - UPM_MOD_PROPS
    
    - [out] Elementeigenschaften wurden geändert.
    
  - UPM_HEADER
    
    - [out] Item ist ein Nachrichtenkopf.
    
  - UPM_OK
    
    - [in] Der Upload war erfolgreich. Der Client legt dies nach dem Hochladen von Informationen an den Server.
    
  - UPM_MOVED
    
    - [in] Element wurde erfolgreich verschoben.
    
  - UPM_COMMIT
    
    - [in] Upload-Status jetzt Commit ausgeführt werden.
    
  - UPM_DELETE
    
    - [in] Jetzt löschen Sie Element.
    
  - UPM_SAVE
    
    - [in] Speichern Sie Änderungen an das Element an.
    
_pmsg_
  
> [out] Open Item-Objekts. Finden Sie unter mapidefs.h für die Definition des **LPMESSAGE**Typs. 
    
_meid_
  
> [out] Die EntryID des Elements.
    
_binReserved1_
  
> [in] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_binReserved2_
  
> [in] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_feid_
  
> [out] Eintrags-ID des Quellordners, wenn das Element verschoben wurde.
    
_binChg_
  
> [out] Ändern Sie Schlüssel des Elements Ziel, wenn das Element verschoben wurde. Finden Sie unter mapidefs.h für die Definition des **SBinary**Typs. 
    
_binPcl_
  
> [out] Ändern Sie Liste des Elements Ziel, wenn das Element verschoben wurde. Finden Sie unter mapidefs.h für die Definition des **SBinary**Typs. 
    
_skeySrc_
  
> [out] Schlüssel Source des Quellelements, wenn das Element verschoben wurde.
    
## <a name="see-also"></a>Siehe auch

- [Informationen über die Replikations-API](about-the-replication-api.md)
- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
- [MAPI-Konstanten](mapi-constants.md)
- [FEID](feid.md)
- [MEID](meid.md)
- [SKEY](skey.md)

