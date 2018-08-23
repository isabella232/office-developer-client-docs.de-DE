---
title: attConversationID und attParentID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bed36900-e44d-434b-a4f2-d10f2d6f70da
description: 'Zuletzt geändert: 12 März 2013'
ms.openlocfilehash: 14b93a952e4776716c333dc730144b55bcc61259
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582714"
---
# <a name="attconversationid-and-attparentid"></a>attConversationID und attParentID

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Die Fenster für Arbeitsgruppen 3.1 e-Mail-Unterhaltung Schlüssel ist eine Textzeichenfolge. MAPI-entspricht einem Binärwert. Um Abwärtskompatibilität zu ermöglichen, die TNEF-Implementierung Binärdaten in Text konvertiert und Endzeichen Null hinzugefügt.
  
> [!NOTE]
> Die entsprechenden Eigenschaften in MAPI, dem diese Attribute TNEF zugeordnet sind, PR_CONVERSATION_KEY und PR_PARENT_KEY, sind veraltet in Microsoft Exchange Server: Verwendung von **PR_CONVERSATION_KEY**, die kanonische PidTagConversationKey [ Eigenschaft](pidtagconversationkey-canonical-property.md), nur für die Suche nach **IPM in Outlook beibehalten. Nachrichten-Managers** Nachrichten. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Die **PR_CONVERSATION_KEY** -Eigenschaft ist die andernfalls veraltet Vorläufer der **PR_CONVERSATION_INDEX**, [Kanonische-Eigenschaft PidTagConversationIndex](pidtagconversationindex-canonical-property.md) und **PR_CONVERSATION_TOPIC**, [Eigenschaftpidtagconversationtopic kanonische Eigenschaft](pidtagconversationtopic-canonical-property.md), die stattdessen verwendet werden soll.
  
## <a name="see-also"></a>Siehe auch

- [IPM-Teilstruktur](ipm-subtree.md)
- [MAPI-Spezialordner](mapi-special-folders.md)

