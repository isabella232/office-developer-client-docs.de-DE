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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348580"
---
# <a name="opening-message-text"></a><span data-ttu-id="90823-103">Öffnen des Nachrichtentexts</span><span class="sxs-lookup"><span data-stu-id="90823-103">Opening message text</span></span>

<span data-ttu-id="90823-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90823-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90823-105">Der Text einer Nachricht wird in seiner **PR\_-Body** -Eigenschaft oder **PR\_-RTF\_** -komprimierten Eigenschaft gespeichert.</span><span class="sxs-lookup"><span data-stu-id="90823-105">The text of a message is stored either in its **PR\_BODY** property or **PR\_RTF\_COMPRESSED** property.</span></span> <span data-ttu-id="90823-106">Weitere Informationen finden Sie unter **PR\_-Textkörper** ([pidtagbody (](pidtagbody-canonical-property.md)), **\_PR-HTML** ([pidtaghtml (](pidtaghtml-canonical-property.md)) und **PR\_-\_RTF-Komprimierung** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="90823-106">For more information, see **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR\_RTF\_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="90823-107">Wenn Sie das Rich-Text-Format (RTF) unterstützen, öffnen Sie **PR\_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="90823-107">If you support the Rich Text Format (RTF), open **PR\_RTF_COMPRESSED**.</span></span> <span data-ttu-id="90823-108">Wenn Sie RTF nicht unterstützen, öffnen **Sie\_PR Body**.</span><span class="sxs-lookup"><span data-stu-id="90823-108">If you do not support RTF, open **PR\_BODY**.</span></span> <span data-ttu-id="90823-109">Da der Text einer Nachricht groß sein kann, unabhängig davon, ob Sie formatiert ist, verwenden Sie **IMAPIProp:: OpenProperty** , um diese Eigenschaften zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="90823-109">Because the text of a message can be large regardless of whether or not it is formatted, use **IMAPIProp::OpenProperty** to open these properties.</span></span> <span data-ttu-id="90823-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="90823-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
  
### <a name="to-display-formatted-message-text"></a><span data-ttu-id="90823-111">So zeigen Sie formatierten Nachrichtentext an</span><span class="sxs-lookup"><span data-stu-id="90823-111">To display formatted message text</span></span>
  
1. <span data-ttu-id="90823-112">Wenn Sie einen nicht-RTF-fähigen Nachrichtenspeicher verwenden, wie durch das Fehlen des STORE_RTF_OK-Flags in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft des Stores angegeben:</span><span class="sxs-lookup"><span data-stu-id="90823-112">If you are using a non-RTF aware message store, as indicated by the absence of the STORE_RTF_OK flag in the store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
    
    1. <span data-ttu-id="90823-113">Rufen Sie die **IMAPIProp::** GetProps-Methode der Nachricht auf, um die **PR_RTF_IN_SYNC** -Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="90823-113">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_RTF_IN_SYNC** property.</span></span> <span data-ttu-id="90823-114">Weitere Informationen finden Sie unter [IMAPIProp::](imapiprop-getprops.md) GetProps und **PR_RTF_IN_SYNC** ([pidtagrtfinsync (](pidtagrtfinsync-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="90823-114">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="90823-115">Rufen Sie RTFSync auf, um die PR_BODY-Eigenschaft der Nachricht mit der **PR_RTF_COMPRESSED** -Eigenschaft zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="90823-115">Call RTFSync to synchronize the message's PR_BODY property with the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="90823-116">Weitere Informationen finden Sie unter [RTFSync](rtfsync.md), **PR_BODY**und **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="90823-116">For more information, see [RTFSync](rtfsync.md), **PR_BODY**, and **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="90823-117">Geben Sie das RTF_SYNC_BODY_CHANGED-Flag zurück, wenn der Aufruf von **PR_RTF_IN_SYNC** fehlgeschlagen ist, weil die Eigenschaft nicht vorhanden ist oder auf false festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="90823-117">Pass the RTF_SYNC_BODY_CHANGED flag if the call to retrieve **PR_RTF_IN_SYNC** failed because the property does not exist or it is set to FALSE.</span></span> 
        
    3. <span data-ttu-id="90823-118">Wenn **RTFSync** zurückgegeben wird, was bedeutet, dass Änderungen vorgenommen wurden, rufen Sie die **IMAPIProp:: SaveChanges** -Methode der Nachricht auf, um Sie dauerhaft zu speichern.</span><span class="sxs-lookup"><span data-stu-id="90823-118">If **RTFSync** returned TRUE — indicating that changes were made — call the message's **IMAPIProp::SaveChanges** method to permanently store them.</span></span> <span data-ttu-id="90823-119">Weitere Informationen finden Sie unter [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="90823-119">For more information, see [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
2. <span data-ttu-id="90823-120">Unabhängig davon, ob Sie einen RTF-fähigen Nachrichtenspeicher verwenden oder nicht:</span><span class="sxs-lookup"><span data-stu-id="90823-120">Regardless of whether or not you are using an RTF-aware message store:</span></span>
    
    1. <span data-ttu-id="90823-121">Rufen Sie **IMAPIProp:: OpenProperty** auf, um die **PR_RTF_COMPRESSED** -Eigenschaft zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="90823-121">Call **IMAPIProp::OpenProperty** to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="90823-122">Weitere Informationen finden Sie unter [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) und **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="90823-122">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
        
    2. <span data-ttu-id="90823-123">Wenn **PR_RTF_COMPRESSED** nicht verfügbar ist, rufen \*\*\*\* Sie OpenProperty auf, um die **PR_BODY** -Eigenschaft zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="90823-123">If **PR_RTF_COMPRESSED** is not available, call **OpenProperty** to open the **PR_BODY** property.</span></span> 
        
    3. <span data-ttu-id="90823-124">Rufen Sie die **WrapCompressedRTFStream** -Funktion auf, um eine nicht komprimierte Version der komprimierten RTF-Daten zu erstellen, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="90823-124">Call the **WrapCompressedRTFStream** function to create an uncompressed version of the compressed RTF data, if available.</span></span> <span data-ttu-id="90823-125">Weitere Informationen finden Sie unter [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span><span class="sxs-lookup"><span data-stu-id="90823-125">For more information, see [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span></span>
        
    4. <span data-ttu-id="90823-126">Kopieren Sie den formatierten Text aus dem Stream an die entsprechende Stelle im Nachrichtenformular.</span><span class="sxs-lookup"><span data-stu-id="90823-126">Copy the formatted text from the stream to the appropriate place in the message form.</span></span> 
    
### <a name="to-display-plain-message-text"></a><span data-ttu-id="90823-127">So zeigen Sie reinen Nachrichtentext an</span><span class="sxs-lookup"><span data-stu-id="90823-127">To display plain message text</span></span>
  
1. <span data-ttu-id="90823-128">Rufen Sie die **IMAPIProp::** GetProps-Methode der Nachricht auf, um die **PR_BODY** -Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="90823-128">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_BODY** property.</span></span> <span data-ttu-id="90823-129">Weitere Informationen finden Sie unter [IMAPIProp::](imapiprop-getprops.md)GetProps.</span><span class="sxs-lookup"><span data-stu-id="90823-129">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
    
2. <span data-ttu-id="90823-130">Wenn \*\*\*\* GetProps entweder PT_ERROR für den Eigenschaftentyp in der Eigenschaftswert Struktur oder MAPI_E_NOT_ENOUGH_MEMORY zurückgibt, rufen Sie die **IMAPIProp:: OpenProperty** -Methode der Nachricht auf.</span><span class="sxs-lookup"><span data-stu-id="90823-130">If **GetProps** returns either PT_ERROR for the property type in the property value structure or MAPI_E_NOT_ENOUGH_MEMORY, call the message's **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="90823-131">Übergibt **PR_BODY** als Property-Tag und IID_IStream als Schnittstellenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="90823-131">Pass **PR_BODY** as the property tag and IID_IStream as the interface identifier.</span></span> <span data-ttu-id="90823-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="90823-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
3. <span data-ttu-id="90823-133">Kopieren Sie den nur-Text aus dem Stream an die entsprechende Stelle im Nachrichtenformular.</span><span class="sxs-lookup"><span data-stu-id="90823-133">Copy the plain text from the stream to the appropriate place in the message form.</span></span> 
    

