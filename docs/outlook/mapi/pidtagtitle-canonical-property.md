---
title: PidTagTitle (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTitle
api_type:
- COM
ms.assetid: f35bbcc3-15dd-40ab-9bf4-bdb21f95d464
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2501ea7c4be08b0bec3c2d65e6a504df47dfc488
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358765"
---
# <a name="pidtagtitle-canonical-property"></a><span data-ttu-id="b1282-103">PidTagTitle (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b1282-103">PidTagTitle Canonical Property</span></span>

  
  
<span data-ttu-id="b1282-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1282-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1282-105">Enthält den Auftragstitel des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="b1282-105">Contains the recipient's job title.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b1282-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b1282-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b1282-107">PR_TITLE, PR_TITLE_A, PR_TITLE_W</span><span class="sxs-lookup"><span data-stu-id="b1282-107">PR_TITLE, PR_TITLE_A, PR_TITLE_W</span></span>  <br/> |
|<span data-ttu-id="b1282-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b1282-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b1282-109">0x3A17</span><span class="sxs-lookup"><span data-stu-id="b1282-109">0x3A17</span></span>  <br/> |
|<span data-ttu-id="b1282-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b1282-110">Data type:</span></span>  <br/> |<span data-ttu-id="b1282-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b1282-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b1282-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b1282-112">Area:</span></span>  <br/> |<span data-ttu-id="b1282-113">MAPI-E-Mail-Benutzer</span><span class="sxs-lookup"><span data-stu-id="b1282-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1282-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b1282-114">Remarks</span></span>

<span data-ttu-id="b1282-115">Diese Eigenschaften stellen Identifikations- und Zugriffsinformationen für einen Empfänger zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="b1282-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="b1282-116">Sie werden vom Empfänger und der Organisation des Empfängers definiert.</span><span class="sxs-lookup"><span data-stu-id="b1282-116">They are defined by the recipient and the recipient's organization.</span></span> 
  
<span data-ttu-id="b1282-117">Diese Eigenschaften werden häufig verwendet, um den formalen Auftragstitel des Empfängers anzugeben, z. B. Senior Programmer, anstatt eine Berufsklasse wie z. B. Programmierer.</span><span class="sxs-lookup"><span data-stu-id="b1282-117">These properties are commonly used to indicate the recipient's formal job title, such as Senior Programmer, rather than occupational class, such as programmer.</span></span> <span data-ttu-id="b1282-118">Es wird in der Regel nicht für "Suffix"-Titel wie Esq verwendet.</span><span class="sxs-lookup"><span data-stu-id="b1282-118">It is not typically used for "suffix" titles such as Esq.</span></span> <span data-ttu-id="b1282-119">oder DDS.</span><span class="sxs-lookup"><span data-stu-id="b1282-119">or DDS.</span></span>
  
<span data-ttu-id="b1282-120">Allgemeine Werte für diese Eigenschaft sind: Managing Director, Programmer II, Associate Professor und Development Lead.</span><span class="sxs-lookup"><span data-stu-id="b1282-120">Common values for this property include: Managing Director, Programmer II, Associate Professor, and Development Lead.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b1282-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b1282-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b1282-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b1282-122">Protocol specifications</span></span>

<span data-ttu-id="b1282-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1282-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1282-124">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="b1282-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b1282-125">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1282-125">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1282-126">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="b1282-126">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="b1282-127">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1282-127">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1282-128">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="b1282-128">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b1282-129">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="b1282-129">Header files</span></span>

<span data-ttu-id="b1282-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b1282-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="b1282-131">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b1282-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="b1282-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b1282-132">Mapitags.h</span></span>
  
> <span data-ttu-id="b1282-133">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b1282-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b1282-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1282-134">See also</span></span>



[<span data-ttu-id="b1282-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1282-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b1282-136">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="b1282-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b1282-137">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b1282-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b1282-138">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b1282-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

