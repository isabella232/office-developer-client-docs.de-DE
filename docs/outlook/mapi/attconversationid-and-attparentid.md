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
  
Der Windows für Workgroups 3.1 E-Mail-Unterhaltungsschlüssel ist eine Textzeichenfolge. Das MAPI-Äquivalent ist ein binärer Wert. Um abwärtskompatibel zu sein, konvertiert die TNEF-Implementierung die Binärdaten in Text und fügt ein endendes Nullzeichen hinzu.
  
> [!NOTE]
> Die entsprechenden Eigenschaften in MAPI, denen diese TNEF-Attribute zugeordnet sind, PR_CONVERSATION_KEY und PR_PARENT_KEY, sind in Microsoft Exchange Server: Use of **PR_CONVERSATION_KEY**, the [PidTagConversationKey Canonical Property](pidtagconversationkey-canonical-property.md), in Outlook nur für die Suche nach **IPM veraltet. MessageManager-Nachrichten.** 
  
## <a name="remarks"></a>Hinweise

Die **PR_CONVERSATION_KEY-Eigenschaft** ist der ansonsten veraltete Vorläufer der **kanonischen Eigenschaft PR_CONVERSATION_INDEX**, [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) und **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic (kanonische](pidtagconversationtopic-canonical-property.md)Eigenschaft), die stattdessen verwendet werden sollte.
  
## <a name="see-also"></a>Siehe auch

- [IPM-Unterstruktur](ipm-subtree.md)
- [MAPI-Sonderordner](mapi-special-folders.md)

