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
ms.openlocfilehash: bace518784bf24807cfca09032a4f3912f4e98ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359206"
---
# <a name="pidtagreceivedbysearchkey-canonical-property"></a><span data-ttu-id="0e3e9-103">PidTagReceivedBySearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0e3e9-103">PidTagReceivedBySearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="0e3e9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e3e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e3e9-105">Enthält den Suchschlüssel des Messagingbenutzers, der die Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-105">Contains the search key of the messaging user who receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0e3e9-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0e3e9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0e3e9-107">PR_RECEIVED_BY_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="0e3e9-107">PR_RECEIVED_BY_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="0e3e9-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="0e3e9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0e3e9-109">0x0051</span><span class="sxs-lookup"><span data-stu-id="0e3e9-109">0x0051</span></span>  <br/> |
|<span data-ttu-id="0e3e9-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0e3e9-110">Data type:</span></span>  <br/> |<span data-ttu-id="0e3e9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0e3e9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0e3e9-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0e3e9-112">Area:</span></span>  <br/> |<span data-ttu-id="0e3e9-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="0e3e9-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e3e9-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0e3e9-114">Remarks</span></span>

<span data-ttu-id="0e3e9-115">Diese Eigenschaft ist eine der Adresseigenschaften für den Messagingbenutzer, der die Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-115">This property is one of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="0e3e9-116">Sie muss vom anbieter für eingehende Transporte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-116">It must be set by the incoming transport provider.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0e3e9-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0e3e9-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0e3e9-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0e3e9-118">Protocol specifications</span></span>

<span data-ttu-id="0e3e9-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e3e9-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e3e9-120">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0e3e9-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e3e9-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e3e9-122">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="0e3e9-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e3e9-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e3e9-124">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-124">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="0e3e9-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e3e9-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e3e9-126">Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="0e3e9-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e3e9-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e3e9-128">Gibt Methoden zum Verbinden und Konfigurieren von Postfächern als Stellvertretung sowie Interaktionen mit Nachrichten- und Kalenderobjekten an, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="0e3e9-129">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e3e9-129">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e3e9-130">Codiert und decodiert Nachrichten- und Anlagenobjekte in eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-130">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0e3e9-131">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="0e3e9-131">Header files</span></span>

<span data-ttu-id="0e3e9-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0e3e9-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="0e3e9-133">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="0e3e9-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0e3e9-134">Mapitags.h</span></span>
  
> <span data-ttu-id="0e3e9-135">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0e3e9-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e3e9-136">See also</span></span>



[<span data-ttu-id="0e3e9-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0e3e9-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0e3e9-138">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="0e3e9-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0e3e9-139">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0e3e9-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0e3e9-140">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0e3e9-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

