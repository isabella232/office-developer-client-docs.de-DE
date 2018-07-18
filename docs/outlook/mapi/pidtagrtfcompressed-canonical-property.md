---
title: PidTagRtfCompressed (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfCompressed
api_type:
- COM
ms.assetid: fd0ccb88-55ce-4d7c-9573-6e5d6239b6a8
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c93d850551e766e97292d5417c3be5577f557af0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795005"
---
# <a name="pidtagrtfcompressed-canonical-property"></a><span data-ttu-id="6e6f9-103">PidTagRtfCompressed (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6e6f9-103">PidTagRtfCompressed Canonical Property</span></span>

  
  
<span data-ttu-id="6e6f9-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6e6f9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6e6f9-105">Die Rich Text Format (RTF) Version des Texts Nachricht in der Regel in komprimierter Form enthält.</span><span class="sxs-lookup"><span data-stu-id="6e6f9-105">Contains the Rich Text Format (RTF) version of the message text, usually in compressed form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6e6f9-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6e6f9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6e6f9-107">PR_RTF_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="6e6f9-107">PR_RTF_COMPRESSED</span></span>  <br/> |
|<span data-ttu-id="6e6f9-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="6e6f9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6e6f9-109">0 x 1009</span><span class="sxs-lookup"><span data-stu-id="6e6f9-109">0x1009</span></span>  <br/> |
|<span data-ttu-id="6e6f9-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6e6f9-110">Data type:</span></span>  <br/> |<span data-ttu-id="6e6f9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6e6f9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6e6f9-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6e6f9-112">Area:</span></span>  <br/> |<span data-ttu-id="6e6f9-113">E-Mail</span><span class="sxs-lookup"><span data-stu-id="6e6f9-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e6f9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e6f9-114">Remarks</span></span>

<span data-ttu-id="6e6f9-115">Diese Eigenschaft enthält den gleichen Nachrichtentext als **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft, aber in RTF.</span><span class="sxs-lookup"><span data-stu-id="6e6f9-115">This property contains the same message text as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property but in RTF.</span></span> 
  
<span data-ttu-id="6e6f9-116">Nachrichtentext in RTF wird normalerweise in komprimierter Form gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6e6f9-116">Message text in RTF is normally stored in compressed form.</span></span> <span data-ttu-id="6e6f9-117">Einige Systeme komprimieren formatierten Text jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="6e6f9-117">However, some systems do not compress formatted text.</span></span> <span data-ttu-id="6e6f9-118">Um diese zu unterstützen, stellt MAPI den DwMagicUncompressedRTF Wert für eine Kopfzeile Stream zum Identifizieren der nicht komprimierten RTF und das Flag **STORE_UNCOMPRESSED_RTF** in **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) für die Nachricht Speichern Sie, um darauf hinzuweisen, dass es nicht komprimierten RTF gespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6e6f9-118">To accommodate them, MAPI provides the dwMagicUncompressedRTF value for a stream header to identify uncompressed RTF, and the **STORE_UNCOMPRESSED_RTF** flag in **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) for the message store to indicate it can store uncompressed RTF.</span></span> 
  
<span data-ttu-id="6e6f9-119">Um den Inhalt dieser Eigenschaft abzurufen, **OpenProperty**und anschließend rufen Sie [WrapCompressedRTFStream](wrapcompressedrtfstream.md) mit dem **MAPI_READ** -Flag auf.</span><span class="sxs-lookup"><span data-stu-id="6e6f9-119">To obtain the contents of this property, call **OpenProperty**, then call [WrapCompressedRTFStream](wrapcompressedrtfstream.md) with the **MAPI_READ** flag.</span></span> <span data-ttu-id="6e6f9-120">Um diese Eigenschaft zu schreiben, öffnen Sie es mit den Flags **MAPI_MODIFY** und **MAPI_CREATE ist** .</span><span class="sxs-lookup"><span data-stu-id="6e6f9-120">To write into this property, open it with the **MAPI_MODIFY** and **MAPI_CREATE** flags.</span></span> <span data-ttu-id="6e6f9-121">Dadurch wird sichergestellt, dass die neuen Daten vollständig alle alten Daten ersetzen und schreibt die mit der Mindestanzahl von Store-Updates durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6e6f9-121">This ensures that the new data completely replace any old data and that the writes are performed using the minimum number of store updates.</span></span> 
  
<span data-ttu-id="6e6f9-122">Nachrichtenspeicher, die RTF unterstützen ignorieren Änderungen an Leerzeichen im Nachrichtentext.</span><span class="sxs-lookup"><span data-stu-id="6e6f9-122">Message stores that support RTF ignore any changes to white space in the message text.</span></span> <span data-ttu-id="6e6f9-123">Wenn **PR_BODY** zum ersten Mal gespeichert wird, wird der Nachrichtenspeicher auch generiert und speichert diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6e6f9-123">When **PR_BODY** is stored for the first time, the message store also generates and stores this property.</span></span> <span data-ttu-id="6e6f9-124">Wenn später die [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode aufgerufen wird und **PR_BODY** geändert wurde, ruft der Nachrichtenspeicher die [RTFSync](rtfsync.md) -Funktion, um die Synchronisierung mit der RTF-Version sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="6e6f9-124">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="6e6f9-125">Wenn nur Leerzeichen geändert wurde, werden die Eigenschaften left unverändert.</span><span class="sxs-lookup"><span data-stu-id="6e6f9-125">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="6e6f9-126">Dadurch bleibt erhalten alle nicht trivialen RTF Formatierung beim Clients RTF nicht unterstützen die Nachricht durchläuft und messaging-Systeme.</span><span class="sxs-lookup"><span data-stu-id="6e6f9-126">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6e6f9-127">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6e6f9-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6e6f9-128">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="6e6f9-128">Protocol specifications</span></span>

<span data-ttu-id="6e6f9-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e6f9-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e6f9-130">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="6e6f9-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6e6f9-131">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e6f9-131">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e6f9-132">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="6e6f9-132">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="6e6f9-133">[[MS-OXRTFCP]](http://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e6f9-133">[[MS-OXRTFCP]](http://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e6f9-134">Codiert und decodiert einen komprimierten Datenstrom im RTF-Nachrichtentexte.</span><span class="sxs-lookup"><span data-stu-id="6e6f9-134">Encodes and decodes a compressed stream in RTF message bodies.</span></span>
    
<span data-ttu-id="6e6f9-135">[[MS-OXRTFEX]](http://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e6f9-135">[[MS-OXRTFEX]](http://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e6f9-136">Kapselt zusätzliche Content-Formate (wie HTML) in die Body-Eigenschaft von RTF-Nachrichten und Anlagen.</span><span class="sxs-lookup"><span data-stu-id="6e6f9-136">Encapsulates additional content formats (such as HTML) within the RTF body property of messages and attachments.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6e6f9-137">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="6e6f9-137">Header files</span></span>

<span data-ttu-id="6e6f9-138">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6e6f9-138">Mapidefs.h</span></span>
  
> <span data-ttu-id="6e6f9-139">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6e6f9-139">Provides data type definitions.</span></span>
    
<span data-ttu-id="6e6f9-140">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6e6f9-140">Mapitags.h</span></span>
  
> <span data-ttu-id="6e6f9-141">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6e6f9-141">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6e6f9-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e6f9-142">See also</span></span>



[<span data-ttu-id="6e6f9-143">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e6f9-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6e6f9-144">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e6f9-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6e6f9-145">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6e6f9-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6e6f9-146">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6e6f9-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

