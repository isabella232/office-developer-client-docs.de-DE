---
title: Kanonische Pidtagdefcreatedl (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateDl
api_type:
- HeaderDef
ms.assetid: 172dc15b-7bda-403f-a93a-446b2f9ff1d3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ff5d35104e9effc27c405b716cb61cf4643677b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417791"
---
# <a name="pidtagdefcreatedl-canonical-property"></a><span data-ttu-id="a1c57-103">Kanonische Pidtagdefcreatedl (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a1c57-103">PidTagDefCreateDl Canonical Property</span></span>

  
  
<span data-ttu-id="a1c57-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1c57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1c57-105">Enthält den Vorlagen Eintragsbezeichner für eine Standardverteilerliste.</span><span class="sxs-lookup"><span data-stu-id="a1c57-105">Contains the template entry identifier for a default distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a1c57-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a1c57-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a1c57-107">PR_DEF_CREATE_DL</span><span class="sxs-lookup"><span data-stu-id="a1c57-107">PR_DEF_CREATE_DL</span></span>  <br/> |
|<span data-ttu-id="a1c57-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="a1c57-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a1c57-109">0x3611</span><span class="sxs-lookup"><span data-stu-id="a1c57-109">0x3611</span></span>  <br/> |
|<span data-ttu-id="a1c57-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a1c57-110">Data type:</span></span>  <br/> |<span data-ttu-id="a1c57-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a1c57-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a1c57-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a1c57-112">Area:</span></span>  <br/> |<span data-ttu-id="a1c57-113">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="a1c57-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1c57-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1c57-114">Remarks</span></span>

<span data-ttu-id="a1c57-115">Client Anwendungen verwenden diese Eigenschaft, um eine Verteilerliste in einem Container zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a1c57-115">Client applications use this property to create a distribution list within a container.</span></span> <span data-ttu-id="a1c57-116">Die Unterstützung der Eintragserstellung ist für Adressbuchcontainer optional. diejenigen, die es nicht unterstützen, müssen diese Eigenschaft nicht offen legen.</span><span class="sxs-lookup"><span data-stu-id="a1c57-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="a1c57-117">Diese Eigenschaft gibt einen Eintrag an, der in der **PR_CREATE_TEMPLATES** ([pidtagcreatetemplates (](pidtagcreatetemplates-canonical-property.md))-Eigenschaft für Verteilerlisten angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a1c57-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for distribution lists.</span></span> <span data-ttu-id="a1c57-118">Nach dem Abrufen des Bezeichners verwendet der Client diesen bei einem Aufruf der [IABContainer:: CreateEntry](iabcontainer-createentry.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a1c57-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="a1c57-119">Der Eintrag stellt die Vorlage für die Standardverteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="a1c57-119">The entry represents the template for the default distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a1c57-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a1c57-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a1c57-121">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="a1c57-121">Header files</span></span>

<span data-ttu-id="a1c57-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a1c57-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="a1c57-123">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="a1c57-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="a1c57-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="a1c57-124">Mapitags.h</span></span>
  
> <span data-ttu-id="a1c57-125">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="a1c57-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a1c57-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1c57-126">See also</span></span>



[<span data-ttu-id="a1c57-127">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="a1c57-127">IABLogon::CompareEntryIDs</span></span>](iablogon-compareentryids.md)


[<span data-ttu-id="a1c57-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a1c57-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a1c57-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a1c57-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a1c57-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a1c57-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a1c57-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a1c57-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

