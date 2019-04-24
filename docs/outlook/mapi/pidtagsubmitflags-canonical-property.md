---
title: Kanonische Pidtagsubmitflags (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ca31aece48236227a03d8e2114f8af4b127b8f90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339354"
---
# <a name="pidtagsubmitflags-canonical-property"></a>Kanonische Pidtagsubmitflags (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske von Flags, die Details zu einer Nachrichtenübermittlung angeben.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SUBMIT_FLAGS  <br/> |
|Kennung:  <br/> |0x0E14  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Nicht transmitable MAPI  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Eine oder mehrere der folgenden Flags können für die **PR_SUBMIT_FLAGS** -Bitmaske festgelegt werden: 
  
SUBMITFLAG_LOCKED 
  
> Der MAPI-Spooler hat die Nachricht derzeit gesperrt. 
    
SUBMITFLAG_PREPROCESS 
  
> Die Nachricht benötigt eine Vorverarbeitung. Wenn die MAPI-Warteschlange die Vorverarbeitung dieser Nachricht abgeschlossen hat, sollte Sie die [IMessage:: SubmitMessage](imessage-submitmessage.md) -Methode aufrufen. Der Nachrichtenspeicher Anbieter erkennt, dass der Spooler anstelle der Clientanwendung **SubmitMessage**aufgerufen hat, löscht das Flag und setzt die Nachrichtenübermittlung fort.
    
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Konvertiert zwischen IETF-RFC2445, RFC2446 und RFC2447 sowie Termin-und Besprechungs Objekten.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[IMsgStore::SetLockState](imsgstore-setlockstate.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

