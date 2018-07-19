---
title: PidTagDefCreateMailuser (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateMailuser
api_type:
- HeaderDef
ms.assetid: e8293dc9-f2f1-4065-89f4-e734a8db63df
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 33c62b81982aaac3659ad4d41ea2cf5298b42287
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794290"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a><span data-ttu-id="bc45f-103">PidTagDefCreateMailuser (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bc45f-103">PidTagDefCreateMailuser Canonical Property</span></span>

  
  
<span data-ttu-id="bc45f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bc45f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bc45f-105">Die Vorlage Eintrags-ID für eine standardmäßige messaging User-Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="bc45f-105">Contains the template entry identifier for a default messaging user object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc45f-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bc45f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bc45f-107">PR_DEF_CREATE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="bc45f-107">PR_DEF_CREATE_MAILUSER</span></span>  <br/> |
|<span data-ttu-id="bc45f-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="bc45f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bc45f-109">0x3612</span><span class="sxs-lookup"><span data-stu-id="bc45f-109">0x3612</span></span>  <br/> |
|<span data-ttu-id="bc45f-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bc45f-110">Data type:</span></span>  <br/> |<span data-ttu-id="bc45f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bc45f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bc45f-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bc45f-112">Area:</span></span>  <br/> |<span data-ttu-id="bc45f-113">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="bc45f-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc45f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc45f-114">Remarks</span></span>

<span data-ttu-id="bc45f-115">Clientanwendungen mit dieser Eigenschaft können Sie um ein messaging User-Objekt in einem Container zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bc45f-115">Client applications use this property to create a messaging user object within a container.</span></span> <span data-ttu-id="bc45f-116">Unterstützung von Eintrag Creation ist optional für Address Book Container. die, die nicht unterstützen sind nicht erforderlich, diese Eigenschaft verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="bc45f-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="bc45f-117">Diese Eigenschaft gibt einen Eintrag, der angezeigt werden, kann in der Eigenschaft **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) für die messaging-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="bc45f-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for messaging users.</span></span> <span data-ttu-id="bc45f-118">Wenn den Bezeichner erhalten haben, verwendet der Client es in einem Aufruf der [IABContainer::CreateEntry](iabcontainer-createentry.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="bc45f-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="bc45f-119">Der Eintrag stellt die Vorlage für den Standard-messaging-Benutzer dar.</span><span class="sxs-lookup"><span data-stu-id="bc45f-119">The entry represents the template for the default messaging user.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bc45f-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bc45f-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bc45f-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="bc45f-121">Header files</span></span>

<span data-ttu-id="bc45f-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bc45f-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="bc45f-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="bc45f-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="bc45f-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bc45f-124">Mapitags.h</span></span>
  
> <span data-ttu-id="bc45f-125">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="bc45f-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bc45f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc45f-126">See also</span></span>



[<span data-ttu-id="bc45f-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bc45f-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bc45f-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bc45f-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bc45f-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bc45f-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bc45f-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bc45f-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

