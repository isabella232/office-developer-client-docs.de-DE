---
title: Erstellen eine Einschränkung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 12abbd8c-f825-493e-af42-344371d9658e
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3b40c8433f93237db2ae4fd5449fe8a0da486539
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791368"
---
# <a name="building-a-restriction"></a>Erstellen eine Einschränkung

**Betrifft**: Outlook 
  
Zum Erstellen einer Einschränkung einer Clientanwendung erstellt eine Hierarchie von mindestens Einschränkung Strukturen der verschiedenen Typen und übergibt einen Zeiger auf der Hierarchie, um die [Methode IMAPITable:: Restrict](imapitable-restrict.md) oder [IMAPITable](imapitable-findrow.md) -Methode. Die Abbildung, die folgt und das Codebeispiel in [Einschränkung Beispielcode](sample-restriction-code.md) veranschaulichen, wie eine normale Einschränkung mit verknüpften Einschränkung Strukturen mit unterschiedlichen Typen implementiert wird. 

In diesem Beispiel wird versucht, ein Benutzer von einer Clientanwendung alle Nachrichten zu finden, die das Wort "Volleyball" in der Betreffzeile enthalten und von Sam an Sue gesendet wurden. Erstens wird eine generische Struktur [SRestriction](srestriction.md) zugewiesen. Diese Struktur wird als Basis für weitere Anrufe an die Funktion [MAPIAllocateMore](mapiallocatemore.md) erstellen Sie mit einem einzigen Aufruf [MAPIFreeBuffer](mapifreebuffer.md)verknüpfte [SRestriction](srestriction.md) und [SPropValue](spropvalue.md) Strukturen, die freigegeben werden können. Da die Kriterien für den Satz von Nachrichten gelten besteht aus drei Teilen, ist die oberste Ebene Einschränkung-Struktur einer Einschränkung **und** . Die [SAndRestriction](sandrestriction.md) Struktur **cRes** Member auf 3 festgelegt ist, um anzugeben, die drei Einschränkungen für ausgewertet werden soll, und seine Member **LpRes** auf ein Array mit drei Mitgliedern der **SRestriction** Strukturen festgelegt ist. 
  
Um nach Nachrichten gesucht, die für einen bestimmten Empfänger gesendet werden, ist es erforderlich, die Empfänger Tabelle für jede Nachricht statt der Nachricht selbst zu durchsuchen. Eine Einschränkung Unterobjekts wird verwendet, um die Empfänger Tabelle Suche durchzuführen. Legen Sie der erste Eintrag der Array verweist auf eine [SSubRestriction](ssubrestriction.md) -Struktur mit den **UlSubObject** -Member aus diesem Grund auf **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)). Klicken Sie, um anzugeben, wonach Sie suchen in der Tabelle Empfänger, eine Content Einschränkung verwendet wird. 
  
Die zweite und dritte Member des Arrays sind einfacher. Beide zeigen Sie auf Content Einschränkung Strukturen, eine nach Nachrichten gesucht, deren eine auf "Sam" und ein weiteres festgelegte **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))-Eigenschaft einen Eigenschaftensatz **PR_SUBJECT** ([PidTagSubject hat](pidtagsubject-canonical-property.md)) zu" Volleyball."
  
**Implementierung von Beschränkungen**
  
![Einschränkungsimplementierung] (media/amapi_61.gif "Einschränkungsimplementierung")
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Tabellen](mapi-tables.md)

