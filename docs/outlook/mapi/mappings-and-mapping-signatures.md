---
title: Zuordnungen und Zuordnung Signaturen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 773f6671-cc21-4d1f-a11d-308bc71c852d
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 16f192ae816aba2dd0e34a42fba211c3ef70ba47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793165"
---
# <a name="mappings-and-mapping-signatures"></a>Zuordnungen und Zuordnung Signaturen

  
  
**Betrifft**: Outlook 
  
Bei ein Dienstanbieter benannte Eigenschaften unterstützt, wird jeder Gruppe von-ID und Name-Paare als eine Zuordnung bezeichnet. Dienstanbieter können eine Zuordnung eines oder mehrere unterstützen. Dass wird eine Nachricht Speicheranbieter, z. B., können die Methoden **GetIDsFromNames** und **GetNamesFromIDs** für alle seine Nachricht, Ordner und Message Store Objekte arbeiten mit einer einzelnen Liste mit Namen und ihren entsprechenden IDs implementieren. Eine andere Nachricht Speicheranbieter möglicherweise haben eine Liste für jeden Ordner und die darin enthaltenen Nachrichten oder eine eindeutige Liste für jede Nachricht und jeder Ordner implementieren. Nachricht-Anbieter, die eine eindeutige Zuordnung für jede Nachricht verwenden darf keine benannte Eigenschaften in ihren Ordner Inhalt Tabellen angezeigt werden, da für einen bestimmten Eigenschaftennamen, der Bezeichner für die Nachricht zu Nachricht unterscheiden sich zulassen. MAPI empfiehlt, dass der Anbieter ganz einfach und Arbeiten mit einer einzelnen Liste für alle ihre Objekte, einschließlich Tabellen. 
  
Für jede Zuordnung müssen Dienstanbieter eine Zuordnung Signatur angeben. Eine Signatur Zuordnung ist ein Binärwert, in der Regel eine GUID, die eine Reihe von eigenschaftskennungen und ihre entsprechenden Namen eindeutig identifiziert. Zuordnung Signaturen werden in der Eigenschaft eines Objekts **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) gespeichert. Dienstanbieter müssen ändern Sie den Wert für die **PR_MAPPING_SIGNATURE** -Eigenschaft immer auf die Zuordnung, das es darstellt, eine Änderung vorgenommen wird. Beispielsweise muss **PR_MAPPING_SIGNATURE** aktualisiert werden, wenn eine neue-ID zugeordnet, einen Namen oder einen neuen Namen ist und Bezeichner-Paar wird hinzugefügt. 
  
Arbeiten mit der benannten Eigenschaft der Objekte Clients verwenden der Objekte **PR_MAPPING_SIGNATURE** Eigenschaften in Vergleiche und kopieren. Zum Vergleichen mit der Eigenschaft Bezeichner, die auf zwei Objekte gehören, Clients, die nicht mit Zuordnung Signaturen [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) für beide Objekte zum Abrufen der Names für jede der Bezeichner aufrufen müssen. Verwenden die Zuordnung Signaturen von Objekten kann dieses Anrufs unnötige rendern. Wenn zwei Objekte den gleichen Wert für ihre **PR_MAPPING_SIGNATURE** Eigenschaften aufweisen, verwenden sie die gleiche Zuordnung. Bezeichner, die die gleiche Zuordnung verwenden können direkt verglichen werden. Dienstanbieter, die die Implementierung [IMAPIProp::CopyTo](imapiprop-copyto.md) und [IMAPIProp::CopyProps](imapiprop-copyprops.md) können auch ein Objekt Zuordnung Signatur nutzen. Beim Kopieren zwischen Objekten Eigenschaften namens können Dienstanbieter den Konvertierungsschritt vermeiden, wenn die Quell- und Ziel-Objekte dieselbe Zuordnung Signatur aufweisen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp: IUnknown](imapipropiunknown.md)


[Benannte Eigenschaften MAPI](mapi-named-properties.md)

