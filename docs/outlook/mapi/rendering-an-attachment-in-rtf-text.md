---
title: Darstellen einer Anlage als RTF-Text
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5d8fc10f876408d616c5acefb664ba5d61c927a2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22562974"
---
# <a name="rendering-an-attachment-in-rtf-text"></a><span data-ttu-id="ce0bd-103">Darstellen einer Anlage als RTF-Text</span><span class="sxs-lookup"><span data-stu-id="ce0bd-103">Rendering an Attachment in RTF Text</span></span>

  
  
<span data-ttu-id="ce0bd-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce0bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce0bd-105">Rich-Text-Format (RTF)-Clients unterstützen können Positionsinformationen Rendering von RTF des Nachrichtentexts anhand der folgenden Escapezeichen in der Nachricht **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft abrufen:</span><span class="sxs-lookup"><span data-stu-id="ce0bd-105">Rich Text Format (RTF)-aware clients can retrieve rendering position information from RTF message text by looking for the following escape sequence in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property:</span></span>
  
 `\objattph`
  
 <span data-ttu-id="ce0bd-106">**Zum Suchen von Rendering-Informationen in formatierten text**</span><span class="sxs-lookup"><span data-stu-id="ce0bd-106">**To locate rendering information in formatted text**</span></span>
  
1. <span data-ttu-id="ce0bd-107">Rufen Sie **IMessage::GetAttachmentTable** Zugriff auf die Nachricht Anlage-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ce0bd-107">Call **IMessage::GetAttachmentTable** to access the message's attachment table.</span></span> <span data-ttu-id="ce0bd-108">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span><span class="sxs-lookup"><span data-stu-id="ce0bd-108">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span></span>
    
2. <span data-ttu-id="ce0bd-109">Erstellen Sie eine eigenschaftseinschränkung, die die Tabelle, um Zeilen beschränkt, die nicht gleich-1 **PR_RENDERING_POSITION** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ce0bd-109">Build a property restriction that limits the table to rows that have **PR_RENDERING_POSITION** not equal to -1.</span></span> <span data-ttu-id="ce0bd-110">Weitere Informationen finden Sie unter **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ce0bd-110">For more information, see **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="ce0bd-111">Rufen Sie die **Methode IMAPITable:: Restrict** , um die Einschränkung zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="ce0bd-111">Call **IMAPITable::Restrict** to enforce the restriction.</span></span> <span data-ttu-id="ce0bd-112">Weitere Informationen finden Sie unter [Methode IMAPITable:: Restrict](imapitable-restrict.md).</span><span class="sxs-lookup"><span data-stu-id="ce0bd-112">For more information, see [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
    
4. <span data-ttu-id="ce0bd-113">Rufen Sie **SortTable** , um die Anlagen zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="ce0bd-113">Call **IMAPITable::SortTable** to sort the attachments.</span></span> <span data-ttu-id="ce0bd-114">Weitere Informationen finden Sie unter [SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="ce0bd-114">For more information, see [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
5. <span data-ttu-id="ce0bd-115">Rufen Sie **IMAPITable::QueryRows** zum Abrufen der entsprechenden Zeilen.</span><span class="sxs-lookup"><span data-stu-id="ce0bd-115">Call **IMAPITable::QueryRows** to retrieve the appropriate rows.</span></span> <span data-ttu-id="ce0bd-116">Weitere Informationen finden Sie unter [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="ce0bd-116">For more information, see [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
    
6. <span data-ttu-id="ce0bd-117">Rufen Sie die Nachricht **IMAPIProp::OpenProperty** -Methode zum Abrufen von **PR_RTF_COMPRESSED** mit der **IStream** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ce0bd-117">Call the message's **IMAPIProp::OpenProperty** method to retrieve **PR_RTF_COMPRESSED** with the **IStream** interface.</span></span> <span data-ttu-id="ce0bd-118">Weitere Informationen finden Sie unter [IMAPIProp::OpenProperty](imapiprop-openproperty.md) und **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="ce0bd-118">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
    
7. <span data-ttu-id="ce0bd-119">Überprüfung den Stream, suchen Sie nach der Platzhalter Rendering `\objattph`.</span><span class="sxs-lookup"><span data-stu-id="ce0bd-119">Scan the stream, looking for the rendering placeholder,  `\objattph`.</span></span> <span data-ttu-id="ce0bd-120">Das Zeichen nach dieser Platzhalter ist der Ort für die neue Anlage in der sortierten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ce0bd-120">The character following this placeholder is the place for the next attachment in the sorted table.</span></span>
    

