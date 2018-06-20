---
title: Kanonische PidTagInternetReferences-Eigenschaft
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
ms.openlocfilehash: 4558fcdba11aed92eb21972ed62320209ade77ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794508"
---
# <a name="pidtaginternetreferences-canonical-property"></a><span data-ttu-id="9e93a-103">Kanonische PidTagInternetReferences-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9e93a-103">PidTagInternetReferences Canonical Property</span></span>

  
  
<span data-ttu-id="9e93a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9e93a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9e93a-105">Enthält den Wert der Verweise Header ein Feld einer Nachricht Multipurpose Internet Mail Extensions (MIME).</span><span class="sxs-lookup"><span data-stu-id="9e93a-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's References header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9e93a-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9e93a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9e93a-107">PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W</span><span class="sxs-lookup"><span data-stu-id="9e93a-107">PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W</span></span>  <br/> |
|<span data-ttu-id="9e93a-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="9e93a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9e93a-109">0x1039</span><span class="sxs-lookup"><span data-stu-id="9e93a-109">0x1039</span></span>  <br/> |
|<span data-ttu-id="9e93a-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9e93a-110">Data type:</span></span>  <br/> |<span data-ttu-id="9e93a-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9e93a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9e93a-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9e93a-112">Area:</span></span>  <br/> |<span data-ttu-id="9e93a-113">MIME</span><span class="sxs-lookup"><span data-stu-id="9e93a-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9e93a-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9e93a-114">Remarks</span></span>

<span data-ttu-id="9e93a-115">Um ein Kopfzeilenfeld Verweise generiert werden soll, müssen die Clients diese Eigenschaften auf den gewünschten Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="9e93a-115">To generate a References header field, clients must set these properties to the desired value.</span></span> <span data-ttu-id="9e93a-116">MIME-Writer müssen den Wert dieser Eigenschaften in die Verweise Kopfzeilenfeld kopieren.</span><span class="sxs-lookup"><span data-stu-id="9e93a-116">MIME writers must copy the value of these properties to the References header field.</span></span>
  
<span data-ttu-id="9e93a-117">Wenn den Wert dieser Eigenschaften festlegen möchten, müssen den gewünschten Wert MIME-Clients in ein Kopfzeilenfeld Verweise geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="9e93a-117">To set the value of these properties, MIME clients must write the desired value to a References header field.</span></span> <span data-ttu-id="9e93a-118">MIME-Leser müssen den Wert des Felds Kopfzeile Verweise auf diese Eigenschaften kopieren.</span><span class="sxs-lookup"><span data-stu-id="9e93a-118">MIME readers must copy the value of the References header field to these properties.</span></span> <span data-ttu-id="9e93a-119">MIME-Leser können den Wert dieser Eigenschaften abschneiden, wenn sie 64 KB Länge überschreitet.</span><span class="sxs-lookup"><span data-stu-id="9e93a-119">MIME readers may truncate the value of these properties if it exceeds 64KB in length.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9e93a-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9e93a-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9e93a-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9e93a-121">Protocol specifications</span></span>

<span data-ttu-id="9e93a-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e93a-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e93a-123">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="9e93a-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9e93a-124">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e93a-124">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e93a-125">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="9e93a-125">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9e93a-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="9e93a-126">Header files</span></span>

<span data-ttu-id="9e93a-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9e93a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="9e93a-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9e93a-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="9e93a-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9e93a-129">Mapitags.h</span></span>
  
> <span data-ttu-id="9e93a-130">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9e93a-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9e93a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e93a-131">See also</span></span>



[<span data-ttu-id="9e93a-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9e93a-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9e93a-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9e93a-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9e93a-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9e93a-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9e93a-135">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9e93a-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

