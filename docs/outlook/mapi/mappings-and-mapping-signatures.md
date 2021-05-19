---
title: Zuordnungen und Zuordnungssignaturen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 773f6671-cc21-4d1f-a11d-308bc71c852d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cd26ce4bc2da3da639b4a611fc9a69f39b13e5f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410014"
---
# <a name="mappings-and-mapping-signatures"></a>Zuordnungen und Zuordnungssignaturen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn ein Dienstanbieter benannte Eigenschaften unterstützt, wird jeder Satz von Bezeichner- und Namenpaaren als Zuordnung bezeichnet. Dienstanbieter können eine oder mehrere Zuordnungen unterstützen. Das heißt, ein Nachrichtenspeicheranbieter kann beispielsweise die **Methoden GetIDsFromNames** und **GetNamesFromIDs** für alle seine Nachrichten-, Ordner- und Nachrichtenspeicherobjekte implementieren, um mit einer einzelnen Liste von Namen und den entsprechenden Bezeichnern zu arbeiten. Ein anderer Nachrichtenspeicheranbieter kann über eine Liste für jeden Ordner und die darin enthaltenen Nachrichten verfügen oder eine eindeutige Liste für jede Nachricht und jeden Ordner implementieren. Nachrichtenspeicheranbieter, die eine eindeutige Zuordnung für jede Nachricht verwenden, dürfen nicht zulassen, dass benannte Eigenschaften in ihren Ordnerinhaltstabellen angezeigt werden, da bei einem angegebenen Eigenschaftennamen der Eigenschaftenbezeichner von Nachricht zu Nachricht unterschiedlich ist. MAPI empfiehlt, dass Anbieter dies einfach halten und mit einer einzigen Liste für alle ihre Objekte einschließlich Tabellen arbeiten. 
  
Für jede Zuordnung müssen Dienstanbieter eine Zuordnungssignatur liefern. Eine Zuordnungssignatur ist ein binärer Wert, in der Regel eine GUID, die eine Reihe von Eigenschaftenbezeichnern und deren entsprechenden Namen eindeutig identifiziert. Zuordnungssignaturen werden in der eigenschaft **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) eines Objekts gespeichert. Dienstanbieter müssen den Wert für ihre PR_MAPPING_SIGNATURE **ändern,** wenn eine Änderung an der zuordnung vorgenommen wird, die sie darstellt. Beispielsweise muss **PR_MAPPING_SIGNATURE** aktualisiert werden, wenn einem Namen ein neuer Bezeichner zugewiesen oder ein neues Name- und Bezeichnerpaar hinzugefügt wird. 
  
Clients, die mit den benannten Eigenschaften von Objekten arbeiten, verwenden die Eigenschaften **PR_MAPPING_SIGNATURE** Objekten in Vergleichs- und Kopiervorgängen. Zum Vergleichen benannter Eigenschaftenbezeichner, die zu zwei Objekten gehören, müssen Clients, die keine Zuordnungssignaturen verwenden, [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) für beide Objekte aufrufen, um die Namen für jeden bezeichner abzurufen. Die Verwendung der Zuordnungssignaturen von Objekten kann diesen Aufruf unnötig machen. Wenn zwei Objekte denselben Wert für ihre PR_MAPPING_SIGNATURE **haben,** verwenden sie dieselbe Zuordnung. Bezeichner, die dieselbe Zuordnung verwenden, können direkt verglichen werden. Dienstanbieter, die [IMAPIProp::CopyTo](imapiprop-copyto.md) und [IMAPIProp::CopyProps implementieren,](imapiprop-copyprops.md) können auch die Zuordnungssignatur eines Objekts nutzen. Beim Kopieren benannter Eigenschaften zwischen Objekten können Dienstanbieter den Konvertierungsschritt vermeiden, wenn die Quell- und Zielobjekte dieselbe Zuordnungssignatur aufweisen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp : IUnknown](imapipropiunknown.md)


[Benannte Eigenschaften MAPI](mapi-named-properties.md)

