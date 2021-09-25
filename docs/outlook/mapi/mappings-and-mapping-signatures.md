---
title: Zuordnungen und Zuordnungssignaturen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 773f6671-cc21-4d1f-a11d-308bc71c852d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: da1a4fe3027d4bf914e93c1000d37bb73e7875db
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595749"
---
# <a name="mappings-and-mapping-signatures"></a>Zuordnungen und Zuordnungssignaturen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn ein Dienstanbieter benannte Eigenschaften unterstützt, wird jede Gruppe von Bezeichner- und Namenspaaren als Zuordnung bezeichnet. Dienstanbieter können eine oder mehrere Zuordnungen unterstützen. Das heißt, ein Nachrichtenspeicheranbieter kann beispielsweise die **Methoden "GetIDsFromNames"** und **"GetNamesFromIDs"** für alle Nachrichten-, Ordner- und Nachrichtenspeicherobjekte implementieren, um mit einer einzigen Liste von Namen und den entsprechenden Bezeichnern zu arbeiten. Ein anderer Nachrichtenspeicheranbieter verfügt möglicherweise über eine Liste für jeden Ordner und die darin enthaltenen Nachrichten oder implementiert eine eindeutige Liste für jede Nachricht und jeden Ordner. Nachrichtenspeicheranbieter, die eine eindeutige Zuordnung für jede Nachricht verwenden, dürfen nicht zulassen, dass benannte Eigenschaften in ihren Ordnerinhaltstabellen angezeigt werden, da sich der Eigenschaftsbezeichner für einen bestimmten Eigenschaftsnamen von Nachricht zu Nachricht unterscheidet. MAPI empfiehlt Anbietern, dies einfach zu halten und mit einer einzigen Liste für alle ihre Objekte einschließlich Tabellen zu arbeiten. 
  
Für jede Zuordnung müssen Dienstanbieter eine Zuordnungssignatur angeben. Eine Zuordnungssignatur ist ein binärer Wert, in der Regel eine GUID, der einen Satz von Eigenschaftsbezeichnern und deren entsprechende Namen eindeutig identifiziert. Zuordnungssignaturen werden in der **PR_MAPPING_SIGNATURE** -[PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) -Eigenschaft eines Objekts gespeichert. Dienstanbieter müssen den Wert für ihre **PR_MAPPING_SIGNATURE** Eigenschaft ändern, wenn eine Änderung an der Zuordnung vorgenommen wird, die sie darstellt. Beispielsweise muss **PR_MAPPING_SIGNATURE** aktualisiert werden, wenn einem Namen ein neuer Bezeichner zugewiesen oder ein neues Name- und Bezeichnerpaar hinzugefügt wird. 
  
Clients, die mit den benannten Eigenschaften von Objekten arbeiten, verwenden die **PR_MAPPING_SIGNATURE** Eigenschaften der Objekte in Vergleichs- und Kopiervorgängen. Um benannte Eigenschaftsbezeichner zu vergleichen, die zu zwei Objekten gehören, müssen Clients, die keine Zuordnungssignaturen [verwenden, IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) für beide Objekte aufrufen, um die Namen für jeden bezeichner abzurufen. Die Verwendung der Zuordnungssignaturen von Objekten kann diesen Aufruf unnötig machen. Wenn zwei Objekte für ihre **PR_MAPPING_SIGNATURE** Eigenschaften denselben Wert haben, verwenden sie dieselbe Zuordnung. Bezeichner, die dieselbe Zuordnung verwenden, können direkt verglichen werden. Dienstanbieter, die [IMAPIProp::CopyTo](imapiprop-copyto.md) und [IMAPIProp::CopyProps](imapiprop-copyprops.md) implementieren, können auch die Zuordnungssignatur eines Objekts nutzen. Beim Kopieren benannter Eigenschaften zwischen Objekten können Dienstanbieter den Konvertierungsschritt vermeiden, wenn die Quell- und Zielobjekte die gleiche Zuordnungssignatur aufweisen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp : IUnknown](imapipropiunknown.md)


[Benannte Eigenschaften MAPI](mapi-named-properties.md)

