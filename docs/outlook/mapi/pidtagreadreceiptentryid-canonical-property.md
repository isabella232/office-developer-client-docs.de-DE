---
title: PidTagReadReceiptEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagReadReceiptEntryId
api_type:
- COM
ms.assetid: 141d49c8-87cf-4d80-a33b-ccbf3eeae19e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e0987f6cdbfcaf53c703ceab4009f4e9386573c6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587261"
---
# <a name="pidtagreadreceiptentryid-canonical-property"></a>PidTagReadReceiptEntryId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Eintragsbezeichner für den Messagingbenutzer, an den das Messagingsystem einen Lesebericht für diese Nachricht weiterleiten soll.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_READ_RECEIPT_ENTRYID  <br/> |
|Kennung:  <br/> |0x0046  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Umschlag  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft wird ignoriert, es sei denn, die **eigenschaft PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) ist auf TRUE festgelegt.
  
Wenn eine Clientanwendung selbst Leseberichte empfangen möchte, kann sie diese Eigenschaft nicht festlegen oder auf den Eintragsbezeichner festlegen, der in der **eigenschaft PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) zum Zeitpunkt der Nachrichtenübermittlung enthalten ist.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

