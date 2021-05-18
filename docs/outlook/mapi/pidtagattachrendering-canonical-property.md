---
title: PidTagAttachRendering (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachRendering
api_type:
- HeaderDef
ms.assetid: 1f31f7f4-fbda-4337-95e5-5474dd1bf84a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 22d3e649641dbe688912ecece7fde73a555f4a88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361096"
---
# <a name="pidtagattachrendering-canonical-property"></a><span data-ttu-id="1a90d-103">PidTagAttachRendering (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1a90d-103">PidTagAttachRendering Canonical Property</span></span>

  
  
<span data-ttu-id="1a90d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a90d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a90d-105">Enthält eine Microsoft-Windows-Metadatei mit Renderinginformationen für eine Anlage.</span><span class="sxs-lookup"><span data-stu-id="1a90d-105">Contains a Microsoft Windows metafile with rendering information for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1a90d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1a90d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1a90d-107">PR_ATTACH_RENDERING</span><span class="sxs-lookup"><span data-stu-id="1a90d-107">PR_ATTACH_RENDERING</span></span>  <br/> |
|<span data-ttu-id="1a90d-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="1a90d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1a90d-109">0x3709</span><span class="sxs-lookup"><span data-stu-id="1a90d-109">0x3709</span></span>  <br/> |
|<span data-ttu-id="1a90d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1a90d-110">Data type:</span></span>  <br/> |<span data-ttu-id="1a90d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1a90d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1a90d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1a90d-112">Area:</span></span>  <br/> |<span data-ttu-id="1a90d-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="1a90d-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a90d-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1a90d-114">Remarks</span></span>

<span data-ttu-id="1a90d-115">Der Zweck dieser Eigenschaft besteht in der Bereitstellung eines Symbols oder einer anderen Bilddarstellung, die innerhalb der übergeordneten Nachricht am Anlagenpunkt angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1a90d-115">The purpose of this property is to provide an icon or other pictorial representation that can be displayed within the parent message at the point of attachment.</span></span> <span data-ttu-id="1a90d-116">Eine solche Darstellung umfasst in der Regel den Namen der Anlage(falls) und die Art der Anlage, z. B. ein Microsoft Office Word-Dokument.</span><span class="sxs-lookup"><span data-stu-id="1a90d-116">Such representation typically includes the name of the attachment, if any, and the nature of the attachment, such as a Microsoft Office Word document.</span></span> <span data-ttu-id="1a90d-117">Eine Clientanwendung kann diese Darstellung in der Anzeige der Nachricht verwenden.</span><span class="sxs-lookup"><span data-stu-id="1a90d-117">A client application can use this representation in the display of the message.</span></span> 
  
<span data-ttu-id="1a90d-118">Bei einer angefügten Datei zeichnet diese Eigenschaft in der Regel ein Symbol für die Datei auf.</span><span class="sxs-lookup"><span data-stu-id="1a90d-118">For an attached file, this property usually portrays an icon for the file.</span></span> 
  
<span data-ttu-id="1a90d-119">Für eine angefügte Nachricht wird diese Eigenschaft in der Regel nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1a90d-119">For an attached message, this property is typically not set.</span></span> <span data-ttu-id="1a90d-120">Eine Clientanwendung, die eine angefügte Nachricht **rendern** muss, sollte die PR_MESSAGE_CLASS ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))-Eigenschaft abrufen, [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) für einen Zeiger auf das entsprechende Formularinformationsobjekt aufrufen, die [IMAPIFormInfo-Schnittstelle](imapiforminfoimapiprop.md) für dieses Objekt öffnen und **GetProps** verwenden, um die **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) oder PR_MINI_ICON ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) **-Eigenschaft** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1a90d-120">A client application needing to render an attached message should obtain its **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property, call [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) for a pointer to the corresponding form information object, open the [IMAPIFormInfo](imapiforminfoimapiprop.md) interface on that object, and use **GetProps** to retrieve the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="1a90d-121">Für ein eingebettetes statisches OLE-Objekt enthält diese Eigenschaft eine Microsoft Windows-Metadatei, die zum Zeichnen der Anlagendarstellung in einem Fenster verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1a90d-121">For an embedded static OLE object, this property contains a Microsoft Windows metafile that can be used to draw the attachment representation in a window.</span></span> 
  
<span data-ttu-id="1a90d-122">Für ein eingebettetes dynamisches OLE-Objekt sollte der Client die OLE-Daten verwenden, um die Renderinginformationen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="1a90d-122">For an embedded dynamic OLE object, the client should use the OLE data to generate the rendering information.</span></span> 
  
<span data-ttu-id="1a90d-123">In allen Fällen sollte die Clientanwendung beachten, dass diese Eigenschaft in der Regel mehrere hundert Bytes groß ist und in der Anlagentabelle abgeschnitten werden muss.</span><span class="sxs-lookup"><span data-stu-id="1a90d-123">In all cases, the client application should be aware that this property is usually several hundred bytes in size and is subject to truncation in the attachment table.</span></span> <span data-ttu-id="1a90d-124">Wenn ein Client die Anlage aus dieser Eigenschaft rendern möchte, ohne die Anlage selbst zu öffnen, muss sie innerhalb der Tabellenkürzungsregel funktionieren.</span><span class="sxs-lookup"><span data-stu-id="1a90d-124">If a client wishes to render the attachment from this property without opening the attachment itself, it must work within the table truncation rule.</span></span> <span data-ttu-id="1a90d-125">Weitere Informationen finden Sie unter [Working with Large Columns](working-with-large-columns.md).</span><span class="sxs-lookup"><span data-stu-id="1a90d-125">For more information, see [Working with Large Columns](working-with-large-columns.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1a90d-126">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1a90d-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1a90d-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1a90d-127">Protocol specifications</span></span>

<span data-ttu-id="1a90d-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a90d-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a90d-129">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="1a90d-129">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1a90d-130">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="1a90d-130">Header files</span></span>

<span data-ttu-id="1a90d-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1a90d-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="1a90d-132">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1a90d-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="1a90d-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1a90d-133">Mapitags.h</span></span>
  
> <span data-ttu-id="1a90d-134">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="1a90d-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a90d-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a90d-135">See also</span></span>



[<span data-ttu-id="1a90d-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1a90d-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1a90d-137">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="1a90d-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1a90d-138">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1a90d-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1a90d-139">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1a90d-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

