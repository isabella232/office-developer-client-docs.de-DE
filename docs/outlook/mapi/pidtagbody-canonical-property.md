---
title: PidTagBody (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 243a59798980d8c0cfaf1a726d6408dbd66ebba8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326635"
---
# <a name="pidtagbody-canonical-property"></a><span data-ttu-id="236ff-103">PidTagBody (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="236ff-103">PidTagBody Canonical Property</span></span>

  
  
<span data-ttu-id="236ff-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="236ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="236ff-105">Enthält den Nachrichtentext.</span><span class="sxs-lookup"><span data-stu-id="236ff-105">Contains the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="236ff-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="236ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="236ff-107">PR_BODY, PR_BODY_A, PR_BODY_W</span><span class="sxs-lookup"><span data-stu-id="236ff-107">PR_BODY, PR_BODY_A, PR_BODY_W</span></span>  <br/> |
|<span data-ttu-id="236ff-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="236ff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="236ff-109">0x1000</span><span class="sxs-lookup"><span data-stu-id="236ff-109">0x1000</span></span>  <br/> |
|<span data-ttu-id="236ff-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="236ff-110">Data type:</span></span>  <br/> |<span data-ttu-id="236ff-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="236ff-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="236ff-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="236ff-112">Area:</span></span>  <br/> |<span data-ttu-id="236ff-113">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="236ff-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="236ff-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="236ff-114">Remarks</span></span>

<span data-ttu-id="236ff-115">Diese Eigenschaften werden in der Regel nur in einer zwischenpersönlichen Nachricht (IPM) verwendet.</span><span class="sxs-lookup"><span data-stu-id="236ff-115">These properties are typically used only in an interpersonal message (IPM).</span></span> 
  
<span data-ttu-id="236ff-116">Nachrichtenspeicher, die Rich Text Format (RTF) unterstützen, ignorieren alle Änderungen an Leerzeichen im Nachrichtentext.</span><span class="sxs-lookup"><span data-stu-id="236ff-116">Message stores that support Rich Text Format (RTF) ignore any changes to white space in the message text.</span></span> <span data-ttu-id="236ff-117">Wenn **PR_BODY** zum ersten Mal gespeichert wird, generiert und speichert der Nachrichtenspeicher auch die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft, die #A0 des Nachrichtentexts.</span><span class="sxs-lookup"><span data-stu-id="236ff-117">When **PR_BODY** is stored for the first time, the message store also generates and stores the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the RTF version of the message text.</span></span> <span data-ttu-id="236ff-118">Wenn die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) anschließend aufgerufen wird und **PR_BODY** geändert wurde, ruft der Nachrichtenspeicher die [RTFSync-Funktion](rtfsync.md) auf, um die Synchronisierung mit der RTF-Version sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="236ff-118">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="236ff-119">Wenn nur Leerzeichen geändert wurden, bleiben die Eigenschaften unverändert.</span><span class="sxs-lookup"><span data-stu-id="236ff-119">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="236ff-120">Dadurch wird jede nichttriviale RTF-Formatierung beibehalten, wenn die Nachricht über nicht RTF-wahrneige Clients und Messagingsysteme geht.</span><span class="sxs-lookup"><span data-stu-id="236ff-120">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
<span data-ttu-id="236ff-121">Der Wert für diese Eigenschaft muss auf der Codeseite des Betriebssystems ausgedrückt werden, auf dem MAPI ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="236ff-121">The value for this property must be expressed in the code page of the operating system that MAPI is running on.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="236ff-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="236ff-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="236ff-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="236ff-123">Protocol specifications</span></span>

<span data-ttu-id="236ff-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="236ff-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="236ff-125">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="236ff-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="236ff-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="236ff-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="236ff-127">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="236ff-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="236ff-128">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="236ff-128">Header files</span></span>

<span data-ttu-id="236ff-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="236ff-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="236ff-130">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="236ff-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="236ff-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="236ff-131">Mapitags.h</span></span>
  
> <span data-ttu-id="236ff-132">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="236ff-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="236ff-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="236ff-133">See also</span></span>



[<span data-ttu-id="236ff-134">PidTagRtfInSync (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="236ff-134">PidTagRtfInSync Canonical Property</span></span>](pidtagrtfinsync-canonical-property.md)


[<span data-ttu-id="236ff-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="236ff-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="236ff-136">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="236ff-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="236ff-137">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="236ff-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="236ff-138">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="236ff-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

