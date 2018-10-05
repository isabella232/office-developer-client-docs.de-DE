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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389771"
---
# <a name="pidtagmessageccme-canonical-property"></a>PidTagMessageCcMe (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält True, wenn dieser Benutzer messaging speziell als Kopie (CC) Empfänger dieser Nachricht heißt und nicht Bestandteil einer Verteilerliste ist. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MESSAGE_CC_ME  <br/> |
|Kennung:  <br/> |0x0058  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Allgemeine messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft bietet eine bequeme Möglichkeit zum bestimmen, ob der Benutzername in der Empfängerliste Carbon Copy, Blindkopie, explizit angezeigt wird, ohne Betrachtung der alle Einträge in der Liste. 
  
Diese Eigenschaft unterstützt Sie auch automatisierte Verarbeitung von erhaltenen Nachrichten zum Zeitpunkt des Eingangs. Unter der Adressbuchhierarchie verwenden wird, diese Eigenschaft enthält FALSE oder ist nicht festgelegt, wenn der messaging-Benutzer nicht direkt in der Empfänger Tabelle aufgeführt ist. 
  
Nachrichtenübermittlung entsteht Verteilerlistenerweiterung oder eine Bezeichnung blind Carbon Copy, Blindkopie bewirkt keine diese Eigenschaft festgelegt werden soll. Der Empfänger muss explizit heißen. 
  
Nicht gesendete Nachrichten führen Sie diese Eigenschaft, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) oder **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)) in der Regel nicht festlegen. Wenn sie in der Benutzer kann in öffentliche Nachrichtenspeichern, in der anderen Benutzer privaten Speicher, in den Dateien auf dem Datenträger, zugreifen oder in anderen empfangenen Nachrichten eingebettet, sie in der Regel die Werte, die festgelegt wurden, enthalten Nachrichten vorhanden sind der letzten Ausführung ein Transportdienstes übermittelt die Nachricht an. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

