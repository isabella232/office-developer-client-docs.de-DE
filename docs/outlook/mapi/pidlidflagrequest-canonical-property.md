---
title: PidLidFlagRequest (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagRequest
api_type:
- COM
ms.assetid: 38981f07-14b8-47c2-93df-e6aed91896e4
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: df2e474206559dadf250bdf9a078c69da61187c8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793597"
---
# <a name="pidlidflagrequest-canonical-property"></a><span data-ttu-id="d3c09-103">PidLidFlagRequest (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d3c09-103">PidLidFlagRequest Canonical Property</span></span>

  
  
<span data-ttu-id="d3c09-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d3c09-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d3c09-105">Den Status der einer Besprechungsanfrage darstellt.</span><span class="sxs-lookup"><span data-stu-id="d3c09-105">Represents the status of a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d3c09-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d3c09-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d3c09-107">dispidRequest</span><span class="sxs-lookup"><span data-stu-id="d3c09-107">dispidRequest</span></span>  <br/> |
|<span data-ttu-id="d3c09-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="d3c09-108">Property set:</span></span>  <br/> |<span data-ttu-id="d3c09-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="d3c09-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="d3c09-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="d3c09-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d3c09-111">0x00008530</span><span class="sxs-lookup"><span data-stu-id="d3c09-111">0x00008530</span></span>  <br/> |
|<span data-ttu-id="d3c09-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d3c09-112">Data type:</span></span>  <br/> |<span data-ttu-id="d3c09-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d3c09-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d3c09-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d3c09-114">Area:</span></span>  <br/> |<span data-ttu-id="d3c09-115">Kennzeichnen von</span><span class="sxs-lookup"><span data-stu-id="d3c09-115">Flagging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3c09-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3c09-116">Remarks</span></span>

<span data-ttu-id="d3c09-117">In Microsoft Office Outlook ist eine Besprechungsanfrage ein Terminelement.</span><span class="sxs-lookup"><span data-stu-id="d3c09-117">In Microsoft Office Outlook, a meeting request is an appointment item.</span></span>
  
<span data-ttu-id="d3c09-118">Diese Eigenschaft enthält Benutzer festzulegen Text ein, um das Flag zugeordnet werden und festgelegt werden soll, wenn das Objekt "Message" gekennzeichnet oder abgeschlossen ist, jedoch nicht für ein Objekt bezüglich Besprechungen vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="d3c09-118">This property contains user-specifiable text to be associated with the flag and should be set if the message object is flagged or completed, but should not exist for a meeting-related object.</span></span> <span data-ttu-id="d3c09-119">Clients können nicht für diese Eigenschaft unterstützen und in diese schreiben immer "Nachverfolgung" (übersetzte Sprache des Benutzers, falls zutreffend) als Wert für die Zeichenfolge, wenn diese Eigenschaft festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3c09-119">Clients may choose not to support this property, and always write "Follow up" (translated to the user's language if appropriate) as the value of the string when this property should be set.</span></span> <span data-ttu-id="d3c09-120">Diese Eigenschaft sollte bedingt basierend auf den Werten der **DispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) und **DispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) Eigenschaften ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="d3c09-120">This property should be conditionally ignored based on the values of the **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d3c09-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d3c09-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d3c09-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d3c09-122">Protocol specifications</span></span>

<span data-ttu-id="d3c09-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d3c09-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d3c09-124">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="d3c09-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d3c09-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d3c09-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d3c09-126">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="d3c09-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d3c09-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="d3c09-127">Header files</span></span>

<span data-ttu-id="d3c09-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d3c09-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="d3c09-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d3c09-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d3c09-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3c09-130">See also</span></span>



[<span data-ttu-id="d3c09-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d3c09-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d3c09-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d3c09-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d3c09-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d3c09-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d3c09-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d3c09-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

