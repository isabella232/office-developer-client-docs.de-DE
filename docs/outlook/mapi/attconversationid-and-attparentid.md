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
# <a name="attconversationid-and-attparentid"></a><span data-ttu-id="983e0-103">attConversationID und attParentID</span><span class="sxs-lookup"><span data-stu-id="983e0-103">attConversationID and attParentID</span></span>

<span data-ttu-id="983e0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="983e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="983e0-105">Der Windows für Workgroups 3.1 E-Mail-Unterhaltungsschlüssel ist eine Textzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="983e0-105">The Windows for Workgroups 3.1 Mail conversation key is a text string.</span></span> <span data-ttu-id="983e0-106">Das MAPI-Äquivalent ist ein binärer Wert.</span><span class="sxs-lookup"><span data-stu-id="983e0-106">The MAPI equivalent is a binary value.</span></span> <span data-ttu-id="983e0-107">Um abwärtskompatibel zu sein, konvertiert die TNEF-Implementierung die Binärdaten in Text und fügt ein endendes Nullzeichen hinzu.</span><span class="sxs-lookup"><span data-stu-id="983e0-107">To provide backward compatibility, the TNEF implementation converts the binary data to text and adds a terminating null character.</span></span>
  
> [!NOTE]
> <span data-ttu-id="983e0-108">Die entsprechenden Eigenschaften in MAPI, denen diese TNEF-Attribute zugeordnet sind, PR_CONVERSATION_KEY und PR_PARENT_KEY, sind in Microsoft Exchange Server: Use of **PR_CONVERSATION_KEY**, the [PidTagConversationKey Canonical Property](pidtagconversationkey-canonical-property.md), in Outlook nur für die Suche nach **IPM veraltet. MessageManager-Nachrichten.**</span><span class="sxs-lookup"><span data-stu-id="983e0-108">The corresponding properties in MAPI to which these TNEF attributes are mapped, PR_CONVERSATION_KEY and PR_PARENT_KEY, have been deprecated in Microsoft Exchange Server: Use of **PR_CONVERSATION_KEY**, the [PidTagConversationKey Canonical Property](pidtagconversationkey-canonical-property.md), persists in Outlook only, for locating **IPM.MessageManager** messages.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="983e0-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="983e0-109">Remarks</span></span>

<span data-ttu-id="983e0-110">Die **PR_CONVERSATION_KEY-Eigenschaft** ist der ansonsten veraltete Vorläufer der **kanonischen Eigenschaft PR_CONVERSATION_INDEX**, [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) und **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic (kanonische](pidtagconversationtopic-canonical-property.md)Eigenschaft), die stattdessen verwendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="983e0-110">The **PR_CONVERSATION_KEY** property is the otherwise obsolete precursor of the **PR_CONVERSATION_INDEX**, [PidTagConversationIndex Canonical Property](pidtagconversationindex-canonical-property.md) and **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic Canonical Property](pidtagconversationtopic-canonical-property.md), which should be used instead.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="983e0-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="983e0-111">See also</span></span>

- [<span data-ttu-id="983e0-112">IPM-Unterstruktur</span><span class="sxs-lookup"><span data-stu-id="983e0-112">IPM Subtree</span></span>](ipm-subtree.md)
- [<span data-ttu-id="983e0-113">MAPI-Sonderordner</span><span class="sxs-lookup"><span data-stu-id="983e0-113">MAPI Special Folders</span></span>](mapi-special-folders.md)

