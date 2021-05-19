---
title: HDRSYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bf6892d0-a923-e926-5361-59efa49ebdc0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2131197ca24804eec74270100fa70c05c47a27cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410252"
---
# <a name="hdrsync"></a>HDRSYNC

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Informationen zum Synchronisieren eines Nachrichtenkopfs während des [Status der Downloadnachrichtkopfzeile](download-message-header-state.md).
  
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

## <a name="members"></a>Elemente

 _pupmsg_
  
- [out] Informationen für den aktuellen Nachrichtenkopf im lokalen Speicher.
    
 _feidPar_
  
- [out] Eintrags-ID für den übergeordneten Ordner des Nachrichtenelements.
    
 _pstmReserved_
  
- [out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt. 
    
 _ulFlags_
  
- [in] Flags zum Ändern des Verhaltens:
    
- HSF_LOCAL
    
  - [in] Das vollständige Element befindet sich im gleichen lokalen Speicher wie das Kopfzeilenelement.
    
- HSF_COPYDESTRUCTIVE
    
  -  [in] Optimieren sie interne Kopiervorgänge. Dies kann zu Datenverlusten führen. **HSF_LOCAL** muss festgelegt werden. 
    
- HSF_OK
    
  - [in] Die Kopfzeilensynchronisierung war erfolgreich. Der Client legt dies nach dem Herunterladen von Informationen vom Server fest.
    
     _pmsgFull_
    
  - [in] Das vollständige Nachrichtenelement einschließlich des Nachrichtenkopfs, der vom Server heruntergeladen wurde. Die Typdefinition von **LPMESSAGE** finden Sie unter mapidefs.h. 
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[FEID](feid.md)

