---
title: PidTagReceivedRepresentingEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagReceivedRepresentingEntryId
api_type:
- COM
ms.assetid: 2ae2266c-f093-41e5-b4d0-e12aa0f03190
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 10560c78854f03fb7a408b74f51031bd18bf88db
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616397"
---
# <a name="pidtagreceivedrepresentingentryid-canonical-property"></a>PidTagReceivedRepresentingEntryId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Eintragsbezeichner für den Messagingbenutzer, der vom empfangenden Benutzer dargestellt wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RCVD_REPRESENTING_ENTRYID  <br/> |
|Kennung:  <br/> |0x0043  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Adresse  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist eine der Adresseigenschaften für den Messagingbenutzer, der vom empfangenden Benutzer dargestellt wird. Sie muss vom anbieter für eingehenden Transport festgelegt werden, der auch für die Autorisierung oder Überprüfung des Stellvertreters verantwortlich ist. Wenn kein Messagingbenutzer dargestellt wird, sollte diese Eigenschaft auf den Eintragsbezeichner festgelegt werden, der in der **eigenschaft PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)) enthalten ist.
  
Eine Clientanwendung, die auf eine Nachricht antwortet, die im Auftrag eines anderen Clients empfangen wurde, sollte diese Eigenschaft aus der empfangenen Nachricht in die **Eigenschaft PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) für die Antwort kopieren.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Gibt Methoden zum Verbinden mit und Konfigurieren von Postfächern als Stellvertretungen und Interaktionen mit Nachrichten- und Kalenderobjekten an, wenn sie im Auftrag eines anderen Benutzers handeln.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

