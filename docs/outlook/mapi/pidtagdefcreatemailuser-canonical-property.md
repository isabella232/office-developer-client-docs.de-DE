---
title: Kanonische Pidtagdefcreatemailuser (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: cd09c85e4f44bbea29807d72a273ccf6980ca6df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32269986"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a><span data-ttu-id="cef8a-103">Kanonische Pidtagdefcreatemailuser (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cef8a-103">PidTagDefCreateMailuser Canonical Property</span></span>

  
  
<span data-ttu-id="cef8a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cef8a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cef8a-105">Enthält den Vorlagen Eintragsbezeichner für ein Standardmäßiges Messaging-Benutzerobjekt.</span><span class="sxs-lookup"><span data-stu-id="cef8a-105">Contains the template entry identifier for a default messaging user object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cef8a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="cef8a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cef8a-107">PR_DEF_CREATE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="cef8a-107">PR_DEF_CREATE_MAILUSER</span></span>  <br/> |
|<span data-ttu-id="cef8a-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="cef8a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cef8a-109">0x3612</span><span class="sxs-lookup"><span data-stu-id="cef8a-109">0x3612</span></span>  <br/> |
|<span data-ttu-id="cef8a-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="cef8a-110">Data type:</span></span>  <br/> |<span data-ttu-id="cef8a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cef8a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cef8a-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="cef8a-112">Area:</span></span>  <br/> |<span data-ttu-id="cef8a-113">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="cef8a-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cef8a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cef8a-114">Remarks</span></span>

<span data-ttu-id="cef8a-115">Client Anwendungen verwenden diese Eigenschaft, um ein Messaging-Benutzerobjekt in einem Container zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cef8a-115">Client applications use this property to create a messaging user object within a container.</span></span> <span data-ttu-id="cef8a-116">Die Unterstützung der Eintragserstellung ist für Adressbuchcontainer optional. diejenigen, die es nicht unterstützen, müssen diese Eigenschaft nicht offen legen.</span><span class="sxs-lookup"><span data-stu-id="cef8a-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="cef8a-117">Diese Eigenschaft gibt einen Eintrag an, der in der **PR_CREATE_TEMPLATES** ([pidtagcreatetemplates (](pidtagcreatetemplates-canonical-property.md))-Eigenschaft für Messagingbenutzer angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cef8a-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for messaging users.</span></span> <span data-ttu-id="cef8a-118">Nach dem Abrufen des Bezeichners verwendet der Client diesen bei einem Aufruf der [IABContainer:: CreateEntry](iabcontainer-createentry.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="cef8a-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="cef8a-119">Der Eintrag stellt die Vorlage für den standardmäßigen Messagingbenutzer dar.</span><span class="sxs-lookup"><span data-stu-id="cef8a-119">The entry represents the template for the default messaging user.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cef8a-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cef8a-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="cef8a-121">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="cef8a-121">Header files</span></span>

<span data-ttu-id="cef8a-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="cef8a-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="cef8a-123">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="cef8a-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="cef8a-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="cef8a-124">Mapitags.h</span></span>
  
> <span data-ttu-id="cef8a-125">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="cef8a-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cef8a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cef8a-126">See also</span></span>



[<span data-ttu-id="cef8a-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cef8a-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cef8a-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cef8a-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cef8a-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="cef8a-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cef8a-130">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="cef8a-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

