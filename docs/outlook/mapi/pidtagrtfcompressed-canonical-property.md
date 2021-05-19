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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3091a76a1b755bf5a0d641ed9bd79bcfaa4641b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357890"
---
# <a name="pidtagrtfcompressed-canonical-property"></a><span data-ttu-id="fe761-103">PidTagRtfCompressed (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fe761-103">PidTagRtfCompressed Canonical Property</span></span>

  
  
<span data-ttu-id="fe761-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe761-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe761-105">Enthält die Rich Text Format (RTF)-Version des Nachrichtentexts, in der Regel in komprimierter Form.</span><span class="sxs-lookup"><span data-stu-id="fe761-105">Contains the Rich Text Format (RTF) version of the message text, usually in compressed form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fe761-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="fe761-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fe761-107">PR_RTF_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="fe761-107">PR_RTF_COMPRESSED</span></span>  <br/> |
|<span data-ttu-id="fe761-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="fe761-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fe761-109">0x1009</span><span class="sxs-lookup"><span data-stu-id="fe761-109">0x1009</span></span>  <br/> |
|<span data-ttu-id="fe761-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="fe761-110">Data type:</span></span>  <br/> |<span data-ttu-id="fe761-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fe761-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fe761-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="fe761-112">Area:</span></span>  <br/> |<span data-ttu-id="fe761-113">E-Mails</span><span class="sxs-lookup"><span data-stu-id="fe761-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe761-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fe761-114">Remarks</span></span>

<span data-ttu-id="fe761-115">Diese Eigenschaft enthält denselben Nachrichtentext wie die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) -Eigenschaft, aber in RTF.</span><span class="sxs-lookup"><span data-stu-id="fe761-115">This property contains the same message text as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property but in RTF.</span></span> 
  
<span data-ttu-id="fe761-116">Nachrichtentext in RTF wird normalerweise in komprimierter Form gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fe761-116">Message text in RTF is normally stored in compressed form.</span></span> <span data-ttu-id="fe761-117">In einigen Systemen wird formatierter Text jedoch nicht komprimiert.</span><span class="sxs-lookup"><span data-stu-id="fe761-117">However, some systems do not compress formatted text.</span></span> <span data-ttu-id="fe761-118">Um sie zu unterstützen, stellt MAPI den wert dwMagicUncompressedRTF für einen Datenstromheader zur Identifizierung nicht komprimierter RTF und das **STORE_UNCOMPRESSED_RTF-Flag** in **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) für den Nachrichtenspeicher zur Angabe, dass nicht komprimiertes RTF gespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="fe761-118">To accommodate them, MAPI provides the dwMagicUncompressedRTF value for a stream header to identify uncompressed RTF, and the **STORE_UNCOMPRESSED_RTF** flag in **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) for the message store to indicate it can store uncompressed RTF.</span></span> 
  
<span data-ttu-id="fe761-119">Um den Inhalt dieser Eigenschaft zu erhalten, rufen **Sie OpenProperty** auf, und rufen Sie [wrapCompressedRTFStream](wrapcompressedrtfstream.md) mit dem MAPI_READ **auf.**</span><span class="sxs-lookup"><span data-stu-id="fe761-119">To obtain the contents of this property, call **OpenProperty**, then call [WrapCompressedRTFStream](wrapcompressedrtfstream.md) with the **MAPI_READ** flag.</span></span> <span data-ttu-id="fe761-120">Um in diese Eigenschaft zu schreiben, öffnen Sie sie **mit** den MAPI_MODIFY und **MAPI_CREATE** Flags.</span><span class="sxs-lookup"><span data-stu-id="fe761-120">To write into this property, open it with the **MAPI_MODIFY** and **MAPI_CREATE** flags.</span></span> <span data-ttu-id="fe761-121">Dadurch wird sichergestellt, dass die neuen Daten alle alten Daten vollständig ersetzen und dass die Schreibvorgänge mithilfe der Mindestanzahl von Speicherupdates ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fe761-121">This ensures that the new data completely replace any old data and that the writes are performed using the minimum number of store updates.</span></span> 
  
<span data-ttu-id="fe761-122">Nachrichtenspeicher, die RTF unterstützen, ignorieren alle Änderungen an Leerzeichen im Nachrichtentext.</span><span class="sxs-lookup"><span data-stu-id="fe761-122">Message stores that support RTF ignore any changes to white space in the message text.</span></span> <span data-ttu-id="fe761-123">Wenn **PR_BODY** zum ersten Mal gespeichert wird, generiert und speichert der Nachrichtenspeicher auch diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="fe761-123">When **PR_BODY** is stored for the first time, the message store also generates and stores this property.</span></span> <span data-ttu-id="fe761-124">Wenn die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) anschließend aufgerufen wird und **PR_BODY** geändert wurde, ruft der Nachrichtenspeicher die [RTFSync-Funktion](rtfsync.md) auf, um die Synchronisierung mit der RTF-Version sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="fe761-124">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="fe761-125">Wenn nur Leerzeichen geändert wurden, bleiben die Eigenschaften unverändert.</span><span class="sxs-lookup"><span data-stu-id="fe761-125">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="fe761-126">Dadurch wird jede nichttriviale RTF-Formatierung beibehalten, wenn die Nachricht über nicht RTF-wahrneige Clients und Messagingsysteme geht.</span><span class="sxs-lookup"><span data-stu-id="fe761-126">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fe761-127">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fe761-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fe761-128">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="fe761-128">Protocol specifications</span></span>

<span data-ttu-id="fe761-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe761-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fe761-130">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="fe761-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fe761-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe761-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fe761-132">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="fe761-132">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="fe761-133">[[MS-OXRTFCP]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe761-133">[[MS-OXRTFCP]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fe761-134">Codiert und decodiert einen komprimierten Datenstrom in RTF-Nachrichtentexten.</span><span class="sxs-lookup"><span data-stu-id="fe761-134">Encodes and decodes a compressed stream in RTF message bodies.</span></span>
    
<span data-ttu-id="fe761-135">[[MS-OXRTFEX]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe761-135">[[MS-OXRTFEX]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fe761-136">Kapselt zusätzliche Inhaltsformate (z. B. HTML) innerhalb der RTF-Body-Eigenschaft von Nachrichten und Anlagen.</span><span class="sxs-lookup"><span data-stu-id="fe761-136">Encapsulates additional content formats (such as HTML) within the RTF body property of messages and attachments.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fe761-137">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="fe761-137">Header files</span></span>

<span data-ttu-id="fe761-138">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fe761-138">Mapidefs.h</span></span>
  
> <span data-ttu-id="fe761-139">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="fe761-139">Provides data type definitions.</span></span>
    
<span data-ttu-id="fe761-140">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fe761-140">Mapitags.h</span></span>
  
> <span data-ttu-id="fe761-141">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="fe761-141">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fe761-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe761-142">See also</span></span>



[<span data-ttu-id="fe761-143">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe761-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fe761-144">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="fe761-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fe761-145">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="fe761-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fe761-146">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="fe761-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

