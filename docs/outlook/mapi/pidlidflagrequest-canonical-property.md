---
title: Kanonische Pidlidflagrequest (-Eigenschaft
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
ms.openlocfilehash: ddcf32df716fe2b0a02655278ff0cd8d821de1f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357806"
---
# <a name="pidlidflagrequest-canonical-property"></a><span data-ttu-id="fe301-103">Kanonische Pidlidflagrequest (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fe301-103">PidLidFlagRequest Canonical Property</span></span>

  
  
<span data-ttu-id="fe301-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe301-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe301-105">Stellt den Status einer Besprechungsanfrage dar.</span><span class="sxs-lookup"><span data-stu-id="fe301-105">Represents the status of a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fe301-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="fe301-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fe301-107">dispidRequest</span><span class="sxs-lookup"><span data-stu-id="fe301-107">dispidRequest</span></span>  <br/> |
|<span data-ttu-id="fe301-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="fe301-108">Property set:</span></span>  <br/> |<span data-ttu-id="fe301-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="fe301-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="fe301-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="fe301-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fe301-111">0x00008530</span><span class="sxs-lookup"><span data-stu-id="fe301-111">0x00008530</span></span>  <br/> |
|<span data-ttu-id="fe301-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="fe301-112">Data type:</span></span>  <br/> |<span data-ttu-id="fe301-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fe301-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fe301-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="fe301-114">Area:</span></span>  <br/> |<span data-ttu-id="fe301-115">Kennzeichnen</span><span class="sxs-lookup"><span data-stu-id="fe301-115">Flagging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe301-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe301-116">Remarks</span></span>

<span data-ttu-id="fe301-117">In Microsoft Office Outlook ist eine Besprechungsanfrage ein Terminelement.</span><span class="sxs-lookup"><span data-stu-id="fe301-117">In Microsoft Office Outlook, a meeting request is an appointment item.</span></span>
  
<span data-ttu-id="fe301-118">Diese Eigenschaft enthält benutzerspezifischen Text, der dem Flag zugeordnet werden soll, und sollte festgelegt werden, wenn das Nachrichtenobjekt gekennzeichnet oder abgeschlossen ist, aber für ein Besprechungs bezogenes Objekt nicht vorhanden sein sollte.</span><span class="sxs-lookup"><span data-stu-id="fe301-118">This property contains user-specifiable text to be associated with the flag and should be set if the message object is flagged or completed, but should not exist for a meeting-related object.</span></span> <span data-ttu-id="fe301-119">Clients können diese Eigenschaft nicht unterstützen und immer "Follow up" (gegebenenfalls in die Sprache des Benutzers übersetzt) als Wert der Zeichenfolge schreiben, wenn diese Eigenschaft festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe301-119">Clients may choose not to support this property, and always write "Follow up" (translated to the user's language if appropriate) as the value of the string when this property should be set.</span></span> <span data-ttu-id="fe301-120">Diese Eigenschaft sollte basierend auf den Werten der Eigenschaften **dispidFlagStringEnum** ([Pidlidflagstring (](pidlidflagstring-canonical-property.md)) und **dispidValidFlagStringProof** ([pidlidvalidflagstringproof (](pidlidvalidflagstringproof-canonical-property.md)) bedingungslos ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="fe301-120">This property should be conditionally ignored based on the values of the **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fe301-121">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fe301-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fe301-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="fe301-122">Protocol specifications</span></span>

<span data-ttu-id="fe301-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe301-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fe301-124">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="fe301-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fe301-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe301-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fe301-126">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Markierung an.</span><span class="sxs-lookup"><span data-stu-id="fe301-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fe301-127">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="fe301-127">Header files</span></span>

<span data-ttu-id="fe301-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="fe301-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="fe301-129">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="fe301-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fe301-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe301-130">See also</span></span>



[<span data-ttu-id="fe301-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe301-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fe301-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe301-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fe301-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="fe301-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fe301-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="fe301-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

