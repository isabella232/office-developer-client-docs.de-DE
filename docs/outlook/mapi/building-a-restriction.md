---
title: Erstellen einer Einschränkung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 12abbd8c-f825-493e-af42-344371d9658e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5036a4989c8a25cecbe31c20512f8f46fec80c54
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556924"
---
# <a name="building-a-restriction"></a>Erstellen einer Einschränkung

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zum Erstellen einer Einschränkung erstellt eine Clientanwendung eine Hierarchie aus einer oder mehreren Einschränkungsstrukturen verschiedener Typen und übergibt einen Zeiger auf die Hierarchie an die [IMAPITable::Restrict-](imapitable-restrict.md) oder [IMAPITable::FindRow-Methode.](imapitable-findrow.md) Die folgende Abbildung und das Codebeispiel in [Beispieleinschränkungscode](sample-restriction-code.md) veranschaulichen, wie eine typische Einschränkung mit verknüpften Einschränkungsstrukturen unterschiedlicher Typen implementiert wird. 

In diesem Beispiel versucht ein Benutzer einer Clientanwendung, alle Nachrichten zu finden, die das Wort "mails" in der Betreffzeile enthalten und von Sam an Sue gesendet wurden. Zunächst wird eine generische [SRestriction-Struktur](srestriction.md) zugewiesen. Diese Struktur wird zur Basis für andere Aufrufe der [MAPIAllocateMore-Funktion,](mapiallocatemore.md) um verknüpfte [SRestriction-](srestriction.md) und [SPropValue-Strukturen](spropvalue.md) zu erstellen, die mit einem einzigen Aufruf von [MAPIFreeBuffer](mapifreebuffer.md)freigegeben werden können. Da die Kriterien, die auf den Satz von Nachrichten angewendet werden  sollen, in drei Teilen bestehen, ist die Einschränkungsstruktur der obersten Ebene eine AND-Einschränkung. Das **cRes-Element** der [SAndRestriction-Struktur](sandrestriction.md) ist auf 3 festgelegt, um die drei zu bewertenden Einschränkungen anzugeben, und der **lpRes-Member** wird auf ein Array mit drei Membern von **SRestriction-Strukturen** festgelegt. 
  
Um nach Nachrichten zu suchen, die an einen bestimmten Empfänger gesendet werden, müssen Sie die Empfängertabelle nach jeder Nachricht und nicht nach der Nachricht selbst durchsuchen. Zum Ausführen der Empfängertabellensuche wird eine Unterobjekteinschränkung verwendet. Daher zeigt das erste Element des Arrays auf eine [SSubRestriction-Struktur,](ssubrestriction.md) deren **ulSubObject-Element** auf **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) festgelegt ist. Um dann anzugeben, wonach in der Empfängertabelle gesucht werden soll, wird eine Inhaltseinschränkung verwendet. 
  
Die zweiten und dritten Elemente des Arrays sind einfacher. Beide verweisen auf Inhaltseinschränkungsstrukturen, eine, um nach Nachrichten zu suchen, für die eine **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) -Eigenschaft auf "Sam" festgelegt ist, und eine andere, für die eine **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) -Eigenschaft auf "bundesland" festgelegt ist.
  
**Implementierung von Beschränkungen**
  
![Implementierung von Beschränkungen](media/amapi_61.gif "Implementierung von Beschränkungen")
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Tabellen](mapi-tables.md)

