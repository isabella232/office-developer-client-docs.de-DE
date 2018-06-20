---
title: Kanonische PidTagStoreRecordKey-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreRecordKey
api_type:
- COM
ms.assetid: 27347302-bd52-4f62-98f1-6c37f9a66463
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4598ca5e654308f7701b1dd66adb227599773b7d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795232"
---
# <a name="pidtagstorerecordkey-canonical-property"></a><span data-ttu-id="20e53-103">Kanonische PidTagStoreRecordKey-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="20e53-103">PidTagStoreRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="20e53-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="20e53-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="20e53-105">Enthält den eindeutigen binär vergleichbaren Bezeichner (Datensatzschlüssel) des Nachrichtenspeichers in der sich ein Objekt befindet.</span><span class="sxs-lookup"><span data-stu-id="20e53-105">Contains the unique binary-comparable identifier (record key) of the message store in which an object resides.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="20e53-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="20e53-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="20e53-107">PR_STORE_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="20e53-107">PR_STORE_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="20e53-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="20e53-108">Identifier:</span></span>  <br/> |<span data-ttu-id="20e53-109">0x0FFA</span><span class="sxs-lookup"><span data-stu-id="20e53-109">0x0FFA</span></span>  <br/> |
|<span data-ttu-id="20e53-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="20e53-110">Data type:</span></span>  <br/> |<span data-ttu-id="20e53-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="20e53-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="20e53-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="20e53-112">Area:</span></span>  <br/> |<span data-ttu-id="20e53-113">ID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="20e53-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="20e53-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="20e53-114">Remarks</span></span>

<span data-ttu-id="20e53-115">Für einen Nachrichtenspeicher ist diese Eigenschaft mit der **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))-Eigenschaft des Speichers identisch.</span><span class="sxs-lookup"><span data-stu-id="20e53-115">For a message store, this property is identical to the store's own **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="20e53-116">Die Beziehung zwischen diesem-Eigenschaft und die **PR_RECORD_KEY** ist dieselbe wie die Beziehung zwischen **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) und **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="20e53-116">The relationship between this property and **PR_RECORD_KEY** is the same as the relationship between **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) and **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="20e53-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="20e53-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="20e53-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="20e53-118">Protocol specifications</span></span>

<span data-ttu-id="20e53-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20e53-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20e53-120">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="20e53-120">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="20e53-121">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20e53-121">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20e53-122">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="20e53-122">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="20e53-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="20e53-123">Header files</span></span>

<span data-ttu-id="20e53-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="20e53-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="20e53-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="20e53-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="20e53-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="20e53-126">Mapitags.h</span></span>
  
> <span data-ttu-id="20e53-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="20e53-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="20e53-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20e53-128">See also</span></span>



[<span data-ttu-id="20e53-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="20e53-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="20e53-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="20e53-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="20e53-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="20e53-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="20e53-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="20e53-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
