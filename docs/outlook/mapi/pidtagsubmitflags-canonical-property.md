---
title: PidTagSubmitFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubmitFlags
api_type:
- COM
ms.assetid: 9ea1c029-d53c-4c28-b413-560083b6215a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fb048d622aaf3cfa97f380e21324749d7421603e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563688"
---
# <a name="pidtagsubmitflags-canonical-property"></a>PidTagSubmitFlags (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske aus Flags, die Details zu einer Nachrichtenübermittlung angibt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SUBMIT_FLAGS  <br/> |
|Kennung:  <br/> |0x0E14  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI Übertragungseinehit  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Für die Bitmaske **PR_SUBMIT_FLAGS** kann eine oder mehrere der folgenden Werte festgelegt werden: 
  
SUBMITFLAG_LOCKED 
  
> Die MAPI-Warteschlange hat derzeit die Nachricht gesperrt. 
    
SUBMITFLAG_PREPROCESS 
  
> Die Meldung erforderlich vorverarbeitung. Wenn die MAPI-Warteschlange erfolgt vorverarbeitung diese Meldung, sollten sie die [IMessage::SubmitMessage](imessage-submitmessage.md) -Methode aufrufen. Die Nachrichtenanbieter erkennt, dass die Warteschlange, statt die Clientanwendung **SubmitMessage**aufgerufen hat, das Flag löscht und weiterhin-Nachrichtenübermittlung.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[IMsgStore::SetLockState](imsgstore-setlockstate.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

