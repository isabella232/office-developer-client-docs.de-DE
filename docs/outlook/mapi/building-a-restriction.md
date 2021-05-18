---
title: Erstellen einer Einschränkung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 12abbd8c-f825-493e-af42-344371d9658e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 38182abd922cd5806a14b6541c22ce675b997387
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422510"
---
# <a name="building-a-restriction"></a>Erstellen einer Einschränkung

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zum Erstellen einer Einschränkung erstellt eine Clientanwendung eine Hierarchie aus einer oder mehreren Einschränkungsstrukturen verschiedener Typen und übergibt einen Zeiger auf die Hierarchie an die [IMAPITable::Restrict-](imapitable-restrict.md) oder [IMAPITable::FindRow-Methode.](imapitable-findrow.md) Die folgende Abbildung und das Codebeispiel in [Beispieleinschränkungscode](sample-restriction-code.md) zeigen, wie eine typische Einschränkung mit verknüpften Einschränkungsstrukturen unterschiedlicher Typen implementiert wird. 

In diesem Beispiel versucht ein Benutzer einer Clientanwendung, alle Nachrichten zu finden, die das Wort "volleyball" in der Betreffzeile enthalten und von Sam an Sue gesendet wurden. Zunächst wird eine generische [SRestriction-Struktur](srestriction.md) zugewiesen. Diese Struktur wird zur Grundlage für andere Aufrufe der [MAPIAllocateMore-Funktion,](mapiallocatemore.md) um verknüpfte [SRestriction-](srestriction.md) und [SPropValue-Strukturen](spropvalue.md) zu erstellen, die mit einem einzelnen Aufruf von [MAPIFreeBuffer](mapifreebuffer.md)frei werden können. Da die Kriterien, die auf den Satz von Nachrichten angewendet werden sollen, in drei Teilen enthalten sind, ist die Einschränkungsstruktur auf oberster Ebene eine **AND-Einschränkung.** Das **cRes-Element** der [SAndRestriction-Struktur](sandrestriction.md) ist auf 3 festgelegt, um die drei auszuwertende Einschränkungen anzugeben, und das **lpRes-Element** ist auf ein drei-Member-Array von **SRestriction-Strukturen** festgelegt. 
  
Um nach Nachrichten zu suchen, die an einen bestimmten Empfänger gesendet werden, muss die Empfängertabelle nach jeder Nachricht und nicht nach der Nachricht selbst durchsucht werden. Zum Ausführen der Empfängertabelle wird eine Unterobjekteinschränkung verwendet. Daher verweist das erste Element des Arrays auf eine [SSubRestriction-Struktur,](ssubrestriction.md) deren **ulSubObject-Element** auf **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) festgelegt ist. Um anzugeben, was in der Empfängertabelle zu suchen ist, wird dann eine Inhaltseinschränkung verwendet. 
  
Die zweiten und dritten Elemente des Arrays sind einfacher. Beide verweisen auf Inhaltseinschränkungsstrukturen, um nach Nachrichten zu **suchen,** für die eine PR_SENDER_NAME ([PidTagSenderName](pidtagsendername-canonical-property.md))-Eigenschaft auf "Sam" festgelegt ist, und eine andere mit einer **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))-Eigenschaft, die auf "volleyball" festgelegt ist.
  
**Implementierung von Beschränkungen**
  
![Einschränkungsimplementierung](media/amapi_61.gif "Einschränkungsimplementierung")
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Tabellen](mapi-tables.md)

