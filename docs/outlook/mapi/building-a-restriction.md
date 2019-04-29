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
  
Zum Erstellen einer Einschränkung erstellt eine Clientanwendung eine Hierarchie einer oder mehrerer Einschränkungs Strukturen unterschiedlicher Typen und übergibt einen Zeiger auf die Hierarchie an die [IMAPITable:: Restrict](imapitable-restrict.md) -oder [IMAPITable:: FindRow](imapitable-findrow.md) -Methode. Die folgende Abbildung und das Codebeispiel im [Beispiel-Einschränkungs Code](sample-restriction-code.md) veranschaulichen, wie eine typische Einschränkung mit verknüpften Einschränkungs Strukturen unterschiedlicher Typen implementiert wird. 

In diesem Beispiel versucht ein Benutzer einer Clientanwendung, alle Nachrichten zu suchen, die das Wort "Volleyball" in der Betreffzeile enthalten und an Sue von Sam gesendet wurden. Zunächst wird eine generische [SRestriction](srestriction.md) -Struktur zugeordnet. Diese Struktur wird zur Grundlage anderer Aufrufe der [MAPIAllocateMore](mapiallocatemore.md) -Funktion, um verknüpfte [SRestriction](srestriction.md) -und [SPropValue](spropvalue.md) -Strukturen zu erstellen, die mit einem einzigen Aufruf von [mapifreebufferfreigegeben](mapifreebuffer.md)freigegeben werden können. Da die Kriterien für den Satz von Nachrichten in drei Teilen angewendet werden, ist die Einschränkungs Struktur auf oberster Ebene eine **und-** Einschränkung. Das **cRes** -Element der [SAndRestriction](sandrestriction.md) -Struktur ist auf 3 festgelegt, um die drei auszuwertenden Einschränkungen anzugeben, und sein **lpRes** -Element wird auf ein Array von **SRestriction** -Strukturen mit drei Elementen festgelegt. 
  
Um nach Nachrichten zu suchen, die an einen bestimmten Empfänger gesendet werden, ist es erforderlich, die Empfängertabelle nach jeder Nachricht anstatt nach der Nachricht selbst zu durchsuchen. Für die Suche nach Empfänger Tabellen wird eine Unterobjekt Einschränkung verwendet. Daher zeigt das erste Element des Arrays auf eine [SSubRestriction](ssubrestriction.md) -Struktur, deren **ulSubObject** -Element auf **PR_MESSAGE_RECIPIENTS** ([pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md)) festgelegt ist. Um anzugeben, wonach in der Empfängertabelle gesucht werden soll, wird eine Inhaltseinschränkung verwendet. 
  
Der zweite und dritte Member des Arrays sind einfacher. Beide verweisen auf Inhalts Einschränkungs Strukturen, eine, um nach Nachrichten zu suchen, deren **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))-Eigenschaft auf "Sam" festgelegt ist, und eine andere, für die eine **PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md))-Eigenschaft auf " Volleyball. "
  
**Implementierung von Beschränkungen**
  
![Einschränkungs Implementierung] (media/amapi_61.gif "Einschränkungs Implementierung")
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Tabellen](mapi-tables.md)

