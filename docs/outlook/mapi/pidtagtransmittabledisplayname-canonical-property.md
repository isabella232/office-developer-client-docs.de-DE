---
title: Kanonische Pidtagtransmittabledisplayname (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e66fe8d3621c122ccc19bdde169f20f7d47a148d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331857"
---
# <a name="pidtagtransmittabledisplayname-canonical-property"></a><span data-ttu-id="82500-103">Kanonische Pidtagtransmittabledisplayname (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="82500-103">PidTagTransmittableDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="82500-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82500-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82500-105">Enthält den Anzeigenamen eines Empfängers in einem sicheren Formular, das nicht geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="82500-105">Contains a recipient's display name in a secure form that cannot be changed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="82500-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="82500-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="82500-107">PR_TRANSMITABLE_DISPLAY_NAME, PR_TRANSMITABLE_DISPLAY_NAME_A, PR_TRANSMITABLE_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="82500-107">PR_TRANSMITABLE_DISPLAY_NAME, PR_TRANSMITABLE_DISPLAY_NAME_A, PR_TRANSMITABLE_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="82500-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="82500-108">Identifier:</span></span>  <br/> |<span data-ttu-id="82500-109">0x3A20</span><span class="sxs-lookup"><span data-stu-id="82500-109">0x3A20</span></span>  <br/> |
|<span data-ttu-id="82500-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="82500-110">Data type:</span></span>  <br/> |<span data-ttu-id="82500-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="82500-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="82500-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="82500-112">Area:</span></span>  <br/> |<span data-ttu-id="82500-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="82500-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82500-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82500-114">Remarks</span></span>

<span data-ttu-id="82500-115">Diese Eigenschaften sollten von allen Adressbuch Anbietern implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="82500-115">These properties should be implemented by all address book providers.</span></span> <span data-ttu-id="82500-116">Sie enthalten die Version des Anzeigenamens des Empfängers, der mit der Nachricht übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="82500-116">They contain the version of the recipient's display name that is transmitted with the message.</span></span> <span data-ttu-id="82500-117">Für die meisten Adressbuchanbieter haben diese Eigenschaften den gleichen Wert wie die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="82500-117">For most address book providers these properties have the same value as the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="82500-118">Anbieter, die keinen sicheren Anzeigenamen aufweisen, geben PT_ERROR und MAPI den Anzeigenamen aus, indem Sie dem Namen Anführungszeichen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="82500-118">Providers that do not have a secure display name return PT_ERROR and MAPI changes the display name by adding quotation marks around the name.</span></span>
  
<span data-ttu-id="82500-119">Eine Clientanwendung kann diese Eigenschaft verwenden, um Änderungen oder Spoofing von Einträgen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="82500-119">A client application can use this property to prevent alteration or "spoofing" of entries.</span></span> <span data-ttu-id="82500-120">Ein Beispiel für Spoofing ist John Doe als John (What a Guy) DOE.</span><span class="sxs-lookup"><span data-stu-id="82500-120">An example of spoofing is transmitting John Doe as John (What a Guy) Doe.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="82500-121">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="82500-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="82500-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="82500-122">Protocol specifications</span></span>

<span data-ttu-id="82500-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82500-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82500-124">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="82500-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="82500-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82500-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82500-126">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="82500-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="82500-127">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82500-127">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82500-128">Verarbeitet die Kommunikation eines Clients mit einem NSPI-Server (Name Service Provider Interface).</span><span class="sxs-lookup"><span data-stu-id="82500-128">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="82500-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82500-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82500-130">Verarbeitet die Reihenfolge und den Ablauf für die Datenübertragung zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="82500-130">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="82500-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82500-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82500-132">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="82500-132">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="82500-133">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="82500-133">Header files</span></span>

<span data-ttu-id="82500-134">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="82500-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="82500-135">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="82500-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="82500-136">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="82500-136">Mapitags.h</span></span>
  
> <span data-ttu-id="82500-137">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="82500-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="82500-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82500-138">See also</span></span>



[<span data-ttu-id="82500-139">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="82500-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="82500-140">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="82500-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="82500-141">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="82500-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="82500-142">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="82500-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

