---
title: Kanonische Pidtaginternetreferences (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 431a212b6e024d695fe2de084080996d8b1054d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360410"
---
# <a name="pidtaginternetreferences-canonical-property"></a><span data-ttu-id="889fb-103">Kanonische Pidtaginternetreferences (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="889fb-103">PidTagInternetReferences Canonical Property</span></span>

  
  
<span data-ttu-id="889fb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="889fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="889fb-105">Enthält den Wert des References-Kopfzeilenfelds für MIME-Nachrichten (Multipurpose Internet Mail Extensions).</span><span class="sxs-lookup"><span data-stu-id="889fb-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's References header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="889fb-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="889fb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="889fb-107">PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W</span><span class="sxs-lookup"><span data-stu-id="889fb-107">PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W</span></span>  <br/> |
|<span data-ttu-id="889fb-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="889fb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="889fb-109">0x1039</span><span class="sxs-lookup"><span data-stu-id="889fb-109">0x1039</span></span>  <br/> |
|<span data-ttu-id="889fb-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="889fb-110">Data type:</span></span>  <br/> |<span data-ttu-id="889fb-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="889fb-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="889fb-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="889fb-112">Area:</span></span>  <br/> |<span data-ttu-id="889fb-113">MIME</span><span class="sxs-lookup"><span data-stu-id="889fb-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="889fb-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="889fb-114">Remarks</span></span>

<span data-ttu-id="889fb-115">Um ein References-Kopfzeilenfeld zu generieren, müssen Clients diese Eigenschaften auf den gewünschten Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="889fb-115">To generate a References header field, clients must set these properties to the desired value.</span></span> <span data-ttu-id="889fb-116">MIME-Writer müssen den Wert dieser Eigenschaften in das Kopfzeilenfeld References kopieren.</span><span class="sxs-lookup"><span data-stu-id="889fb-116">MIME writers must copy the value of these properties to the References header field.</span></span>
  
<span data-ttu-id="889fb-117">Um den Wert dieser Eigenschaften festzulegen, müssen MIME-Clients den gewünschten Wert in ein References-Kopfzeilenfeld schreiben.</span><span class="sxs-lookup"><span data-stu-id="889fb-117">To set the value of these properties, MIME clients must write the desired value to a References header field.</span></span> <span data-ttu-id="889fb-118">MIME-Leser müssen den Wert des Headerfelds References in diese Eigenschaften kopieren.</span><span class="sxs-lookup"><span data-stu-id="889fb-118">MIME readers must copy the value of the References header field to these properties.</span></span> <span data-ttu-id="889fb-119">MIME-Leser können den Wert dieser Eigenschaften abschneiden, wenn Sie die Länge von 64 KB überschreiten.</span><span class="sxs-lookup"><span data-stu-id="889fb-119">MIME readers may truncate the value of these properties if it exceeds 64KB in length.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="889fb-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="889fb-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="889fb-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="889fb-121">Protocol specifications</span></span>

<span data-ttu-id="889fb-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="889fb-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="889fb-123">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="889fb-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="889fb-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="889fb-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="889fb-125">Konvertiert von Internet Standard-e-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="889fb-125">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="889fb-126">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="889fb-126">Header files</span></span>

<span data-ttu-id="889fb-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="889fb-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="889fb-128">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="889fb-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="889fb-129">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="889fb-129">Mapitags.h</span></span>
  
> <span data-ttu-id="889fb-130">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="889fb-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="889fb-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="889fb-131">See also</span></span>



[<span data-ttu-id="889fb-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="889fb-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="889fb-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="889fb-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="889fb-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="889fb-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="889fb-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="889fb-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

