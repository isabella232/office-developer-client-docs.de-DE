---
title: Rendern einer Anlage in RTF-Text
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b2a1a23f073d05e85c8203826e3407c5ae193f19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439793"
---
# <a name="rendering-an-attachment-in-rtf-text"></a><span data-ttu-id="e2fd1-103">Rendern einer Anlage in RTF-Text</span><span class="sxs-lookup"><span data-stu-id="e2fd1-103">Rendering an Attachment in RTF Text</span></span>

  
  
<span data-ttu-id="e2fd1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2fd1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2fd1-105">Rich Text Format (RTF)-fähige Clients können Informationen zur Renderingposition aus RTF-Nachrichten Text abrufen, indem Sie in der **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft der Nachricht nach der folgenden Escapesequenz suchen:</span><span class="sxs-lookup"><span data-stu-id="e2fd1-105">Rich Text Format (RTF)-aware clients can retrieve rendering position information from RTF message text by looking for the following escape sequence in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property:</span></span>
  
 `\objattph`
  
 <span data-ttu-id="e2fd1-106">**So suchen Sie Informationen zur Darstellung in formatiertem Text**</span><span class="sxs-lookup"><span data-stu-id="e2fd1-106">**To locate rendering information in formatted text**</span></span>
  
1. <span data-ttu-id="e2fd1-107">Rufen Sie **IMessage::** getattachmentable auf die Anlage Tabelle der Nachricht zugreifen.</span><span class="sxs-lookup"><span data-stu-id="e2fd1-107">Call **IMessage::GetAttachmentTable** to access the message's attachment table.</span></span> <span data-ttu-id="e2fd1-108">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span><span class="sxs-lookup"><span data-stu-id="e2fd1-108">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span></span>
    
2. <span data-ttu-id="e2fd1-109">Erstellen Sie eine Eigenschaftseinschränkung, die die Tabelle auf Zeilen beschränkt, die **PR_RENDERING_POSITION** ungleich-1 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e2fd1-109">Build a property restriction that limits the table to rows that have **PR_RENDERING_POSITION** not equal to -1.</span></span> <span data-ttu-id="e2fd1-110">Weitere Informationen finden Sie unter **PR_RENDERING_POSITION** ([pidtagrenderingposition (](pidtagrenderingposition-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e2fd1-110">For more information, see **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="e2fd1-111">Rufen Sie **IMAPITable:: Restrict** auf, um die Einschränkung zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="e2fd1-111">Call **IMAPITable::Restrict** to enforce the restriction.</span></span> <span data-ttu-id="e2fd1-112">Weitere Informationen finden Sie unter [IMAPITable:: Restrict](imapitable-restrict.md).</span><span class="sxs-lookup"><span data-stu-id="e2fd1-112">For more information, see [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
    
4. <span data-ttu-id="e2fd1-113">Rufen Sie **IMAPITable:: sortable** auf, um die Anlagen zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="e2fd1-113">Call **IMAPITable::SortTable** to sort the attachments.</span></span> <span data-ttu-id="e2fd1-114">Weitere Informationen finden Sie unter [IMAPITable:: sortable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="e2fd1-114">For more information, see [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
5. <span data-ttu-id="e2fd1-115">Rufen Sie **IMAPITable:: QueryRows** auf, um die entsprechenden Zeilen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e2fd1-115">Call **IMAPITable::QueryRows** to retrieve the appropriate rows.</span></span> <span data-ttu-id="e2fd1-116">Weitere Informationen finden Sie unter [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="e2fd1-116">For more information, see [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
    
6. <span data-ttu-id="e2fd1-117">Rufen Sie die **IMAPIProp:: OpenProperty** -Methode der Nachricht auf, um **PR_RTF_COMPRESSED** mit der **IStream** -Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e2fd1-117">Call the message's **IMAPIProp::OpenProperty** method to retrieve **PR_RTF_COMPRESSED** with the **IStream** interface.</span></span> <span data-ttu-id="e2fd1-118">Weitere Informationen finden Sie unter [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) und **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="e2fd1-118">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
    
7. <span data-ttu-id="e2fd1-119">Überprüfen Sie den Stream, und suchen Sie nach `\objattph`dem Render-Platzhalter.</span><span class="sxs-lookup"><span data-stu-id="e2fd1-119">Scan the stream, looking for the rendering placeholder,  `\objattph`.</span></span> <span data-ttu-id="e2fd1-120">Das Zeichen nach diesem Platzhalter ist die Stelle für die nächste Anlage in der sortierten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e2fd1-120">The character following this placeholder is the place for the next attachment in the sorted table.</span></span>
    

