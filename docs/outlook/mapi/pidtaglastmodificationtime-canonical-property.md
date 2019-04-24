---
title: Kanonische PidTagLastModificationTime-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: dea709b457e28efef62718fc388621e01c4eb5bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279709"
---
# <a name="pidtaglastmodificationtime-canonical-property"></a><span data-ttu-id="ed4a5-103">Kanonische PidTagLastModificationTime-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ed4a5-103">PidTagLastModificationTime Canonical Property</span></span>

  
  
<span data-ttu-id="ed4a5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed4a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed4a5-105">Enthält das Datum und die Uhrzeit der letzten Änderung des Objekts oder des Unterobjekts.</span><span class="sxs-lookup"><span data-stu-id="ed4a5-105">Contains the date and time when the object or subobject was last modified.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ed4a5-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ed4a5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ed4a5-107">PR_LAST_MODIFICATION_TIME</span><span class="sxs-lookup"><span data-stu-id="ed4a5-107">PR_LAST_MODIFICATION_TIME</span></span>  <br/> |
|<span data-ttu-id="ed4a5-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="ed4a5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ed4a5-109">0x3008</span><span class="sxs-lookup"><span data-stu-id="ed4a5-109">0x3008</span></span>  <br/> |
|<span data-ttu-id="ed4a5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ed4a5-110">Data type:</span></span>  <br/> |<span data-ttu-id="ed4a5-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="ed4a5-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="ed4a5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ed4a5-112">Area:</span></span>  <br/> |<span data-ttu-id="ed4a5-113">Nachrichten Zeit</span><span class="sxs-lookup"><span data-stu-id="ed4a5-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed4a5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed4a5-114">Remarks</span></span>

<span data-ttu-id="ed4a5-115">Diese Eigenschaft wird anfänglich auf den gleichen Wert wie die **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))-Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ed4a5-115">This property is initially set to the same value as the **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)) property.</span></span> <span data-ttu-id="ed4a5-116">Attachment-unter Objekte können Sie bei Bedarf aktualisieren, indem Sie den zuletzt vom systemeigenen Dateisystem verwalteten Zeitpunkt kopieren.</span><span class="sxs-lookup"><span data-stu-id="ed4a5-116">Attachment subobjects can update it as necessary by copying the last modification time maintained by the native file system.</span></span> <span data-ttu-id="ed4a5-117">Eine Clientanwendung kann diese Eigenschaft festlegen, bis der erste Aufruf der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ed4a5-117">A client application can set this property until the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="ed4a5-118">Von nun an sollte der Anbieter **PR_LAST_MODIFICATION_TIME** während jedes **IMAPIProp:: SaveChanges** -Aufrufs aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ed4a5-118">From then on the provider should update **PR_LAST_MODIFICATION_TIME** during every **IMAPIProp::SaveChanges** call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ed4a5-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ed4a5-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ed4a5-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ed4a5-120">Protocol specifications</span></span>

<span data-ttu-id="ed4a5-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed4a5-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed4a5-122">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="ed4a5-122">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="ed4a5-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed4a5-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed4a5-124">Behandelt das Synchronisieren von Messagingobjekt Daten zwischen einem Server und einem Client.</span><span class="sxs-lookup"><span data-stu-id="ed4a5-124">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="ed4a5-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed4a5-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed4a5-126">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="ed4a5-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ed4a5-127">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="ed4a5-127">Header files</span></span>

<span data-ttu-id="ed4a5-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ed4a5-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="ed4a5-129">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="ed4a5-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="ed4a5-130">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="ed4a5-130">Mapitags.h</span></span>
  
> <span data-ttu-id="ed4a5-131">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="ed4a5-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ed4a5-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed4a5-132">See also</span></span>



[<span data-ttu-id="ed4a5-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ed4a5-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ed4a5-134">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ed4a5-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ed4a5-135">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ed4a5-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ed4a5-136">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ed4a5-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

