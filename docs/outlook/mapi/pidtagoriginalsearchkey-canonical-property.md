---
title: Kanonische Pidtagoriginalsearchkey (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSearchKey
api_type:
- COM
ms.assetid: ac5eb91d-31c9-459b-bb22-f4ccfc92d1db
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d106a216e8d72c126f3293f9d492db73992c3872
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355293"
---
# <a name="pidtagoriginalsearchkey-canonical-property"></a><span data-ttu-id="1ce55-103">Kanonische Pidtagoriginalsearchkey (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1ce55-103">PidTagOriginalSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="1ce55-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ce55-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ce55-105">Enthält den ursprünglichen Suchschlüssel für einen Eintrag, der aus einem Adressbuch in ein persönliches Adressbuch oder ein anderes beschreibbares Adressbuch kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1ce55-105">Contains the original search key for an entry copied from an address book to a personal address book or other writeable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1ce55-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1ce55-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1ce55-107">PR_ORIGINAL_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="1ce55-107">PR_ORIGINAL_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="1ce55-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="1ce55-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1ce55-109">0x3A14</span><span class="sxs-lookup"><span data-stu-id="1ce55-109">0x3A14</span></span>  <br/> |
|<span data-ttu-id="1ce55-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1ce55-110">Data type:</span></span>  <br/> |<span data-ttu-id="1ce55-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1ce55-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1ce55-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1ce55-112">Area:</span></span>  <br/> |<span data-ttu-id="1ce55-113">Allgemeine Nachrichtenübermittlung</span><span class="sxs-lookup"><span data-stu-id="1ce55-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ce55-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ce55-114">Remarks</span></span>

<span data-ttu-id="1ce55-115">Diese Eigenschaft ist eine der Eigenschaften, die Informationen zur ursprünglichen Quelle eines kopierten Eintrags enthalten.</span><span class="sxs-lookup"><span data-stu-id="1ce55-115">This property is one of the properties that contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="1ce55-116">Bei einem nicht gelesenen Bericht enthält diese Eigenschaft eine Kopie des Suchschlüssels des ursprünglichen Nachrichtenempfängers, für den der Bericht generiert wird.</span><span class="sxs-lookup"><span data-stu-id="1ce55-116">For a nonread report, this property contains a copy of the search key of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="1ce55-117">Wenn der ursprüngliche Empfänger Teil einer Verteilerliste ist, wird der Suchschlüssel der Verteilerliste für den Bericht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="1ce55-117">When the original recipient is part of a distribution list, the search key of the distribution list is preserved for the report.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1ce55-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1ce55-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1ce55-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1ce55-119">Protocol specifications</span></span>

<span data-ttu-id="1ce55-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1ce55-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1ce55-121">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="1ce55-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1ce55-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1ce55-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1ce55-123">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="1ce55-123">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1ce55-124">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="1ce55-124">Header files</span></span>

<span data-ttu-id="1ce55-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1ce55-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="1ce55-126">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="1ce55-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="1ce55-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="1ce55-127">Mapitags.h</span></span>
  
> <span data-ttu-id="1ce55-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="1ce55-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1ce55-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ce55-129">See also</span></span>



[<span data-ttu-id="1ce55-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ce55-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1ce55-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ce55-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1ce55-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1ce55-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1ce55-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1ce55-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

