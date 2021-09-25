---
title: PidTagReplyRecipientEntries (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagReplyRecipientEntries
api_type:
- COM
ms.assetid: a903fd22-a3f2-464f-99b0-c087e211b124
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b38207262fa97a368c8b993877c5694ed4c9d9be
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591612"
---
# <a name="pidtagreplyrecipiententries-canonical-property"></a>PidTagReplyRecipientEntries (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array mit Eintragsbezeichnern der Größe für Empfänger, die eine Antwort erhalten sollen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_REPLY_RECIPIENT_ENTRIES  <br/> |
|Kennung:  <br/> |0x004F  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Umschlag  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft enthält eine [FLATENTRYLIST-Struktur](flatentrylist.md) und ist keine mehrwertige Eigenschaft. 
  
Wenn diese Eigenschaft nicht vorhanden ist, wird eine Antwort nur an den Benutzer gesendet, der von der **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) -Eigenschaft identifiziert wird. Wenn diese und die **eigenschaften PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) definiert sind, wird die Antwort an alle empfänger gesendet, die von diesen beiden Eigenschaften identifiziert werden. Ein Transportanbieter verwendet diese Eigenschaften, um die übliche Antwortlogik zu überschreiben.
  
Wenn diese Eigenschaft oder die **PR_REPLY_RECIPIENT_NAMES-Eigenschaft** festgelegt ist, muss auch die andere Eigenschaft festgelegt werden. Diese Eigenschaften müssen dieselbe Anzahl von Empfängern enthalten, und sie müssen in derselben Reihenfolge enthalten sein. Wenn diese Anforderungen nicht beachtet werden, kann dies zu unvorhersehbaren Ergebnissen führen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichten zulässig sind.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.
    
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

