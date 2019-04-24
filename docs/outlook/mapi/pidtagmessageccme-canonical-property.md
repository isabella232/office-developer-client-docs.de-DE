---
title: Kanonische PidTagMessageCcMe-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7605739dd6d0f0205a1a4f09eb8c45d235c0c179
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329736"
---
# <a name="pidtagmessageccme-canonical-property"></a>Kanonische PidTagMessageCcMe-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn dieser Messagingbenutzer ausdrücklich als CC-Empfänger dieser Nachricht benannt wurde und nicht Teil einer Verteilerliste ist. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MESSAGE_CC_ME  <br/> |
|Kennung:  <br/> |0x0058  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Allgemeine Nachrichtenübermittlung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft stellt eine bequeme Möglichkeit dar, um zu bestimmen, ob der Benutzername explizit in der Liste für den Carbon Copy-Empfänger angezeigt wird, ohne alle Einträge in der Liste zu überprüfen. 
  
Diese Eigenschaft unterstützt auch die automatisierte Behandlung von empfangenen Nachrichten zum Zeitpunkt des Empfangs. Bei der Option des Transportanbieters enthält diese Eigenschaft entweder FALSE oder wird nicht festgelegt, wenn der Messagingbenutzer nicht direkt in der Empfängertabelle aufgeführt ist. 
  
Durch die Nachrichtenübermittlung aufgrund der Erweiterung der Verteilerliste oder durch eine Blindkopie-Bezeichnung wird diese Eigenschaft nicht festgelegt. Der Empfänger muss explizit benannt werden. 
  
Nicht gesendete Nachrichten legen diese Eigenschaft im Allgemeinen nicht fest, **PR_MESSAGE_RECIP_ME** ([Pidtagmessagerecipientme (](pidtagmessagerecipientme-canonical-property.md)) oder **PR_MESSAGE_TO_ME** ([pidtagmessagetome (](pidtagmessagetome-canonical-property.md)). Wenn Sie in Nachrichten vorhanden sind, die der Benutzer in öffentlichen Nachrichten speichern, in privaten Speichern anderer Benutzer, in Dateien auf dem Datenträger oder in andere empfangene Nachrichten einbetten kann, enthalten Sie in der Regel die Werte, für die Sie den letzten Zeitpunkt festgelegt wurden, die Nachricht wurde übermittelt. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

