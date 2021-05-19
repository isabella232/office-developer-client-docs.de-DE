---
title: PidTagTransmittableDisplayName (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTransmittableDisplayName
api_type:
- COM
ms.assetid: aadd9086-b936-4067-bf7d-f54fc50e3c83
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e66fe8d3621c122ccc19bdde169f20f7d47a148d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331857"
---
# <a name="pidtagtransmittabledisplayname-canonical-property"></a><span data-ttu-id="3660a-103">PidTagTransmittableDisplayName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3660a-103">PidTagTransmittableDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="3660a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3660a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3660a-105">Enthält den Anzeigenamen eines Empfängers in einem sicheren Formular, das nicht geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="3660a-105">Contains a recipient's display name in a secure form that cannot be changed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3660a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="3660a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3660a-107">PR_TRANSMITABLE_DISPLAY_NAME, PR_TRANSMITABLE_DISPLAY_NAME_A, PR_TRANSMITABLE_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="3660a-107">PR_TRANSMITABLE_DISPLAY_NAME, PR_TRANSMITABLE_DISPLAY_NAME_A, PR_TRANSMITABLE_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="3660a-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="3660a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3660a-109">0x3A20</span><span class="sxs-lookup"><span data-stu-id="3660a-109">0x3A20</span></span>  <br/> |
|<span data-ttu-id="3660a-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="3660a-110">Data type:</span></span>  <br/> |<span data-ttu-id="3660a-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="3660a-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="3660a-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="3660a-112">Area:</span></span>  <br/> |<span data-ttu-id="3660a-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="3660a-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3660a-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3660a-114">Remarks</span></span>

<span data-ttu-id="3660a-115">Diese Eigenschaften sollten von allen Adressbuchanbietern implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="3660a-115">These properties should be implemented by all address book providers.</span></span> <span data-ttu-id="3660a-116">Sie enthalten die Version des Anzeigenamens des Empfängers, die mit der Nachricht übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="3660a-116">They contain the version of the recipient's display name that is transmitted with the message.</span></span> <span data-ttu-id="3660a-117">Für die meisten Adressbuchanbieter haben diese Eigenschaften denselben Wert wie die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="3660a-117">For most address book providers these properties have the same value as the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="3660a-118">Anbieter ohne sicheren Anzeigenamen geben PT_ERROR und MAPI ändert den Anzeigenamen durch Hinzufügen von Anführungszeichen um den Namen.</span><span class="sxs-lookup"><span data-stu-id="3660a-118">Providers that do not have a secure display name return PT_ERROR and MAPI changes the display name by adding quotation marks around the name.</span></span>
  
<span data-ttu-id="3660a-119">Eine Clientanwendung kann diese Eigenschaft verwenden, um änderungen oder "Spoofing" von Einträgen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="3660a-119">A client application can use this property to prevent alteration or "spoofing" of entries.</span></span> <span data-ttu-id="3660a-120">Ein Beispiel für Spoofing ist die Übertragung von John Doe als John (What a Guy) Doe.</span><span class="sxs-lookup"><span data-stu-id="3660a-120">An example of spoofing is transmitting John Doe as John (What a Guy) Doe.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3660a-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3660a-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3660a-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="3660a-122">Protocol specifications</span></span>

<span data-ttu-id="3660a-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3660a-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3660a-124">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="3660a-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3660a-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3660a-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3660a-126">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="3660a-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="3660a-127">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3660a-127">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3660a-128">Verarbeitet die Kommunikation eines Clients mit einem NSPI-Server (Name Service Provider Interface).</span><span class="sxs-lookup"><span data-stu-id="3660a-128">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="3660a-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3660a-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3660a-130">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="3660a-130">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="3660a-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3660a-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3660a-132">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="3660a-132">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3660a-133">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="3660a-133">Header files</span></span>

<span data-ttu-id="3660a-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3660a-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="3660a-135">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="3660a-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="3660a-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3660a-136">Mapitags.h</span></span>
  
> <span data-ttu-id="3660a-137">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="3660a-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3660a-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3660a-138">See also</span></span>



[<span data-ttu-id="3660a-139">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3660a-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3660a-140">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="3660a-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3660a-141">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="3660a-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3660a-142">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="3660a-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

