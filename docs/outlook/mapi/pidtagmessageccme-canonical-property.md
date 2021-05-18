---
title: PidTagMessageCcMe (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageCcMe
api_type:
- HeaderDef
ms.assetid: 7310a0f2-a109-40a4-99bf-e963d754a067
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7605739dd6d0f0205a1a4f09eb8c45d235c0c179
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329736"
---
# <a name="pidtagmessageccme-canonical-property"></a>PidTagMessageCcMe (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn dieser Messagingbenutzer ausdrücklich als Cc(Carbon Copy)-Empfänger dieser Nachricht bezeichnet wird und nicht Teil einer Verteilerliste ist. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MESSAGE_CC_ME  <br/> |
|Kennung:  <br/> |0x0058  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft bietet eine bequeme Möglichkeit, um zu bestimmen, ob der Benutzername explizit in der Empfängerliste für die Kopie einer Kopie angezeigt wird, ohne alle Einträge in der Liste zu untersuchen. 
  
Diese Eigenschaft hilft auch bei der automatisierten Behandlung von empfangenen Nachrichten zum Zeitpunkt des Empfangs. Auf Die Option des Transportanbieters enthält diese Eigenschaft entweder FALSE oder ist nicht festgelegt, wenn der Messagingbenutzer nicht direkt in der Empfängertabelle aufgeführt ist. 
  
Die Nachrichtenzustellung, die sich aus der Erweiterung der Verteilerliste oder einer Blindkopienbezeichnung ergibt, führt nicht dazu, dass diese Eigenschaft festgelegt wird. Der Empfänger muss explizit benannt werden. 
  
Nicht gesendete Nachrichten legen diese Eigenschaft in der Regel nicht **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) oder **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)). Wenn sie in Nachrichten vorhanden sind, auf die der Benutzer in öffentlichen Nachrichtenspeichern, in privaten Speichern anderer Benutzer, in Dateien auf dem Datenträger oder eingebettet in andere empfangene Nachrichten zugreifen kann, enthalten sie in der Regel die Werte, auf die sie beim letzten Senden der Nachricht durch einen Transportanbieter festgelegt wurden. 
  
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

