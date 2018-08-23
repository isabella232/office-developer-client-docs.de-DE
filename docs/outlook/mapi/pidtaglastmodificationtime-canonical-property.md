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
ms.openlocfilehash: 653bdf26988c46be5f866cfbda331510c5a54afd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575707"
---
# <a name="pidtaglastmodificationtime-canonical-property"></a><span data-ttu-id="c762c-103">PidTagLastModificationTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c762c-103">PidTagLastModificationTime Canonical Property</span></span>

  
  
<span data-ttu-id="c762c-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c762c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c762c-105">Enthält Datum und Uhrzeit, wann das Objekt oder Unterobjekts zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="c762c-105">Contains the date and time when the object or subobject was last modified.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c762c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c762c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c762c-107">PR_LAST_MODIFICATION_TIME</span><span class="sxs-lookup"><span data-stu-id="c762c-107">PR_LAST_MODIFICATION_TIME</span></span>  <br/> |
|<span data-ttu-id="c762c-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="c762c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c762c-109">0x3008</span><span class="sxs-lookup"><span data-stu-id="c762c-109">0x3008</span></span>  <br/> |
|<span data-ttu-id="c762c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c762c-110">Data type:</span></span>  <br/> |<span data-ttu-id="c762c-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c762c-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="c762c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c762c-112">Area:</span></span>  <br/> |<span data-ttu-id="c762c-113">Nachrichtzeit</span><span class="sxs-lookup"><span data-stu-id="c762c-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c762c-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="c762c-114">Remarks</span></span>

<span data-ttu-id="c762c-115">Diese Eigenschaft ist ursprünglich auf den gleichen Wert wie die Eigenschaft **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c762c-115">This property is initially set to the same value as the **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)) property.</span></span> <span data-ttu-id="c762c-116">Anlage Unterobjekte können sie nach Bedarf aktualisieren, indem Kopieren der Zeitpunkt der letzten Änderung, die systemeigene Dateisystem verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c762c-116">Attachment subobjects can update it as necessary by copying the last modification time maintained by the native file system.</span></span> <span data-ttu-id="c762c-117">Eine Clientanwendung kann diese Eigenschaft erst nach dem ersten Aufruf der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c762c-117">A client application can set this property until the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="c762c-118">Anschließend sollte der Anbieter **PR_LAST_MODIFICATION_TIME** bei jedem Aufruf **IMAPIProp::SaveChanges** aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c762c-118">From then on the provider should update **PR_LAST_MODIFICATION_TIME** during every **IMAPIProp::SaveChanges** call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c762c-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c762c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c762c-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c762c-120">Protocol specifications</span></span>

<span data-ttu-id="c762c-121">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c762c-121">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c762c-122">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="c762c-122">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="c762c-123">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c762c-123">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c762c-124">Synchronisieren von messaging Objektdaten zwischen einem Server und einem Client behandelt.</span><span class="sxs-lookup"><span data-stu-id="c762c-124">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="c762c-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c762c-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c762c-126">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="c762c-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c762c-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="c762c-127">Header files</span></span>

<span data-ttu-id="c762c-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c762c-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="c762c-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c762c-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="c762c-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c762c-130">Mapitags.h</span></span>
  
> <span data-ttu-id="c762c-131">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c762c-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c762c-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c762c-132">See also</span></span>



[<span data-ttu-id="c762c-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c762c-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c762c-134">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c762c-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c762c-135">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c762c-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c762c-136">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c762c-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

