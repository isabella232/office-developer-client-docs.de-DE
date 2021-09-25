---
title: attConversationID und attParentID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: bed36900-e44d-434b-a4f2-d10f2d6f70da
description: 'Letzte Änderung: 12. März 2013'
ms.openlocfilehash: f52383c5208fc2288018dcdeb644722e73dfc86a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605181"
---
# <a name="attconversationid-and-attparentid"></a>attConversationID und attParentID

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Windows für den E-Mail-Unterhaltungsschlüssel für Arbeitsgruppen 3.1 ist eine Textzeichenfolge. Das MAPI-Äquivalent ist ein binärer Wert. Zur Gewährleistung der Abwärtskompatibilität konvertiert die TNEF-Implementierung die Binärdaten in Text und fügt ein nullendes Zeichen hinzu.
  
> [!NOTE]
> Die entsprechenden Eigenschaften in der MAPI, denen diese TNEF-Attribute zugeordnet sind, PR_CONVERSATION_KEY und PR_PARENT_KEY, sind in Microsoft Exchange Server veraltet: Die Verwendung von **PR_CONVERSATION_KEY**, der [kanonischen PidTagConversationKey-Eigenschaft,](pidtagconversationkey-canonical-property.md)wird nur in Outlook beibehalten, um IPM zu **suchen. MessageManager-Nachrichten.** 
  
## <a name="remarks"></a>HinwBemerkungeneise

Die **PR_CONVERSATION_KEY-Eigenschaft** ist die ansonsten veraltete Vorgängereigenschaft der **kanonischen PR_CONVERSATION_INDEX**, [PidTagConversationIndex-Eigenschaft](pidtagconversationindex-canonical-property.md) und **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic (kanonische Eigenschaft),](pidtagconversationtopic-canonical-property.md)die stattdessen verwendet werden sollte.
  
## <a name="see-also"></a>Siehe auch

- [IPM-Unterstruktur](ipm-subtree.md)
- [MAPI-Spezialordner](mapi-special-folders.md)

