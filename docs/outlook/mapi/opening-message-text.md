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
ms.openlocfilehash: 7a2dbe8d2143fd330ae1f5ca5804e30b79909576
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569408"
---
# <a name="opening-message-text"></a><span data-ttu-id="5f7b9-103">Öffnen des Nachrichtentexts</span><span class="sxs-lookup"><span data-stu-id="5f7b9-103">Opening message text</span></span>

<span data-ttu-id="5f7b9-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f7b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f7b9-105">Der Text einer Nachricht gespeichert ist entweder in seiner **PR\_BODY** Eigenschaft oder **PR\_RTF\_komprimierte** Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5f7b9-105">The text of a message is stored either in its **PR\_BODY** property or **PR\_RTF\_COMPRESSED** property.</span></span> <span data-ttu-id="5f7b9-106">Weitere Informationen finden Sie unter **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) und **PR\_RTF\_komprimierte** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5f7b9-106">For more information, see **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR\_RTF\_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="5f7b9-107">Wenn Sie die Rich Text Format (RTF) unterstützen, öffnen **PR\_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="5f7b9-107">If you support the Rich Text Format (RTF), open **PR\_RTF_COMPRESSED**.</span></span> <span data-ttu-id="5f7b9-108">Wenn Sie keine RTF unterstützen, öffnen **PR\_BODY**.</span><span class="sxs-lookup"><span data-stu-id="5f7b9-108">If you do not support RTF, open **PR\_BODY**.</span></span> <span data-ttu-id="5f7b9-109">Der Text einer Nachricht kann werden große unabhängig davon, ob es formatiert ist, verwenden Sie **IMAPIProp::OpenProperty** , um diese Eigenschaften zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5f7b9-109">Because the text of a message can be large regardless of whether or not it is formatted, use **IMAPIProp::OpenProperty** to open these properties.</span></span> <span data-ttu-id="5f7b9-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="5f7b9-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
  
### <a name="to-display-formatted-message-text"></a><span data-ttu-id="5f7b9-111">Anzeigen formatierter Nachrichtentext</span><span class="sxs-lookup"><span data-stu-id="5f7b9-111">To display formatted message text</span></span>
  
1. <span data-ttu-id="5f7b9-112">Wenn Sie einen bewusst nicht RTF-Nachrichtenspeicher verwenden, wie durch die Abwesenheit des STORE_RTF_OK-Flags in den Speicher **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft angegeben:</span><span class="sxs-lookup"><span data-stu-id="5f7b9-112">If you are using a non-RTF aware message store, as indicated by the absence of the STORE_RTF_OK flag in the store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
    
    1. <span data-ttu-id="5f7b9-113">Rufen Sie die Nachricht **IMAPIProp::GetProps** -Methode zum Abrufen der **PR_RTF_IN_SYNC** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5f7b9-113">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_RTF_IN_SYNC** property.</span></span> <span data-ttu-id="5f7b9-114">Weitere Informationen finden Sie unter [IMAPIProp::GetProps](imapiprop-getprops.md) und **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5f7b9-114">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="5f7b9-115">Rufen Sie RTFSync, um die Nachricht PR_BODY-Eigenschaft mit der **PR_RTF_COMPRESSED** -Eigenschaft zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="5f7b9-115">Call RTFSync to synchronize the message's PR_BODY property with the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="5f7b9-116">Weitere Informationen finden Sie unter [RTFSync](rtfsync.md), **PR_BODY**und **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="5f7b9-116">For more information, see [RTFSync](rtfsync.md), **PR_BODY**, and **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="5f7b9-117">Übergeben Sie die RTF_SYNC_BODY_CHANGED kennzeichnen, wenn die Aufrufs zum Abrufen von **PR_RTF_IN_SYNC** ist fehlgeschlagen, da die Eigenschaft nicht vorhanden ist, oder es ist auf FALSE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5f7b9-117">Pass the RTF_SYNC_BODY_CHANGED flag if the call to retrieve **PR_RTF_IN_SYNC** failed because the property does not exist or it is set to FALSE.</span></span> 
        
    3. <span data-ttu-id="5f7b9-118">Wenn **RTFSync** den Wert TRUE zurückgegeben, was bedeutet, dass Änderungen vorgenommen wurden – rufen Sie die Nachricht **IMAPIProp::SaveChanges** -Methode, um sie dauerhaft zu speichern.</span><span class="sxs-lookup"><span data-stu-id="5f7b9-118">If **RTFSync** returned TRUE — indicating that changes were made — call the message's **IMAPIProp::SaveChanges** method to permanently store them.</span></span> <span data-ttu-id="5f7b9-119">Weitere Informationen finden Sie unter [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="5f7b9-119">For more information, see [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
2. <span data-ttu-id="5f7b9-120">Speichern Sie unabhängig davon, ob Sie eine RTF-fähigen Nachricht verwenden:</span><span class="sxs-lookup"><span data-stu-id="5f7b9-120">Regardless of whether or not you are using an RTF-aware message store:</span></span>
    
    1. <span data-ttu-id="5f7b9-121">Rufen Sie **IMAPIProp::OpenProperty** , um die **PR_RTF_COMPRESSED** -Eigenschaft zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5f7b9-121">Call **IMAPIProp::OpenProperty** to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="5f7b9-122">Weitere Informationen finden Sie unter [IMAPIProp::OpenProperty](imapiprop-openproperty.md) und **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="5f7b9-122">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
        
    2. <span data-ttu-id="5f7b9-123">Wenn **PR_RTF_COMPRESSED** nicht verfügbar ist, rufen Sie **OpenProperty** , um die **PR_BODY** -Eigenschaft zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5f7b9-123">If **PR_RTF_COMPRESSED** is not available, call **OpenProperty** to open the **PR_BODY** property.</span></span> 
        
    3. <span data-ttu-id="5f7b9-124">Rufen Sie die **WrapCompressedRTFStream** -Funktion, um eine nicht komprimierten Version der komprimierten RTF-Daten zu erstellen, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5f7b9-124">Call the **WrapCompressedRTFStream** function to create an uncompressed version of the compressed RTF data, if available.</span></span> <span data-ttu-id="5f7b9-125">Weitere Informationen finden Sie unter [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span><span class="sxs-lookup"><span data-stu-id="5f7b9-125">For more information, see [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span></span>
        
    4. <span data-ttu-id="5f7b9-126">Kopieren des formatierten Texts aus dem Stream an der entsprechenden Stelle in das Nachrichtenformular.</span><span class="sxs-lookup"><span data-stu-id="5f7b9-126">Copy the formatted text from the stream to the appropriate place in the message form.</span></span> 
    
### <a name="to-display-plain-message-text"></a><span data-ttu-id="5f7b9-127">Einfache Meldungstext angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5f7b9-127">To display plain message text</span></span>
  
1. <span data-ttu-id="5f7b9-128">Rufen Sie die Nachricht **IMAPIProp::GetProps** -Methode zum Abrufen der **PR_BODY** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5f7b9-128">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_BODY** property.</span></span> <span data-ttu-id="5f7b9-129">Weitere Informationen finden Sie unter [IMAPIProp::GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="5f7b9-129">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
    
2. <span data-ttu-id="5f7b9-130">Wenn **GetProps** entweder PT_ERROR für den Eigenschaftentyp in der Eigenschaft Wert Struktur oder MAPI_E_NOT_ENOUGH_MEMORY zurückgibt, rufen Sie die Nachricht **IMAPIProp::OpenProperty** -Methode.</span><span class="sxs-lookup"><span data-stu-id="5f7b9-130">If **GetProps** returns either PT_ERROR for the property type in the property value structure or MAPI_E_NOT_ENOUGH_MEMORY, call the message's **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="5f7b9-131">Übergeben Sie **PR_BODY** als Eigenschafts-Tag und IID_IStream als Schnittstellenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="5f7b9-131">Pass **PR_BODY** as the property tag and IID_IStream as the interface identifier.</span></span> <span data-ttu-id="5f7b9-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="5f7b9-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
3. <span data-ttu-id="5f7b9-133">Kopieren Sie die nur-Text aus dem Stream an der entsprechenden Stelle in das Nachrichtenformular.</span><span class="sxs-lookup"><span data-stu-id="5f7b9-133">Copy the plain text from the stream to the appropriate place in the message form.</span></span> 
    

