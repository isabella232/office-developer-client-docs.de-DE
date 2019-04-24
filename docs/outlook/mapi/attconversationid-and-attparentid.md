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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318417"
---
# <a name="attconversationid-and-attparentid"></a><span data-ttu-id="2d57c-103">attConversationID und attParentID</span><span class="sxs-lookup"><span data-stu-id="2d57c-103">attConversationID and attParentID</span></span>

<span data-ttu-id="2d57c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d57c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d57c-105">Der Schlüssel Windows für Workgroups 3,1-e-Mail-Unterhaltung ist eine Textzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="2d57c-105">The Windows for Workgroups 3.1 Mail conversation key is a text string.</span></span> <span data-ttu-id="2d57c-106">Die MAPI-Entsprechung ist ein Binärwert.</span><span class="sxs-lookup"><span data-stu-id="2d57c-106">The MAPI equivalent is a binary value.</span></span> <span data-ttu-id="2d57c-107">Um die Abwärtskompatibilität zu gewährleisten, wandelt die TNEF-Implementierung die Binärdaten in Text um und fügt ein endgültiges NULL-Zeichen hinzu.</span><span class="sxs-lookup"><span data-stu-id="2d57c-107">To provide backward compatibility, the TNEF implementation converts the binary data to text and adds a terminating null character.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2d57c-108">Die entsprechenden Eigenschaften in MAPI, denen diese TNEF-Attribute zugeordnet sind, PR_CONVERSATION_KEY und PR_PARENT_KEY, sind in Microsoft Exchange Server veraltet: Verwendung von **PR_CONVERSATION_KEY**, der [kanonischen pidtagconversationkey ( -Eigenschaft](pidtagconversationkey-canonical-property.md), bleibt in Outlook nur für die Suche nach **IPM. MessageManager** -Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="2d57c-108">The corresponding properties in MAPI to which these TNEF attributes are mapped, PR_CONVERSATION_KEY and PR_PARENT_KEY, have been deprecated in Microsoft Exchange Server: Use of **PR_CONVERSATION_KEY**, the [PidTagConversationKey Canonical Property](pidtagconversationkey-canonical-property.md), persists in Outlook only, for locating **IPM.MessageManager** messages.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2d57c-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d57c-109">Remarks</span></span>

<span data-ttu-id="2d57c-110">Die **PR_CONVERSATION_KEY** -Eigenschaft ist der andernfalls veraltete Vorläufer der **PR_CONVERSATION_INDEX**, [PidTagConversationIndex kanonischen Eigenschaft](pidtagconversationindex-canonical-property.md) und **PR_CONVERSATION_TOPIC**, [eigenschaftpidtagconversationtopic kanonischen -Eigenschaft](pidtagconversationtopic-canonical-property.md), die stattdessen verwendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="2d57c-110">The **PR_CONVERSATION_KEY** property is the otherwise obsolete precursor of the **PR_CONVERSATION_INDEX**, [PidTagConversationIndex Canonical Property](pidtagconversationindex-canonical-property.md) and **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic Canonical Property](pidtagconversationtopic-canonical-property.md), which should be used instead.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2d57c-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d57c-111">See also</span></span>

- [<span data-ttu-id="2d57c-112">IPM-unterStruktur</span><span class="sxs-lookup"><span data-stu-id="2d57c-112">IPM Subtree</span></span>](ipm-subtree.md)
- [<span data-ttu-id="2d57c-113">MAPI-Spezialordner</span><span class="sxs-lookup"><span data-stu-id="2d57c-113">MAPI Special Folders</span></span>](mapi-special-folders.md)

