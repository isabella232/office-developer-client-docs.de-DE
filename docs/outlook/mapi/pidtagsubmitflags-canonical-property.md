---
title: PidTagSubmitFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagSubmitFlags
api_type:
- COM
ms.assetid: 9ea1c029-d53c-4c28-b413-560083b6215a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 90a3807a4dd5edc5a0a18baebbc9754bd35ea1fc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624426"
---
# <a name="pidtagsubmitflags-canonical-property"></a>PidTagSubmitFlags (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske mit Flags, die Details zu einer Nachrichtenübermittlung angeben.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SUBMIT_FLAGS  <br/> |
|Kennung:  <br/> |0x0E14  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI nicht datenübertragungsfähig  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Mindestens eines der folgenden Flags kann für die **PR_SUBMIT_FLAGS** Bitmaske festgelegt werden: 
  
SUBMITFLAG_LOCKED 
  
> Für den MAPI-Spooler ist die Nachricht derzeit gesperrt. 
    
SUBMITFLAG_PREPROCESS 
  
> Die Nachricht muss vorverarbeitet werden. Wenn der MAPI-Spooler die Vorverarbeitung dieser Nachricht abgeschlossen hat, sollte die [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) aufgerufen werden. Der Nachrichtenspeicheranbieter erkennt, dass der Spooler anstelle der Clientanwendung **SubmitMessage** aufgerufen hat, löscht das Flag und setzt die Nachrichtenübermittlung fort.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[IMsgStore::SetLockState](imsgstore-setlockstate.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

