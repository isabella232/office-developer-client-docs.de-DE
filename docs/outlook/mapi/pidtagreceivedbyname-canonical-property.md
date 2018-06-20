---
title: Kanonische PidTagReceivedByName-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByName
api_type:
- COM
ms.assetid: edd29217-74bb-4321-82fd-65f0fbfd05f8
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7b564b1dda1d72a28e16fad40f0ef90451aaaf0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794877"
---
# <a name="pidtagreceivedbyname-canonical-property"></a><span data-ttu-id="164c3-103">Kanonische PidTagReceivedByName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="164c3-103">PidTagReceivedByName Canonical Property</span></span>

  
  
<span data-ttu-id="164c3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="164c3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="164c3-105">Enthält den Anzeigenamen des Benutzers, der die Nachricht empfängt messaging.</span><span class="sxs-lookup"><span data-stu-id="164c3-105">Contains the display name of the messaging user who receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="164c3-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="164c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="164c3-107">PR_RECEIVED_BY_NAME, PR_RECEIVED_BY_NAME_A, PR_RECEIVED_BY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="164c3-107">PR_RECEIVED_BY_NAME, PR_RECEIVED_BY_NAME_A, PR_RECEIVED_BY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="164c3-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="164c3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="164c3-109">0x0040</span><span class="sxs-lookup"><span data-stu-id="164c3-109">0x0040</span></span>  <br/> |
|<span data-ttu-id="164c3-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="164c3-110">Data type:</span></span>  <br/> |<span data-ttu-id="164c3-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="164c3-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="164c3-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="164c3-112">Area:</span></span>  <br/> |<span data-ttu-id="164c3-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="164c3-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="164c3-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="164c3-114">Remarks</span></span>

<span data-ttu-id="164c3-115">Diese Eigenschaften sind ein Beispiel für die Adresseigenschaften für den messaging-Benutzer, der die Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="164c3-115">These properties are an example of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="164c3-116">Sie müssen von der eingehenden Adressbuchhierarchie festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="164c3-116">They must be set by the incoming transport provider.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="164c3-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="164c3-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="164c3-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="164c3-118">Protocol specifications</span></span>

<span data-ttu-id="164c3-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="164c3-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="164c3-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="164c3-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="164c3-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="164c3-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="164c3-122">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="164c3-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="164c3-123">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="164c3-123">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="164c3-124">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="164c3-124">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="164c3-125">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="164c3-125">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="164c3-126">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="164c3-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="164c3-127">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="164c3-127">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="164c3-128">Gibt die Methoden zum Herstellen einer Verbindung mit und Konfiguration von Postfächer als Stellvertretungen und Interaktionen mit Nachricht und Kalender-Objekte, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="164c3-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="164c3-129">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="164c3-129">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="164c3-130">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="164c3-130">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="164c3-131">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="164c3-131">Header files</span></span>

<span data-ttu-id="164c3-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="164c3-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="164c3-133">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="164c3-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="164c3-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="164c3-134">Mapitags.h</span></span>
  
> <span data-ttu-id="164c3-135">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="164c3-135">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="164c3-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="164c3-136">See also</span></span>



[<span data-ttu-id="164c3-137">Kanonische PidTagDisplayName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="164c3-137">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="164c3-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="164c3-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="164c3-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="164c3-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="164c3-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="164c3-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="164c3-141">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="164c3-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
