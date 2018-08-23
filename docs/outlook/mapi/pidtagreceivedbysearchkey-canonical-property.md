---
title: PidTagReceivedBySearchKey (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedBySearchKey
api_type:
- COM
ms.assetid: 4b37555a-1d07-4f42-95e3-b8fa37ed0c3b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 94d33910650de4f0d625d7a819c66ad8c599a47e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581454"
---
# <a name="pidtagreceivedbysearchkey-canonical-property"></a><span data-ttu-id="e463d-103">PidTagReceivedBySearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e463d-103">PidTagReceivedBySearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="e463d-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e463d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e463d-105">Enthält den Suchschlüssel des messaging Benutzers, der die Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="e463d-105">Contains the search key of the messaging user who receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e463d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e463d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e463d-107">PR_RECEIVED_BY_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="e463d-107">PR_RECEIVED_BY_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="e463d-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e463d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e463d-109">0x0051</span><span class="sxs-lookup"><span data-stu-id="e463d-109">0x0051</span></span>  <br/> |
|<span data-ttu-id="e463d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e463d-110">Data type:</span></span>  <br/> |<span data-ttu-id="e463d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e463d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e463d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e463d-112">Area:</span></span>  <br/> |<span data-ttu-id="e463d-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="e463d-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e463d-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="e463d-114">Remarks</span></span>

<span data-ttu-id="e463d-115">Diese Eigenschaft ist eine der Adresseigenschaften für den messaging-Benutzer, der die Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="e463d-115">This property is one of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="e463d-116">Es muss von der eingehenden Adressbuchhierarchie festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e463d-116">It must be set by the incoming transport provider.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e463d-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e463d-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e463d-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e463d-118">Protocol specifications</span></span>

<span data-ttu-id="e463d-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e463d-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e463d-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e463d-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e463d-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e463d-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e463d-122">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="e463d-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="e463d-123">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e463d-123">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e463d-124">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="e463d-124">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="e463d-125">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e463d-125">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e463d-126">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="e463d-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="e463d-127">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e463d-127">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e463d-128">Gibt die Methoden zum Herstellen einer Verbindung mit und Konfiguration von Postfächer als Stellvertretungen und Interaktionen mit Nachricht und Kalender-Objekte, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="e463d-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="e463d-129">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e463d-129">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e463d-130">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="e463d-130">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e463d-131">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="e463d-131">Header files</span></span>

<span data-ttu-id="e463d-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e463d-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="e463d-133">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e463d-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="e463d-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e463d-134">Mapitags.h</span></span>
  
> <span data-ttu-id="e463d-135">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e463d-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e463d-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e463d-136">See also</span></span>



[<span data-ttu-id="e463d-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e463d-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e463d-138">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e463d-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e463d-139">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e463d-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e463d-140">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e463d-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

