---
title: Kanonische Pidtagbody (-Eigenschaft
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
ms.openlocfilehash: 243a59798980d8c0cfaf1a726d6408dbd66ebba8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326635"
---
# <a name="pidtagbody-canonical-property"></a><span data-ttu-id="c7786-103">Kanonische Pidtagbody (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c7786-103">PidTagBody Canonical Property</span></span>

  
  
<span data-ttu-id="c7786-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7786-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7786-105">Enthält den Nachrichtentext.</span><span class="sxs-lookup"><span data-stu-id="c7786-105">Contains the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c7786-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c7786-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c7786-107">PR_BODY, PR_BODY_A, PR_BODY_W</span><span class="sxs-lookup"><span data-stu-id="c7786-107">PR_BODY, PR_BODY_A, PR_BODY_W</span></span>  <br/> |
|<span data-ttu-id="c7786-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="c7786-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c7786-109">0x1000</span><span class="sxs-lookup"><span data-stu-id="c7786-109">0x1000</span></span>  <br/> |
|<span data-ttu-id="c7786-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c7786-110">Data type:</span></span>  <br/> |<span data-ttu-id="c7786-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="c7786-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="c7786-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c7786-112">Area:</span></span>  <br/> |<span data-ttu-id="c7786-113">Allgemeine Nachrichtenübermittlung</span><span class="sxs-lookup"><span data-stu-id="c7786-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7786-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7786-114">Remarks</span></span>

<span data-ttu-id="c7786-115">Diese Eigenschaften werden in der Regel nur in einer zwischenmenschlichen Nachricht (IPM) verwendet.</span><span class="sxs-lookup"><span data-stu-id="c7786-115">These properties are typically used only in an interpersonal message (IPM).</span></span> 
  
<span data-ttu-id="c7786-116">Nachrichtenspeicher, die Rich-Text-Format (RTF) unterstützen, ignorieren alle Änderungen an Leerzeichen im Nachrichten Text.</span><span class="sxs-lookup"><span data-stu-id="c7786-116">Message stores that support Rich Text Format (RTF) ignore any changes to white space in the message text.</span></span> <span data-ttu-id="c7786-117">Wenn **PR_BODY** zum ersten Mal gespeichert wird, generiert und speichert der Nachrichtenspeicher auch die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft, die RTF-Version des Nachrichtentexts.</span><span class="sxs-lookup"><span data-stu-id="c7786-117">When **PR_BODY** is stored for the first time, the message store also generates and stores the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the RTF version of the message text.</span></span> <span data-ttu-id="c7786-118">Wenn die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode anschließend aufgerufen wird und **PR_BODY** geändert wurde, ruft der Nachrichtenspeicher die [RTFSync](rtfsync.md) -Funktion auf, um die Synchronisierung mit der RTF-Version sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="c7786-118">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="c7786-119">Wenn nur Leerraum geändert wurde, bleiben die Eigenschaften unverändert.</span><span class="sxs-lookup"><span data-stu-id="c7786-119">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="c7786-120">Dadurch werden alle nicht trivialen RTF-Formatierungen beibehalten, wenn die Nachricht über nicht-RTF-fähige Clients und Messagingsysteme reist.</span><span class="sxs-lookup"><span data-stu-id="c7786-120">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
<span data-ttu-id="c7786-121">Der Wert für diese Eigenschaft muss auf der Codepage des Betriebssystems ausgedrückt werden, auf dem MAPI läuft.</span><span class="sxs-lookup"><span data-stu-id="c7786-121">The value for this property must be expressed in the code page of the operating system that MAPI is running on.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c7786-122">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c7786-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c7786-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c7786-123">Protocol specifications</span></span>

<span data-ttu-id="c7786-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7786-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7786-125">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c7786-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c7786-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7786-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7786-127">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="c7786-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c7786-128">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="c7786-128">Header files</span></span>

<span data-ttu-id="c7786-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c7786-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="c7786-130">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="c7786-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="c7786-131">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="c7786-131">Mapitags.h</span></span>
  
> <span data-ttu-id="c7786-132">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="c7786-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c7786-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7786-133">See also</span></span>



[<span data-ttu-id="c7786-134">Kanonische Pidtagrtfinsync (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c7786-134">PidTagRtfInSync Canonical Property</span></span>](pidtagrtfinsync-canonical-property.md)


[<span data-ttu-id="c7786-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c7786-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c7786-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c7786-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c7786-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c7786-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c7786-138">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c7786-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

