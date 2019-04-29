---
title: attConversationID und attParentID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bed36900-e44d-434b-a4f2-d10f2d6f70da
description: 'Letzte Änderung: 12. März 2013'
ms.openlocfilehash: c5880aefe7c2dba2e5e4c5405aae2020bb86c711
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410049"
---
# <a name="attconversationid-and-attparentid"></a>attConversationID und attParentID

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Schlüssel Windows für Workgroups 3,1-e-Mail-Unterhaltung ist eine Textzeichenfolge. Die MAPI-Entsprechung ist ein Binärwert. Um die Abwärtskompatibilität zu gewährleisten, wandelt die TNEF-Implementierung die Binärdaten in Text um und fügt ein endgültiges NULL-Zeichen hinzu.
  
> [!NOTE]
> Die entsprechenden Eigenschaften in MAPI, denen diese TNEF-Attribute zugeordnet sind, PR_CONVERSATION_KEY und PR_PARENT_KEY, sind in Microsoft Exchange Server veraltet: Verwendung von **PR_CONVERSATION_KEY**, der [kanonischen pidtagconversationkey ( -Eigenschaft](pidtagconversationkey-canonical-property.md), bleibt in Outlook nur für die Suche nach **IPM. MessageManager** -Nachrichten. 
  
## <a name="remarks"></a>Bemerkungen

Die **PR_CONVERSATION_KEY** -Eigenschaft ist der andernfalls veraltete Vorläufer der **PR_CONVERSATION_INDEX**, [PidTagConversationIndex kanonischen Eigenschaft](pidtagconversationindex-canonical-property.md) und **PR_CONVERSATION_TOPIC**, [eigenschaftpidtagconversationtopic kanonischen -Eigenschaft](pidtagconversationtopic-canonical-property.md), die stattdessen verwendet werden sollte.
  
## <a name="see-also"></a>Siehe auch

- [IPM-unterStruktur](ipm-subtree.md)
- [MAPI-Spezialordner](mapi-special-folders.md)

