---
title: Unterstützen von RTF-Text für Nachrichtenspeicher Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: dc1d8a5e237b7b34f3a57e9789e03e2f16237764
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414214"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a><span data-ttu-id="6535f-103">Unterstützen von RTF-Text für Nachrichtenspeicher Anbieter</span><span class="sxs-lookup"><span data-stu-id="6535f-103">Supporting RTF Text for Message Store Providers</span></span>

  
  
<span data-ttu-id="6535f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6535f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6535f-105">Einige Clientanwendungen ermöglichen es Benutzern, RTF-Text (Rich Text Format) in ihren Nachrichten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6535f-105">Some client applications allow users to use Rich Text Format (RTF) text in their messages.</span></span> <span data-ttu-id="6535f-106">Wenn der Nachrichtenspeicher Anbieter RTF-Text in Nachrichten unterstützen muss, muss er zusätzlich zur **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md))-Eigenschaft die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft behandeln.</span><span class="sxs-lookup"><span data-stu-id="6535f-106">If your message store provider needs to support RTF text in messages, it needs to handle the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, in addition to the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span> <span data-ttu-id="6535f-107">Dies ist in erster Linie das Speichern beider Eigenschaften und das sicherstellen, dass **PR_BODY** eine nur-Text-Version des Texts in **PR_RTF_COMPRESSED**enthält.</span><span class="sxs-lookup"><span data-stu-id="6535f-107">Primarily, this means storing both properties, and making sure that **PR_BODY** contains a plain text version of the text in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="6535f-108">Die [RTFSync](rtfsync.md) -Funktion ist für diesen Zweck nützlich.</span><span class="sxs-lookup"><span data-stu-id="6535f-108">The [RTFSync](rtfsync.md) function is useful for this purpose.</span></span> 
  
<span data-ttu-id="6535f-109">Es gibt zwei Flags, die in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft des Nachrichtenspeicher Objekts festgelegt werden können, die den Clients mitteilen, was Sie vom Nachrichtenspeicher Anbieter im Hinblick auf **PR_BODY** und PR_ erwarten können. \*\* RTF_COMPRESSED\*\* -Eigenschaften für Nachrichten im Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="6535f-109">There are two flags that can be set in the message store object's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property that tell clients what they can expect from the message store provider with respect to the **PR_BODY** and **PR_RTF_COMPRESSED** properties on messages in the message store.</span></span> <span data-ttu-id="6535f-110">Das STORE_RTF_OK-Flag gibt an, dass der Speicher den Wert der **PR_BODY** -Eigenschaft aus der **PR_RTF_COMPRESSED** -Eigenschaft dynamisch generieren kann, wodurch Clients von der Last der expliziten Synchronisierung entlastet werden.</span><span class="sxs-lookup"><span data-stu-id="6535f-110">The STORE_RTF_OK flag indicates that the store can generate the value of the **PR_BODY** property from the **PR_RTF_COMPRESSED** property dynamically, which relieves clients from the burden of synchronizing them explicitly.</span></span> <span data-ttu-id="6535f-111">Das STORE_UNCOMPRESSED_RTF-Flag gibt an, dass der Nachrichtenspeicher Anbieter nicht komprimierte Daten in **PR_RTF_COMPRESSED**unterstützenkann.</span><span class="sxs-lookup"><span data-stu-id="6535f-111">The STORE_UNCOMPRESSED_RTF flag indicates that the message store provider can support uncompressed data in **PR_RTF_COMPRESSED**.</span></span>
  
<span data-ttu-id="6535f-112">Nachrichtenspeicher Anbieter, die keinen RTF-Text unterstützen, müssen die **PR_RTF_IN_SYNC** ([pidtagrtfinsync (](pidtagrtfinsync-canonical-property.md))-Eigenschaft löschen, wenn sich die **PR_BODY** -Eigenschaft ändert, um ordnungsgemäß mit CLIENTanwendungen zu interagieren, die RTF-Text unterstützen. .</span><span class="sxs-lookup"><span data-stu-id="6535f-112">Message store providers that do not support RTF text need to delete the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property when the **PR_BODY** property changes in order to interoperate properly with client applications that do support RTF text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6535f-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6535f-113">See also</span></span>



[<span data-ttu-id="6535f-114">Nachrichtenspeicher-Features</span><span class="sxs-lookup"><span data-stu-id="6535f-114">Message Store Features</span></span>](message-store-features.md)

