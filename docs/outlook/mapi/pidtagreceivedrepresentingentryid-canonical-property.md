---
title: PidTagReceivedRepresentingEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingEntryId
api_type:
- COM
ms.assetid: 2ae2266c-f093-41e5-b4d0-e12aa0f03190
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 33e41343e0c159be20ed1499fc24223947975e1d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359094"
---
# <a name="pidtagreceivedrepresentingentryid-canonical-property"></a>PidTagReceivedRepresentingEntryId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Eintrags-ID für den Messagingbenutzer, der vom empfangenden Benutzer dargestellt wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RCVD_REPRESENTING_ENTRYID  <br/> |
|Kennung:  <br/> |0x0043  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Adresse  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist eine der Adresseigenschaften für den Messagingbenutzer, der vom empfangenden Benutzer dargestellt wird. Sie muss vom eingehenden Transportanbieter festgelegt werden, der auch für die Autorisierung oder Überprüfung der Stellvertretung zuständig ist. Wenn kein Messagingbenutzer dargestellt wird, sollte diese Eigenschaft auf den Eintragsbezeichner festgelegt werden, der in der **PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)) -Eigenschaft enthalten ist.
  
Eine Clientanwendung, die auf eine Nachricht antwortet, die im Namen eines anderen Clients empfangen wurde, sollte diese Eigenschaft aus der empfangenen Nachricht in die **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) -Eigenschaft für die Antwort kopieren.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Gibt Methoden zum Verbinden und Konfigurieren von Postfächern als Stellvertretung sowie Interaktionen mit Nachrichten- und Kalenderobjekten an, wenn sie im Auftrag eines anderen Benutzers agieren.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

