---
title: PidTagInternetReferences (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetReferences
api_type:
- HeaderDef
ms.assetid: 645fe61d-414a-455e-b034-db3cfd003b9d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 431a212b6e024d695fe2de084080996d8b1054d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360410"
---
# <a name="pidtaginternetreferences-canonical-property"></a><span data-ttu-id="8e296-103">PidTagInternetReferences (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8e296-103">PidTagInternetReferences Canonical Property</span></span>

  
  
<span data-ttu-id="8e296-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e296-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e296-105">Enthält den Wert des Headerfelds References einer MIME-Nachricht (Multipurpose Internet Mail Extensions).</span><span class="sxs-lookup"><span data-stu-id="8e296-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's References header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8e296-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8e296-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8e296-107">PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W</span><span class="sxs-lookup"><span data-stu-id="8e296-107">PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W</span></span>  <br/> |
|<span data-ttu-id="8e296-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="8e296-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8e296-109">0x1039</span><span class="sxs-lookup"><span data-stu-id="8e296-109">0x1039</span></span>  <br/> |
|<span data-ttu-id="8e296-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8e296-110">Data type:</span></span>  <br/> |<span data-ttu-id="8e296-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8e296-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8e296-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8e296-112">Area:</span></span>  <br/> |<span data-ttu-id="8e296-113">MIME</span><span class="sxs-lookup"><span data-stu-id="8e296-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e296-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8e296-114">Remarks</span></span>

<span data-ttu-id="8e296-115">Um ein References-Kopfzeilenfeld zu generieren, müssen Clients diese Eigenschaften auf den gewünschten Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="8e296-115">To generate a References header field, clients must set these properties to the desired value.</span></span> <span data-ttu-id="8e296-116">MIME-Writer müssen den Wert dieser Eigenschaften in das Kopfzeilenfeld Verweise kopieren.</span><span class="sxs-lookup"><span data-stu-id="8e296-116">MIME writers must copy the value of these properties to the References header field.</span></span>
  
<span data-ttu-id="8e296-117">Um den Wert dieser Eigenschaften festlegen zu können, müssen MIME-Clients den gewünschten Wert in ein References-Kopfzeilenfeld schreiben.</span><span class="sxs-lookup"><span data-stu-id="8e296-117">To set the value of these properties, MIME clients must write the desired value to a References header field.</span></span> <span data-ttu-id="8e296-118">MIME-Reader müssen den Wert des Kopfzeilenfelds Verweise in diese Eigenschaften kopieren.</span><span class="sxs-lookup"><span data-stu-id="8e296-118">MIME readers must copy the value of the References header field to these properties.</span></span> <span data-ttu-id="8e296-119">MIME-Reader können den Wert dieser Eigenschaften kürzen, wenn sie eine Länge von 64 KB überschreiten.</span><span class="sxs-lookup"><span data-stu-id="8e296-119">MIME readers may truncate the value of these properties if it exceeds 64KB in length.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8e296-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8e296-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8e296-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="8e296-121">Protocol specifications</span></span>

<span data-ttu-id="8e296-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e296-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e296-123">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="8e296-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8e296-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e296-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e296-125">Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="8e296-125">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8e296-126">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="8e296-126">Header files</span></span>

<span data-ttu-id="8e296-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e296-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="8e296-128">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="8e296-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="8e296-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8e296-129">Mapitags.h</span></span>
  
> <span data-ttu-id="8e296-130">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="8e296-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8e296-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e296-131">See also</span></span>



[<span data-ttu-id="8e296-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8e296-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8e296-133">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="8e296-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8e296-134">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8e296-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8e296-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8e296-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

