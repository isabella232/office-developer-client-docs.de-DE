---
title: Kanonische Pidtagreplyrecipiententries (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReplyRecipientEntries
api_type:
- COM
ms.assetid: a903fd22-a3f2-464f-99b0-c087e211b124
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 000132f052abb666ae844ec7d21b59c85ab43613
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355055"
---
# <a name="pidtagreplyrecipiententries-canonical-property"></a>Kanonische Pidtagreplyrecipiententries (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein großes Array von Eintrags Bezeichnern für Empfänger, die eine Antwort erhalten sollen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_REPLY_RECIPIENT_ENTRIES  <br/> |
|Kennung:  <br/> |0x004F  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Umschlag  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft enthält eine [FLATENTRYLIST](flatentrylist.md) -Struktur und ist keine mehrwertige Eigenschaft. 
  
Wenn diese Eigenschaft nicht vorhanden ist, wird eine Antwort nur an den Benutzer gesendet, der von der **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))-Eigenschaft identifiziert wird. Wenn diese und die **PR_REPLY_RECIPIENT_NAMES** ([pidtagreplyrecipientnames (](pidtagreplyrecipientnames-canonical-property.md))-Eigenschaft definiert sind, wird die Antwort an alle Empfänger gesendet, die von diesen beiden Eigenschaften identifiziert werden. Ein Transportanbieter verwendet diese Eigenschaften, um die übliche Antwort Logik außer Kraft zu setzen.
  
Wenn diese Eigenschaft oder die **PR_REPLY_RECIPIENT_NAMES** -Eigenschaft festgelegt ist, muss auch die andere Eigenschaft festgelegt werden. Diese Eigenschaften müssen dieselbe Anzahl von Empfängern enthalten, und Sie müssen diese in derselben Reihenfolge enthalten. Die Nichteinhaltung dieser Anforderungen kann zu unvorhersehbaren Ergebnissen führen. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichten zulässig sind.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internet Standard-e-Mail-Konventionen in Nachrichtenobjekte.
    
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

