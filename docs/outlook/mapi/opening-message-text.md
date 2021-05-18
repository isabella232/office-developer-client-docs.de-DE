---
title: Öffnen des Nachrichtentexts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 305b0534f828ea72c1e116fd38fb8f578062e32e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407536"
---
# <a name="opening-message-text"></a><span data-ttu-id="a60fb-103">Öffnen des Nachrichtentexts</span><span class="sxs-lookup"><span data-stu-id="a60fb-103">Opening message text</span></span>

<span data-ttu-id="a60fb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a60fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a60fb-105">Der Text einer Nachricht wird entweder in der **PR \_ BODY-Eigenschaft** oder **in der PR \_ RTF \_ COMPRESSED-Eigenschaft** gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a60fb-105">The text of a message is stored either in its **PR\_BODY** property or **PR\_RTF\_COMPRESSED** property.</span></span> <span data-ttu-id="a60fb-106">Weitere Informationen finden Sie unter **PR \_ BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR \_ HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) und **PR \_ RTF \_ COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a60fb-106">For more information, see **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR\_RTF\_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="a60fb-107">Wenn Sie das Rich Text Format (RTF) unterstützen, öffnen Sie **pr \_ RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="a60fb-107">If you support the Rich Text Format (RTF), open **PR\_RTF_COMPRESSED**.</span></span> <span data-ttu-id="a60fb-108">Wenn Sie RTF nicht unterstützen, öffnen Sie **PR \_ BODY**.</span><span class="sxs-lookup"><span data-stu-id="a60fb-108">If you do not support RTF, open **PR\_BODY**.</span></span> <span data-ttu-id="a60fb-109">Da der Text einer Nachricht unabhängig davon, ob sie formatiert ist, groß sein kann, verwenden Sie **IMAPIProp::OpenProperty,** um diese Eigenschaften zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a60fb-109">Because the text of a message can be large regardless of whether or not it is formatted, use **IMAPIProp::OpenProperty** to open these properties.</span></span> <span data-ttu-id="a60fb-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="a60fb-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
  
### <a name="to-display-formatted-message-text"></a><span data-ttu-id="a60fb-111">So zeigen Sie formatierten Nachrichtentext an</span><span class="sxs-lookup"><span data-stu-id="a60fb-111">To display formatted message text</span></span>
  
1. <span data-ttu-id="a60fb-112">Wenn Sie einen Nicht-RTF-unterstützenden Nachrichtenspeicher verwenden, wie durch das Fehlen des STORE_RTF_OK-Flag in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft des Speichers angegeben:</span><span class="sxs-lookup"><span data-stu-id="a60fb-112">If you are using a non-RTF aware message store, as indicated by the absence of the STORE_RTF_OK flag in the store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
    
    1. <span data-ttu-id="a60fb-113">Rufen Sie die **IMAPIProp::GetProps-Methode** der Nachricht auf, um die **PR_RTF_IN_SYNC** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a60fb-113">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_RTF_IN_SYNC** property.</span></span> <span data-ttu-id="a60fb-114">Weitere Informationen finden Sie unter [IMAPIProp::GetProps](imapiprop-getprops.md) und **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a60fb-114">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="a60fb-115">Rufen Sie RTFSync auf, um die PR_BODY der Nachricht mit der **PR_RTF_COMPRESSED** zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="a60fb-115">Call RTFSync to synchronize the message's PR_BODY property with the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="a60fb-116">Weitere Informationen finden Sie unter [RTFSync](rtfsync.md), **PR_BODY** und **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="a60fb-116">For more information, see [RTFSync](rtfsync.md), **PR_BODY**, and **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="a60fb-117">Übergeben Sie das RTF_SYNC_BODY_CHANGED, wenn der  Aufruf des PR_RTF_IN_SYNC fehlgeschlagen ist, da die Eigenschaft nicht vorhanden ist oder auf FALSE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a60fb-117">Pass the RTF_SYNC_BODY_CHANGED flag if the call to retrieve **PR_RTF_IN_SYNC** failed because the property does not exist or it is set to FALSE.</span></span> 
        
    3. <span data-ttu-id="a60fb-118">Wenn **RTFSync** TRUE zurückgegeben hat , was angibt, dass Änderungen vorgenommen wurden, rufen Sie die **IMAPIProp::SaveChanges-Methode** der Nachricht auf, um sie dauerhaft zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a60fb-118">If **RTFSync** returned TRUE — indicating that changes were made — call the message's **IMAPIProp::SaveChanges** method to permanently store them.</span></span> <span data-ttu-id="a60fb-119">Weitere Informationen finden Sie unter [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="a60fb-119">For more information, see [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
2. <span data-ttu-id="a60fb-120">Unabhängig davon, ob Sie einen RTF-unterstützten Nachrichtenspeicher verwenden:</span><span class="sxs-lookup"><span data-stu-id="a60fb-120">Regardless of whether or not you are using an RTF-aware message store:</span></span>
    
    1. <span data-ttu-id="a60fb-121">Rufen **Sie IMAPIProp::OpenProperty auf,** um die **PR_RTF_COMPRESSED** öffnen.</span><span class="sxs-lookup"><span data-stu-id="a60fb-121">Call **IMAPIProp::OpenProperty** to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="a60fb-122">Weitere Informationen finden Sie unter [IMAPIProp::OpenProperty](imapiprop-openproperty.md) und **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="a60fb-122">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
        
    2. <span data-ttu-id="a60fb-123">Wenn **PR_RTF_COMPRESSED** nicht verfügbar ist, rufen **Sie OpenProperty auf,** um die **PR_BODY** öffnen.</span><span class="sxs-lookup"><span data-stu-id="a60fb-123">If **PR_RTF_COMPRESSED** is not available, call **OpenProperty** to open the **PR_BODY** property.</span></span> 
        
    3. <span data-ttu-id="a60fb-124">Rufen Sie **die WrapCompressedRTFStream-Funktion auf,** um eine nicht komprimierte Version der komprimierten RTF-Daten zu erstellen, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a60fb-124">Call the **WrapCompressedRTFStream** function to create an uncompressed version of the compressed RTF data, if available.</span></span> <span data-ttu-id="a60fb-125">Weitere Informationen finden Sie unter [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span><span class="sxs-lookup"><span data-stu-id="a60fb-125">For more information, see [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span></span>
        
    4. <span data-ttu-id="a60fb-126">Kopieren Sie den formatierten Text aus dem Datenstrom an die entsprechende Stelle im Nachrichtenformular.</span><span class="sxs-lookup"><span data-stu-id="a60fb-126">Copy the formatted text from the stream to the appropriate place in the message form.</span></span> 
    
### <a name="to-display-plain-message-text"></a><span data-ttu-id="a60fb-127">So zeigen Sie Nur-Nachrichten-Text an</span><span class="sxs-lookup"><span data-stu-id="a60fb-127">To display plain message text</span></span>
  
1. <span data-ttu-id="a60fb-128">Rufen Sie die **IMAPIProp::GetProps-Methode** der Nachricht auf, um die **PR_BODY** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a60fb-128">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_BODY** property.</span></span> <span data-ttu-id="a60fb-129">Weitere Informationen finden Sie unter [IMAPIProp::GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="a60fb-129">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
    
2. <span data-ttu-id="a60fb-130">Wenn **GetProps** entweder PT_ERROR Eigenschaftstyp in der Eigenschaftswertstruktur oder MAPI_E_NOT_ENOUGH_MEMORY zurückgibt, rufen Sie die **IMAPIProp::OpenProperty-Methode** der Nachricht auf.</span><span class="sxs-lookup"><span data-stu-id="a60fb-130">If **GetProps** returns either PT_ERROR for the property type in the property value structure or MAPI_E_NOT_ENOUGH_MEMORY, call the message's **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="a60fb-131">Übergeben **PR_BODY** als Eigenschaftstag und IID_IStream als Schnittstellenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="a60fb-131">Pass **PR_BODY** as the property tag and IID_IStream as the interface identifier.</span></span> <span data-ttu-id="a60fb-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="a60fb-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
3. <span data-ttu-id="a60fb-133">Kopieren Sie den Nur-Text aus dem Datenstrom an die entsprechende Stelle im Nachrichtenformular.</span><span class="sxs-lookup"><span data-stu-id="a60fb-133">Copy the plain text from the stream to the appropriate place in the message form.</span></span> 
    

