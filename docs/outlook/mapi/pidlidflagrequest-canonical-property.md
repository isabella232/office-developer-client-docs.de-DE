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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4a2bcfbbc06427e5bf7e06f1c4060a29689fce3a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575392"
---
# <a name="pidlidflagrequest-canonical-property"></a><span data-ttu-id="f212e-103">PidLidFlagRequest (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f212e-103">PidLidFlagRequest Canonical Property</span></span>

  
  
<span data-ttu-id="f212e-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f212e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f212e-105">Den Status der einer Besprechungsanfrage darstellt.</span><span class="sxs-lookup"><span data-stu-id="f212e-105">Represents the status of a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f212e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f212e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f212e-107">dispidRequest</span><span class="sxs-lookup"><span data-stu-id="f212e-107">dispidRequest</span></span>  <br/> |
|<span data-ttu-id="f212e-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="f212e-108">Property set:</span></span>  <br/> |<span data-ttu-id="f212e-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="f212e-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="f212e-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="f212e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f212e-111">0x00008530</span><span class="sxs-lookup"><span data-stu-id="f212e-111">0x00008530</span></span>  <br/> |
|<span data-ttu-id="f212e-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f212e-112">Data type:</span></span>  <br/> |<span data-ttu-id="f212e-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f212e-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f212e-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f212e-114">Area:</span></span>  <br/> |<span data-ttu-id="f212e-115">Kennzeichnen von</span><span class="sxs-lookup"><span data-stu-id="f212e-115">Flagging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f212e-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="f212e-116">Remarks</span></span>

<span data-ttu-id="f212e-117">In Microsoft Office Outlook ist eine Besprechungsanfrage ein Terminelement.</span><span class="sxs-lookup"><span data-stu-id="f212e-117">In Microsoft Office Outlook, a meeting request is an appointment item.</span></span>
  
<span data-ttu-id="f212e-118">Diese Eigenschaft enthält Benutzer festzulegen Text ein, um das Flag zugeordnet werden und festgelegt werden soll, wenn das Objekt "Message" gekennzeichnet oder abgeschlossen ist, jedoch nicht für ein Objekt bezüglich Besprechungen vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="f212e-118">This property contains user-specifiable text to be associated with the flag and should be set if the message object is flagged or completed, but should not exist for a meeting-related object.</span></span> <span data-ttu-id="f212e-119">Clients können nicht für diese Eigenschaft unterstützen und in diese schreiben immer "Nachverfolgung" (übersetzte Sprache des Benutzers, falls zutreffend) als Wert für die Zeichenfolge, wenn diese Eigenschaft festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f212e-119">Clients may choose not to support this property, and always write "Follow up" (translated to the user's language if appropriate) as the value of the string when this property should be set.</span></span> <span data-ttu-id="f212e-120">Diese Eigenschaft sollte bedingt basierend auf den Werten der **DispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) und **DispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) Eigenschaften ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="f212e-120">This property should be conditionally ignored based on the values of the **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f212e-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f212e-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f212e-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f212e-122">Protocol specifications</span></span>

<span data-ttu-id="f212e-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f212e-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f212e-124">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="f212e-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f212e-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f212e-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f212e-126">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="f212e-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f212e-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="f212e-127">Header files</span></span>

<span data-ttu-id="f212e-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f212e-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="f212e-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f212e-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f212e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f212e-130">See also</span></span>



[<span data-ttu-id="f212e-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f212e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f212e-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f212e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f212e-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f212e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f212e-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f212e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

