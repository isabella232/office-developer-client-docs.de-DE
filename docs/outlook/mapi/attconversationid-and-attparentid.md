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
# <a name="attconversationid-and-attparentid"></a><span data-ttu-id="666e6-103">AttConversationID und attParentID</span><span class="sxs-lookup"><span data-stu-id="666e6-103">attConversationID and attParentID</span></span>

<span data-ttu-id="666e6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="666e6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="666e6-105">Die Fenster für Arbeitsgruppen 3.1 e-Mail-Unterhaltung Schlüssel ist eine Textzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="666e6-105">The Windows for Workgroups 3.1 Mail conversation key is a text string.</span></span> <span data-ttu-id="666e6-106">MAPI-entspricht einem Binärwert.</span><span class="sxs-lookup"><span data-stu-id="666e6-106">The MAPI equivalent is a binary value.</span></span> <span data-ttu-id="666e6-107">Um Abwärtskompatibilität zu ermöglichen, die TNEF-Implementierung Binärdaten in Text konvertiert und Endzeichen Null hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="666e6-107">To provide backward compatibility, the TNEF implementation converts the binary data to text and adds a terminating null character.</span></span>
  
> [!NOTE]
> <span data-ttu-id="666e6-108">Die entsprechenden Eigenschaften in MAPI, dem diese Attribute TNEF zugeordnet sind, PR_CONVERSATION_KEY und PR_PARENT_KEY, sind veraltet in Microsoft Exchange Server: Verwendung von **PR_CONVERSATION_KEY**, die kanonische PidTagConversationKey [ Eigenschaft](pidtagconversationkey-canonical-property.md), nur für die Suche nach **IPM in Outlook beibehalten. Nachrichten-Managers** Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="666e6-108">The corresponding properties in MAPI to which these TNEF attributes are mapped, PR_CONVERSATION_KEY and PR_PARENT_KEY, have been deprecated in Microsoft Exchange Server: Use of **PR_CONVERSATION_KEY**, the [PidTagConversationKey Canonical Property](pidtagconversationkey-canonical-property.md), persists in Outlook only, for locating **IPM.MessageManager** messages.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="666e6-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="666e6-109">Remarks</span></span>

<span data-ttu-id="666e6-110">Die **PR_CONVERSATION_KEY** -Eigenschaft ist die andernfalls veraltet Vorläufer der **PR_CONVERSATION_INDEX**, [Kanonische-Eigenschaft PidTagConversationIndex](pidtagconversationindex-canonical-property.md) und **PR_CONVERSATION_TOPIC**, [Eigenschaftpidtagconversationtopic kanonische Eigenschaft](pidtagconversationtopic-canonical-property.md), die stattdessen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="666e6-110">The **PR_CONVERSATION_KEY** property is the otherwise obsolete precursor of the **PR_CONVERSATION_INDEX**, [PidTagConversationIndex Canonical Property](pidtagconversationindex-canonical-property.md) and **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic Canonical Property](pidtagconversationtopic-canonical-property.md), which should be used instead.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="666e6-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="666e6-111">See also</span></span>

- [<span data-ttu-id="666e6-112">IPM-Unterstruktur</span><span class="sxs-lookup"><span data-stu-id="666e6-112">IPM Subtree</span></span>](ipm-subtree.md)
- [<span data-ttu-id="666e6-113">MAPI-Spezialordner</span><span class="sxs-lookup"><span data-stu-id="666e6-113">MAPI Special Folders</span></span>](mapi-special-folders.md)

