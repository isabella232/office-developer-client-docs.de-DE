---
title: HDRSYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bf6892d0-a923-e926-5361-59efa49ebdc0
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bd1c327eb2042957c8fb043736950af3dae520b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791827"
---
# <a name="hdrsync"></a>HDRSYNC

  
  
**Betrifft**: Outlook 
  
Informationen zum Synchronisieren von Nachrichtenkopfzeile während der [Status der Nachricht Kopfzeilen herunterladen](download-message-header-state.md).
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct HDRSYNC 
{ 
    UPMSG *pupmsg; 
    FEID feidPar; 
    LPSTREAM pstmReserved; 
    ULONG ulFlags; 
    LPMESSAGE pmsgFull; 
};
```

## <a name="members"></a>Members

 _pupmsg_
  
- [out] Informationen für die aktuelle Nachrichtenkopfzeile in den lokalen Speicher.
    
 _feidPar_
  
- [out] Eintrags-ID für den übergeordneten Ordner des Nachrichtenobjekts.
    
 _pstmReserved_
  
- [out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
 _ulFlags_
  
- [in] Flags, Verhalten zu ändern:
    
- HSF_LOCAL
    
  - [in] Vollständige Element befindet sich im gleichen lokalen Speicher als Headerelement.
    
- HSF_COPYDESTRUCTIVE
    
  -  [in] Interne Copy-Vorgänge zu optimieren. Dies kann zu Datenverlusten führen. **HSF_LOCAL** muss festgelegt werden. 
    
- HSF_OK
    
  - [in] Header-Synchronisierung war erfolgreich. Der Client legt dies nach dem Herunterladen von Informationen vom Server.
    
     _pmsgFull_
    
  - [in] Das vollständige e-Mail-Element mit der Kopfzeile, die vom Server heruntergeladen werden. Finden Sie unter mapidefs.h für die Definition des **LPMESSAGE**Typs. 
    
## <a name="see-also"></a>Siehe auch



[Über die API-Replikation](about-the-replication-api.md)
  
[Informationen zu den Replikationsstatus Computer](about-the-replication-state-machine.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[FEID](feid.md)

