---
title: AttConversationID und attParentID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bed36900-e44d-434b-a4f2-d10f2d6f70da
description: 'Zuletzt geändert: 12 März 2013'
ms.openlocfilehash: 2fd3e66e3171c677465a533ede3001cd0b28c8aa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791321"
---
# <a name="attconversationid-and-attparentid"></a>AttConversationID und attParentID

**Betrifft**: Outlook 
  
Die Fenster für Arbeitsgruppen 3.1 e-Mail-Unterhaltung Schlüssel ist eine Textzeichenfolge. MAPI-entspricht einem Binärwert. Um Abwärtskompatibilität zu ermöglichen, die TNEF-Implementierung Binärdaten in Text konvertiert und Endzeichen Null hinzugefügt.
  
> [!NOTE]
> Die entsprechenden Eigenschaften in MAPI, dem diese Attribute TNEF zugeordnet sind, PR_CONVERSATION_KEY und PR_PARENT_KEY, sind veraltet in Microsoft Exchange Server: Verwendung von **PR_CONVERSATION_KEY**, die kanonische PidTagConversationKey [ Eigenschaft](pidtagconversationkey-canonical-property.md), nur für die Suche nach **IPM in Outlook beibehalten. Nachrichten-Managers** Nachrichten. 
  
## <a name="remarks"></a>Hinweise

Die **PR_CONVERSATION_KEY** -Eigenschaft ist die andernfalls veraltet Vorläufer der **PR_CONVERSATION_INDEX**, [Kanonische-Eigenschaft PidTagConversationIndex](pidtagconversationindex-canonical-property.md) und **PR_CONVERSATION_TOPIC**, [Eigenschaftpidtagconversationtopic kanonische Eigenschaft](pidtagconversationtopic-canonical-property.md), die stattdessen verwendet werden soll.
  
## <a name="see-also"></a>Siehe auch

- [IPM-Unterstruktur](ipm-subtree.md)
- [MAPI-Spezialordner](mapi-special-folders.md)

