---
title: Kanonische Pidtagreplyrecipientnames (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReplyRecipientNames
api_type:
- COM
ms.assetid: f5ae6124-3e44-400f-95c2-24b19f3085b5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 02dcbcccd003fb0b53356da11a3b90b38e632c2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355174"
---
# <a name="pidtagreplyrecipientnames-canonical-property"></a>Kanonische Pidtagreplyrecipientnames (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Liste von Anzeigenamen für Empfänger, die eine Antwort erhalten sollen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_REPLY_RECIPIENT_NAMES, PR_REPLY_RECIPIENT_NAMES_A, PR_REPLY_RECIPIENT_NAMES_W  <br/> |
|Kennung:  <br/> |0x0050  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Umschlag  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften enthalten die Anzeige Namen, die durch Semikolons getrennt sind.
  
Wenn diese Eigenschaft nicht vorhanden ist, wird eine Antwort nur an den Benutzer gesendet, der von der **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))-Eigenschaft identifiziert wird. Wenn **PR_REPLY_RECIPIENT_ENTRIES** ([pidtagreplyrecipiententries (](pidtagreplyrecipiententries-canonical-property.md)) und diese Eigenschaften definiert sind, wird die Antwort an alle Empfänger gesendet, die von diesen beiden Eigenschaften identifiziert werden. Ein Transportanbieter verwendet diese Eigenschaften, um die übliche Antwort Logik außer Kraft zu setzen.
  
Wenn entweder **PR_REPLY_RECIPIENT_ENTRIES** oder diese Eigenschaften festgelegt sind, muss auch die andere Eigenschaft festgelegt werden. Diese Eigenschaften müssen dieselbe Anzahl von Empfängern enthalten, und Sie müssen diese in derselben Reihenfolge enthalten. Die Nichteinhaltung dieser Anforderungen kann zu unvorhersehbaren Ergebnissen führen. 
  
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

