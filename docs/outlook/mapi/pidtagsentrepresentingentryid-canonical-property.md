---
title: PidTagSentRepresentingEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagSentRepresentingEntryId
api_type:
- COM
ms.assetid: f23bde8b-94cc-48c8-891a-166aa39aa3ee
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4c9b33285594450f6714ee7b7c234498f6cdbc08
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591444"
---
# <a name="pidtagsentrepresentingentryid-canonical-property"></a>PidTagSentRepresentingEntryId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Eintragsbezeichner für den vom Absender dargestellten Messagingbenutzer.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SENT_REPRESENTING_ENTRYID  <br/> |
|Kennung:  <br/> |0x0041  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Adresse  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft ist eine der Adresseigenschaften für den Messagingbenutzer, der vom Absender dargestellt wird. Wenn eine Clientanwendung eine Nachricht im Auftrag eines anderen Clients sendet, sollte sie alle dargestellten Absendereigenschaften auf die Werte für diesen Client festlegen. Ein Messaging-Benutzer, der in seinem eigenen Auftrag sendet, lässt in der Regel die dargestellten Absendereigenschaften unet.
  
Der ausgehende Transportanbieter muss diese Eigenschaft immer unverändert lassen, wenn sie vom sendenden Client festgelegt wurde. Wenn es nicht festgelegt ist, sollte der Transportanbieter ihn auf **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) für die ausgehende Kopie der Nachricht festlegen und ihn in der lokalen Kopie nicht festlegen.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungsanfrage- und Antwortnachrichten an.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Gibt Methoden zum Verbinden mit und Konfigurieren von Postfächern als Stellvertretungen und Interaktionen mit Nachrichten- und Kalenderobjekten an, wenn sie im Auftrag eines anderen Benutzers handeln.
    
[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Post-Objekte zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[PidTagEntryId (kanonische Eigenschaft)](pidtagentryid-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

