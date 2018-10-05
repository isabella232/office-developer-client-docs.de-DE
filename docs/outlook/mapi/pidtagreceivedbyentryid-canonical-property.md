---
title: PidTagReceivedByEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByEntryId
api_type:
- COM
ms.assetid: 737f8584-fc52-4324-ac40-2fc554a3095d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2f0203fc787ced9a0198be10c238f6245cb15144
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383856"
---
# <a name="pidtagreceivedbyentryid-canonical-property"></a><span data-ttu-id="95b65-103">PidTagReceivedByEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="95b65-103">PidTagReceivedByEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="95b65-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95b65-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95b65-105">Enthält die Eintrags-ID des Benutzers, der die Nachricht tatsächlich empfängt messaging.</span><span class="sxs-lookup"><span data-stu-id="95b65-105">Contains the entry identifier of the messaging user who actually receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="95b65-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="95b65-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="95b65-107">PR_RECEIVED_BY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="95b65-107">PR_RECEIVED_BY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="95b65-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="95b65-108">Identifier:</span></span>  <br/> |<span data-ttu-id="95b65-109">0x003F</span><span class="sxs-lookup"><span data-stu-id="95b65-109">0x003F</span></span>  <br/> |
|<span data-ttu-id="95b65-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="95b65-110">Data type:</span></span>  <br/> |<span data-ttu-id="95b65-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="95b65-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="95b65-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="95b65-112">Area:</span></span>  <br/> |<span data-ttu-id="95b65-113">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="95b65-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95b65-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="95b65-114">Remarks</span></span>

<span data-ttu-id="95b65-115">Diese Eigenschaft ist eine der Adresseigenschaften für den messaging-Benutzer, der die Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="95b65-115">This property is one of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="95b65-116">Es muss von der eingehenden Adressbuchhierarchie festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="95b65-116">It must be set by the incoming transport provider.</span></span>
  
<span data-ttu-id="95b65-117">Diese Eigenschaft entspricht einem x. 400-Übermittlung Umschlag pro Nachricht MH_T_-Attribut.</span><span class="sxs-lookup"><span data-stu-id="95b65-117">This property corresponds to an X.400 delivery envelope per-message MH_T_ attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="95b65-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="95b65-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="95b65-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="95b65-119">Protocol specifications</span></span>

<span data-ttu-id="95b65-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95b65-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95b65-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="95b65-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="95b65-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95b65-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95b65-123">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="95b65-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="95b65-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95b65-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95b65-125">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="95b65-125">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="95b65-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95b65-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95b65-127">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und Besprechungsanfragen.</span><span class="sxs-lookup"><span data-stu-id="95b65-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
<span data-ttu-id="95b65-128">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95b65-128">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95b65-129">Gibt die Methoden zum Herstellen einer Verbindung mit und Konfiguration von Postfächer als Stellvertretungen und Interaktionen mit Nachricht und Kalender-Objekte, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="95b65-129">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="95b65-130">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95b65-130">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95b65-131">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="95b65-131">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="95b65-132">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="95b65-132">Header files</span></span>

<span data-ttu-id="95b65-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="95b65-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="95b65-134">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="95b65-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="95b65-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="95b65-135">Mapitags.h</span></span>
  
> <span data-ttu-id="95b65-136">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="95b65-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="95b65-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95b65-137">See also</span></span>



[<span data-ttu-id="95b65-138">PidTagEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="95b65-138">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)


[<span data-ttu-id="95b65-139">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="95b65-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="95b65-140">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="95b65-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="95b65-141">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="95b65-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="95b65-142">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="95b65-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

