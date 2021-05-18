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
ms.openlocfilehash: cd09c85e4f44bbea29807d72a273ccf6980ca6df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407480"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a><span data-ttu-id="1b8d0-103">PidTagDefCreateMailuser (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1b8d0-103">PidTagDefCreateMailuser Canonical Property</span></span>

  
  
<span data-ttu-id="1b8d0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b8d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b8d0-105">Enthält die Vorlageneintrags-ID für ein Standardmäßiges Messagingbenutzerobjekt.</span><span class="sxs-lookup"><span data-stu-id="1b8d0-105">Contains the template entry identifier for a default messaging user object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1b8d0-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1b8d0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1b8d0-107">PR_DEF_CREATE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="1b8d0-107">PR_DEF_CREATE_MAILUSER</span></span>  <br/> |
|<span data-ttu-id="1b8d0-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="1b8d0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1b8d0-109">0x3612</span><span class="sxs-lookup"><span data-stu-id="1b8d0-109">0x3612</span></span>  <br/> |
|<span data-ttu-id="1b8d0-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1b8d0-110">Data type:</span></span>  <br/> |<span data-ttu-id="1b8d0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1b8d0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1b8d0-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1b8d0-112">Area:</span></span>  <br/> |<span data-ttu-id="1b8d0-113">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="1b8d0-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b8d0-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1b8d0-114">Remarks</span></span>

<span data-ttu-id="1b8d0-115">Clientanwendungen verwenden diese Eigenschaft, um ein Messagingbenutzerobjekt in einem Container zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1b8d0-115">Client applications use this property to create a messaging user object within a container.</span></span> <span data-ttu-id="1b8d0-116">Die Unterstützung der Eintragserstellung ist für Adressbuchcontainer optional. Diejenigen, die sie nicht unterstützen, müssen diese Eigenschaft nicht verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="1b8d0-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="1b8d0-117">Diese Eigenschaft gibt einen Eintrag an, der in der **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) -Eigenschaft für Messagingbenutzer angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1b8d0-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for messaging users.</span></span> <span data-ttu-id="1b8d0-118">Nach dem Abrufen des Bezeichners verwendet der Client ihn in einem Aufruf der [IABContainer::CreateEntry-Methode.](iabcontainer-createentry.md)</span><span class="sxs-lookup"><span data-stu-id="1b8d0-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="1b8d0-119">Der Eintrag stellt die Vorlage für den Standardnachrichtenbenutzer dar.</span><span class="sxs-lookup"><span data-stu-id="1b8d0-119">The entry represents the template for the default messaging user.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1b8d0-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1b8d0-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1b8d0-121">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="1b8d0-121">Header files</span></span>

<span data-ttu-id="1b8d0-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1b8d0-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="1b8d0-123">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1b8d0-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="1b8d0-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1b8d0-124">Mapitags.h</span></span>
  
> <span data-ttu-id="1b8d0-125">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="1b8d0-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1b8d0-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b8d0-126">See also</span></span>



[<span data-ttu-id="1b8d0-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1b8d0-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1b8d0-128">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="1b8d0-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1b8d0-129">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1b8d0-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1b8d0-130">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1b8d0-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

