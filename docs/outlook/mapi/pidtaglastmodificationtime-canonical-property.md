---
title: PidTagLastModificationTime (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLastModificationTime
api_type:
- HeaderDef
ms.assetid: a64e5300-6865-4588-8e1b-158cfd9c60c2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dea709b457e28efef62718fc388621e01c4eb5bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279709"
---
# <a name="pidtaglastmodificationtime-canonical-property"></a><span data-ttu-id="5f864-103">PidTagLastModificationTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5f864-103">PidTagLastModificationTime Canonical Property</span></span>

  
  
<span data-ttu-id="5f864-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f864-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f864-105">Enthält das Datum und die Uhrzeit, zu der das Objekt oder Unterobjekt zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="5f864-105">Contains the date and time when the object or subobject was last modified.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5f864-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5f864-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5f864-107">PR_LAST_MODIFICATION_TIME</span><span class="sxs-lookup"><span data-stu-id="5f864-107">PR_LAST_MODIFICATION_TIME</span></span>  <br/> |
|<span data-ttu-id="5f864-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="5f864-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5f864-109">0x3008</span><span class="sxs-lookup"><span data-stu-id="5f864-109">0x3008</span></span>  <br/> |
|<span data-ttu-id="5f864-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5f864-110">Data type:</span></span>  <br/> |<span data-ttu-id="5f864-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="5f864-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="5f864-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5f864-112">Area:</span></span>  <br/> |<span data-ttu-id="5f864-113">Nachrichtenzeit</span><span class="sxs-lookup"><span data-stu-id="5f864-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f864-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5f864-114">Remarks</span></span>

<span data-ttu-id="5f864-115">Diese Eigenschaft wird zunächst auf denselben Wert wie die **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5f864-115">This property is initially set to the same value as the **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)) property.</span></span> <span data-ttu-id="5f864-116">Anlagenunterobjekte können sie bei Bedarf aktualisieren, indem sie die letzte Änderungszeit kopieren, die vom systemeigenen Dateisystem verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="5f864-116">Attachment subobjects can update it as necessary by copying the last modification time maintained by the native file system.</span></span> <span data-ttu-id="5f864-117">Eine Clientanwendung kann diese Eigenschaft bis zum ersten Aufruf der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) festlegen.</span><span class="sxs-lookup"><span data-stu-id="5f864-117">A client application can set this property until the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="5f864-118">Von da an sollte der Anbieter die **PR_LAST_MODIFICATION_TIME** bei jedem **IMAPIProp::SaveChanges-Aufruf** aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5f864-118">From then on the provider should update **PR_LAST_MODIFICATION_TIME** during every **IMAPIProp::SaveChanges** call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5f864-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5f864-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5f864-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5f864-120">Protocol specifications</span></span>

<span data-ttu-id="5f864-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f864-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f864-122">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="5f864-122">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="5f864-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f864-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f864-124">Behandelt die Synchronisierung von Messagingobjektdaten zwischen einem Server und einem Client.</span><span class="sxs-lookup"><span data-stu-id="5f864-124">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="5f864-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f864-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f864-126">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="5f864-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5f864-127">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="5f864-127">Header files</span></span>

<span data-ttu-id="5f864-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5f864-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="5f864-129">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5f864-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="5f864-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5f864-130">Mapitags.h</span></span>
  
> <span data-ttu-id="5f864-131">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5f864-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f864-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f864-132">See also</span></span>



[<span data-ttu-id="5f864-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5f864-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5f864-134">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="5f864-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5f864-135">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5f864-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5f864-136">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5f864-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

