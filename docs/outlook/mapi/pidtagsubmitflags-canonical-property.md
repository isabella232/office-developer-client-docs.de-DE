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
ms.openlocfilehash: ca31aece48236227a03d8e2114f8af4b127b8f90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339354"
---
# <a name="pidtagsubmitflags-canonical-property"></a>PidTagSubmitFlags (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske mit Flags, die Details zu einer Nachrichtenübermittlung angibt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SUBMIT_FLAGS  <br/> |
|Kennung:  <br/> |0x0E14  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI nicht durchlässig  <br/> |
   
## <a name="remarks"></a>Hinweise

Mindestens eines der folgenden Flags kann für die PR_SUBMIT_FLAGS **festgelegt** werden: 
  
SUBMITFLAG_LOCKED 
  
> Im MAPI-Spooler ist die Nachricht derzeit gesperrt. 
    
SUBMITFLAG_PREPROCESS 
  
> Die Nachricht muss vorverarbeitet werden. Wenn der MAPI-Spooler diese Nachricht vorverarbeitet hat, sollte er die [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) aufrufen. Der Nachrichtenspeicheranbieter erkennt, dass der Spooler anstelle der Clientanwendung **SubmitMessage** aufgerufen hat, das Flag entfernt und die Nachrichtenübermittlung fortgesetzt wird.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[IMsgStore::SetLockState](imsgstore-setlockstate.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

