---
title: PidTagCreationTime (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCreationTime
api_type:
- HeaderDef
ms.assetid: 13122af2-06c8-4342-983d-e38178743d8f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 475c93e7f2c246e0351f3054b0f827fb7ee015a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794266"
---
# <a name="pidtagcreationtime-canonical-property"></a><span data-ttu-id="45c81-103">PidTagCreationTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="45c81-103">PidTagCreationTime Canonical Property</span></span>

  
  
<span data-ttu-id="45c81-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="45c81-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="45c81-105">Enthält das Erstellungsdatum und die Uhrzeit einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="45c81-105">Contains the creation date and time of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="45c81-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="45c81-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="45c81-107">PR_CREATION_TIME</span><span class="sxs-lookup"><span data-stu-id="45c81-107">PR_CREATION_TIME</span></span>  <br/> |
|<span data-ttu-id="45c81-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="45c81-108">Identifier:</span></span>  <br/> |<span data-ttu-id="45c81-109">0x3007</span><span class="sxs-lookup"><span data-stu-id="45c81-109">0x3007</span></span>  <br/> |
|<span data-ttu-id="45c81-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="45c81-110">Data type:</span></span>  <br/> |<span data-ttu-id="45c81-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="45c81-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="45c81-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="45c81-112">Area:</span></span>  <br/> |<span data-ttu-id="45c81-113">Nachrichtzeit</span><span class="sxs-lookup"><span data-stu-id="45c81-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45c81-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45c81-114">Remarks</span></span>

<span data-ttu-id="45c81-115">Ein Nachrichtenspeicher wird diese Eigenschaft für jede Nachricht, das erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="45c81-115">A message store sets this property for each message that it creates.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="45c81-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="45c81-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="45c81-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="45c81-117">Protocol specifications</span></span>

<span data-ttu-id="45c81-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45c81-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45c81-119">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="45c81-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="45c81-120">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45c81-120">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45c81-121">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="45c81-121">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="45c81-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="45c81-122">Header files</span></span>

<span data-ttu-id="45c81-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45c81-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="45c81-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="45c81-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="45c81-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="45c81-125">Mapitags.h</span></span>
  
> <span data-ttu-id="45c81-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="45c81-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45c81-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45c81-127">See also</span></span>



[<span data-ttu-id="45c81-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45c81-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45c81-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45c81-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45c81-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="45c81-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45c81-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="45c81-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

