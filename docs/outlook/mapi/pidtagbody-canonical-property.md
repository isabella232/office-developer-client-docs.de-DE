---
title: Kanonische PidTagBody-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBody
api_type:
- HeaderDef
ms.assetid: 47c0d0fe-4d57-4b81-bdb5-336de85c194c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 23d943d5576f5e9d7694b03c90dea79a878dee64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794134"
---
# <a name="pidtagbody-canonical-property"></a><span data-ttu-id="a8f41-103">Kanonische PidTagBody-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a8f41-103">PidTagBody Canonical Property</span></span>

  
  
<span data-ttu-id="a8f41-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a8f41-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a8f41-105">Enthält den Nachrichtentext.</span><span class="sxs-lookup"><span data-stu-id="a8f41-105">Contains the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a8f41-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a8f41-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a8f41-107">PR_BODY, PR_BODY_A, PR_BODY_W</span><span class="sxs-lookup"><span data-stu-id="a8f41-107">PR_BODY, PR_BODY_A, PR_BODY_W</span></span>  <br/> |
|<span data-ttu-id="a8f41-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="a8f41-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a8f41-109">0 x 1000</span><span class="sxs-lookup"><span data-stu-id="a8f41-109">0x1000</span></span>  <br/> |
|<span data-ttu-id="a8f41-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a8f41-110">Data type:</span></span>  <br/> |<span data-ttu-id="a8f41-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="a8f41-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="a8f41-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a8f41-112">Area:</span></span>  <br/> |<span data-ttu-id="a8f41-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="a8f41-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8f41-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a8f41-114">Remarks</span></span>

<span data-ttu-id="a8f41-115">Diese Eigenschaften werden in der Regel nur in einer zwischen Personen Nachricht (IPM) verwendet.</span><span class="sxs-lookup"><span data-stu-id="a8f41-115">These properties are typically used only in an interpersonal message (IPM).</span></span> 
  
<span data-ttu-id="a8f41-116">Nachrichtenspeicher, die Rich Text Format (RTF) unterstützen ignorieren Änderungen an Leerzeichen im Nachrichtentext.</span><span class="sxs-lookup"><span data-stu-id="a8f41-116">Message stores that support Rich Text Format (RTF) ignore any changes to white space in the message text.</span></span> <span data-ttu-id="a8f41-117">Wenn **PR_BODY** zum ersten Mal gespeichert wird, wird der Nachrichtenspeicher auch generiert und speichert die RTF-Version des Texts Message-Eigenschaft **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a8f41-117">When **PR_BODY** is stored for the first time, the message store also generates and stores the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the RTF version of the message text.</span></span> <span data-ttu-id="a8f41-118">Wenn später die [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode aufgerufen wird und **PR_BODY** geändert wurde, ruft der Nachrichtenspeicher die [RTFSync](rtfsync.md) -Funktion, um die Synchronisierung mit der RTF-Version sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="a8f41-118">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="a8f41-119">Wenn nur Leerzeichen geändert wurde, werden die Eigenschaften left unverändert.</span><span class="sxs-lookup"><span data-stu-id="a8f41-119">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="a8f41-120">Dadurch bleibt erhalten alle nicht trivialen RTF Formatierung beim Clients RTF nicht unterstützen die Nachricht durchläuft und messaging-Systeme.</span><span class="sxs-lookup"><span data-stu-id="a8f41-120">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
<span data-ttu-id="a8f41-121">Der Wert für diese Eigenschaft muss in der Codepage des Betriebssystems ausgedrückt werden, die MAPI ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8f41-121">The value for this property must be expressed in the code page of the operating system that MAPI is running on.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a8f41-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a8f41-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a8f41-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a8f41-123">Protocol specifications</span></span>

<span data-ttu-id="a8f41-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8f41-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8f41-125">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="a8f41-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a8f41-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8f41-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8f41-127">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="a8f41-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a8f41-128">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="a8f41-128">Header files</span></span>

<span data-ttu-id="a8f41-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a8f41-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="a8f41-130">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a8f41-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="a8f41-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a8f41-131">Mapitags.h</span></span>
  
> <span data-ttu-id="a8f41-132">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a8f41-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a8f41-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8f41-133">See also</span></span>



[<span data-ttu-id="a8f41-134">Kanonische PidTagRtfInSync-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a8f41-134">PidTagRtfInSync Canonical Property</span></span>](pidtagrtfinsync-canonical-property.md)


[<span data-ttu-id="a8f41-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8f41-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a8f41-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8f41-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a8f41-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a8f41-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a8f41-138">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a8f41-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

