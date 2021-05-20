---
title: UPMSG
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5fe3956b-819a-3edf-0e49-7a44bcfbabcd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1e0e2f9b794c4cee25488a754290922e58b7658d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427269"
---
# <a name="upmsg"></a>UPMSG

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Informationen zum Hochladen eines Outlook element während des [Status der Uploadnachricht](upload-message-state.md).
  
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
  
> [out]/[in] Flags, um das entsprechende Verhalten während des Uploads zu bestimmen. 
    
  - UPM_ASSOC
    
    - [out] Element ist zugeordnet.
    
  - UPM_NEW
    
    - [out] Neues Element. 
    
  - UPM_MOV
    
    - [out] Element wurde hier verschoben.
    
  - UPM_MOD_PROPS
    
    - [out] Elementeigenschaften wurden geändert.
    
  - UPM_HEADER
    
    - [out] Element ist eine Nachrichtenkopfzeile.
    
  - UPM_OK
    
    - [in] Hochladen war erfolgreich. Der Client legt dies nach dem Hochladen von Informationen auf den Server fest.
    
  - UPM_MOVED
    
    - [in] Element wurde erfolgreich verschoben.
    
  - UPM_COMMIT
    
    - [in] Commit-Uploadstatus jetzt.
    
  - UPM_DELETE
    
    - [in] Element jetzt löschen.
    
  - UPM_SAVE
    
    - [in] Speichern Sie Änderungen am Element.
    
_pmsg_
  
> [out] Öffnen Sie das Elementobjekt. Die Typdefinition von **LPMESSAGE** finden Sie unter mapidefs.h. 
    
_meid_
  
> [out] Eintrags-ID des Elements.
    
_binReserved1_
  
> [in] Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_binReserved2_
  
> [in] Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
_feid_
  
> [out] Eintrags-ID des Quellordners, wenn das Element verschoben wurde.
    
_binChg_
  
> [out] Ändern Sie den Schlüssel des Zielelements, wenn das Element verschoben wurde. Die Typdefinition von **SBinary** finden Sie unter mapidefs.h. 
    
_binPcl_
  
> [out] Ändern der Liste des Zielelements, wenn das Element verschoben wurde. Die Typdefinition von **SBinary** finden Sie unter mapidefs.h. 
    
_skeySrc_
  
> [out] Quellschlüssel des Quellelements, wenn das Element verschoben wurde.
    
## <a name="see-also"></a>Siehe auch

- [Informationen über die Replikations-API](about-the-replication-api.md)
- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
- [MAPI-Konstanten](mapi-constants.md)
- [FEID](feid.md)
- [MEID](meid.md)
- [SKEY](skey.md)

