---
title: Zuordnungen und Zuordnungs Signaturen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 773f6671-cc21-4d1f-a11d-308bc71c852d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cd26ce4bc2da3da639b4a611fc9a69f39b13e5f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357638"
---
# <a name="mappings-and-mapping-signatures"></a>Zuordnungen und Zuordnungs Signaturen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn ein Dienstanbieter benannte Eigenschaften unterstützt, wird jede Gruppe von Bezeichner-und namens Paaren als Zuordnung bezeichnet. Dienstanbieter können eine oder mehrere Zuordnungen unterstützen. Ein Nachrichtenspeicher Anbieter kann beispielsweise die Methoden **GetIDsFromNames** und **GetNamesFromIDs** für alle Nachrichten-, Ordner-und Nachrichtenspeicher Objekte implementieren, um mit einer einzelnen Liste von Namen und deren entsprechenden Bezeichnern zu arbeiten. Ein anderer Nachrichtenspeicher Anbieter verfügt möglicherweise über eine Liste für jeden Ordner und die darin enthaltenen Nachrichten oder implementiert eine eindeutige Liste für jede Nachricht und jeden Ordner. Nachrichtenspeicher Anbieter, die eine eindeutige Zuordnung für jede Nachricht verwenden, dürfen nicht zulassen, dass benannte Eigenschaften in ihren Ordnerinhaltstabellen angezeigt werden, da für einen bestimmten Eigenschaftennamen der Eigenschaftenbezeichner von Nachricht zu Nachricht unterschiedlich ist. MAPI empfiehlt, dass Anbieter es einfach halten und mit einer einzigen Liste für alle Objekte einschließlich Tabellen arbeiten. 
  
Für jede Zuordnung müssen Dienstanbieter eine Zuordnungs Signatur angeben. Eine Zuordnungs Signatur ist ein binärer Wert, in der Regel eine GUID, die einen Satz von Eigenschafts Bezeichnern und die zugehörigen Namen eindeutig identifiziert. Zuordnungs Signaturen werden in der **PR_MAPPING_SIGNATURE** ([pidtagmappingsignature (](pidtagmappingsignature-canonical-property.md))-Eigenschaft eines Objekts gespeichert. Dienstanbieter müssen den Wert für Ihre **PR_MAPPING_SIGNATURE** -Eigenschaft ändern, wenn die Zuordnung geändert wird, die Sie darstellt. Beispielsweise muss **PR_MAPPING_SIGNATURE** aktualisiert werden, wenn einem Namen ein neuer Bezeichner zugewiesen wird oder ein neuer Name und ein Bezeichner-Paar hinzugefügt werden. 
  
Clients, die mit den benannten Eigenschaften von Objekten arbeiten, verwenden die **PR_MAPPING_SIGNATURE** -Eigenschaften der Objekte in Vergleichs-und Kopiervorgängen. Um benannte Eigenschaftenbezeichner zu vergleichen, die zu zwei Objekten gehören, müssen Clients, die keine Zuordnungs Signaturen verwenden, [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) für beide Objekte aufrufen, um die Namen der einzelnen Bezeichner abzurufen. Bei Verwendung der Zuordnungs Signaturen von Objekten kann dieser Aufruf nicht erforderlich sein. Wenn zwei Objekte den gleichen Wert für Ihre **PR_MAPPING_SIGNATURE** -Eigenschaften haben, verwenden Sie die gleiche Zuordnung. Bezeichner, die dieselbe Zuordnung verwenden, können direkt verglichen werden. Dienstanbieter, die [IMAPIProp:: CopyTo](imapiprop-copyto.md) und [IMAPIProp:: CopyProps](imapiprop-copyprops.md) implementieren, können auch die Zuordnungs Signatur eines Objekts nutzen. Beim Kopieren benannter Eigenschaften zwischen Objekten können Dienstanbieter den Konvertierungsschritt vermeiden, wenn die Quell-und Zielobjekte dieselbe Zuordnungs Signatur aufweisen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp : IUnknown](imapipropiunknown.md)


[Benannte Eigenschaften MAPI](mapi-named-properties.md)

