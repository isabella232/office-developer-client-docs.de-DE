---
title: PidTagMessageRecipientMe (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipientMe
api_type:
- HeaderDef
ms.assetid: 90333258-8913-4f98-aefb-4cc2ab34abcf
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 78423e874becdfc232b0dd964b32ae0c4530d19e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325620"
---
# <a name="pidtagmessagerecipientme-canonical-property"></a>PidTagMessageRecipientMe (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn dieser Messagingbenutzer speziell als Primärempfänger (An), Als Carbon Copy (CC) oder Blind Carbon Copy (BCC)-Empfänger dieser Nachricht bezeichnet wird und nicht Teil einer Verteilerliste ist. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MESSAGE_RECIP_ME  <br/> |
|Kennung:  <br/> |0x0059  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft bietet eine bequeme Möglichkeit, um zu bestimmen, ob der Benutzername explizit in der Empfängerliste angezeigt wird, ohne alle Einträge in der Liste zu untersuchen. Der Wert stellt den logischen **#A0** der Eigenschaften **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) und **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)) und der BCC-Informationen (die andernfalls nicht in einer Eigenschaft angezeigt werden) dar. 
  
Diese Eigenschaft unterstützt die automatisierte Verarbeitung von empfangenen Nachrichten zum Zeitpunkt des Empfangs. Bei der Option des Transportanbieters enthält diese Eigenschaft entweder FALSE oder ist nicht enthalten, wenn der Messagingbenutzer nicht direkt in der Empfängertabelle aufgeführt ist. 
  
Die Nachrichtenzustellung, die aus der Erweiterung der Verteilerliste resultiert, führt nicht dazu, dass diese Eigenschaft festgelegt wird. Der Empfänger muss explizit benannt werden. 
  
Nicht gesendete Nachrichten legen diese **Eigenschaft,** PR_MESSAGE_CC_ME oder **PR_MESSAGE_TO_ME.** Wenn sie in Nachrichten vorhanden sind, auf die der Benutzer in öffentlichen Nachrichtenspeichern, in privaten Speichern anderer Benutzer, in Dateien auf dem Datenträger oder eingebettet in andere empfangene Nachrichten zugreifen kann, enthalten sie in der Regel die Werte, auf die sie beim letzten Senden der Nachricht durch einen Transportanbieter festgelegt wurden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

