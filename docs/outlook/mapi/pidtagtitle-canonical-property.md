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
ms.openlocfilehash: c19a757b8adf474a3624f90a7cf19cc2308fa0d0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582266"
---
# <a name="pidtagtitle-canonical-property"></a><span data-ttu-id="13092-103">PidTagTitle (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="13092-103">PidTagTitle Canonical Property</span></span>

  
  
<span data-ttu-id="13092-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13092-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13092-105">Enthält die Position des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="13092-105">Contains the recipient's job title.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="13092-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="13092-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="13092-107">PR_TITLE, PR_TITLE_A, PR_TITLE_W</span><span class="sxs-lookup"><span data-stu-id="13092-107">PR_TITLE, PR_TITLE_A, PR_TITLE_W</span></span>  <br/> |
|<span data-ttu-id="13092-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="13092-108">Identifier:</span></span>  <br/> |<span data-ttu-id="13092-109">0x3A17</span><span class="sxs-lookup"><span data-stu-id="13092-109">0x3A17</span></span>  <br/> |
|<span data-ttu-id="13092-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="13092-110">Data type:</span></span>  <br/> |<span data-ttu-id="13092-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="13092-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="13092-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="13092-112">Area:</span></span>  <br/> |<span data-ttu-id="13092-113">MAPI-e-Mail-Benutzer</span><span class="sxs-lookup"><span data-stu-id="13092-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13092-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="13092-114">Remarks</span></span>

<span data-ttu-id="13092-115">Diese Eigenschaften Identitätsnachweis und Zugriff auf Informationen für einen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="13092-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="13092-116">Sie sind durch den Empfänger und des Empfängers Organisation definiert.</span><span class="sxs-lookup"><span data-stu-id="13092-116">They are defined by the recipient and the recipient's organization.</span></span> 
  
<span data-ttu-id="13092-117">Diese Eigenschaften werden häufig verwendet, des Empfängers formelle Position, wie beispielsweise Senior Programmierer, statt berufliche-Klasse, wie Programmierer an.</span><span class="sxs-lookup"><span data-stu-id="13092-117">These properties are commonly used to indicate the recipient's formal job title, such as Senior Programmer, rather than occupational class, such as programmer.</span></span> <span data-ttu-id="13092-118">Es wird nicht in der Regel für Titel wie eines Unternehmens? "Suffix" verwendet</span><span class="sxs-lookup"><span data-stu-id="13092-118">It is not typically used for "suffix" titles such as Esq.</span></span> <span data-ttu-id="13092-119">oder DDS.</span><span class="sxs-lookup"><span data-stu-id="13092-119">or DDS.</span></span>
  
<span data-ttu-id="13092-120">Allgemeine Werte für diese Eigenschaft sind: Managing Director, Programmierer II, Dozenten zuordnen und leitender Softwareentwickler.</span><span class="sxs-lookup"><span data-stu-id="13092-120">Common values for this property include: Managing Director, Programmer II, Associate Professor, and Development Lead.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="13092-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="13092-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="13092-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="13092-122">Protocol specifications</span></span>

<span data-ttu-id="13092-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13092-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13092-124">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="13092-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="13092-125">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13092-125">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13092-126">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="13092-126">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="13092-127">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13092-127">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13092-128">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="13092-128">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="13092-129">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="13092-129">Header files</span></span>

<span data-ttu-id="13092-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="13092-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="13092-131">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="13092-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="13092-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="13092-132">Mapitags.h</span></span>
  
> <span data-ttu-id="13092-133">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="13092-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="13092-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13092-134">See also</span></span>



[<span data-ttu-id="13092-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="13092-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="13092-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="13092-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="13092-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="13092-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="13092-138">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="13092-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

