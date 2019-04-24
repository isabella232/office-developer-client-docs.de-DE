---
title: Kanonische Pidtagattachrendering (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 22d3e649641dbe688912ecece7fde73a555f4a88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361096"
---
# <a name="pidtagattachrendering-canonical-property"></a><span data-ttu-id="e0a3a-103">Kanonische Pidtagattachrendering (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e0a3a-103">PidTagAttachRendering Canonical Property</span></span>

  
  
<span data-ttu-id="e0a3a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0a3a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0a3a-105">Enthält eine Microsoft Windows-Metadatei mit Renderinginformationen für eine Anlage.</span><span class="sxs-lookup"><span data-stu-id="e0a3a-105">Contains a Microsoft Windows metafile with rendering information for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e0a3a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e0a3a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e0a3a-107">PR_ATTACH_RENDERING</span><span class="sxs-lookup"><span data-stu-id="e0a3a-107">PR_ATTACH_RENDERING</span></span>  <br/> |
|<span data-ttu-id="e0a3a-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e0a3a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e0a3a-109">0x3709</span><span class="sxs-lookup"><span data-stu-id="e0a3a-109">0x3709</span></span>  <br/> |
|<span data-ttu-id="e0a3a-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e0a3a-110">Data type:</span></span>  <br/> |<span data-ttu-id="e0a3a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e0a3a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e0a3a-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e0a3a-112">Area:</span></span>  <br/> |<span data-ttu-id="e0a3a-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="e0a3a-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0a3a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0a3a-114">Remarks</span></span>

<span data-ttu-id="e0a3a-115">Der Zweck dieser Eigenschaft besteht darin, ein Symbol oder eine andere bildliche Darstellung bereitzustellen, die in der übergeordneten Nachricht am Punkt der Anlage angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e0a3a-115">The purpose of this property is to provide an icon or other pictorial representation that can be displayed within the parent message at the point of attachment.</span></span> <span data-ttu-id="e0a3a-116">Eine solche Darstellung enthält in der Regel den Namen der Anlage, falls vorhanden, und die Art der Anlage, wie beispielsweise ein Microsoft Office Word-Dokument.</span><span class="sxs-lookup"><span data-stu-id="e0a3a-116">Such representation typically includes the name of the attachment, if any, and the nature of the attachment, such as a Microsoft Office Word document.</span></span> <span data-ttu-id="e0a3a-117">Eine Clientanwendung kann diese Darstellung in der Anzeige der Nachricht verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0a3a-117">A client application can use this representation in the display of the message.</span></span> 
  
<span data-ttu-id="e0a3a-118">Für eine angefügte Datei wird in der Regel ein Symbol für die Datei dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e0a3a-118">For an attached file, this property usually portrays an icon for the file.</span></span> 
  
<span data-ttu-id="e0a3a-119">Für eine angefügte Nachricht ist diese Eigenschaft in der Regel nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e0a3a-119">For an attached message, this property is typically not set.</span></span> <span data-ttu-id="e0a3a-120">Eine Clientanwendung, die eine angefügte Nachricht Rendern muss, sollte Ihre **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))-Eigenschaft aufrufen [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) für einen Zeiger auf das entsprechende Formular Informationsobjekt, Öffnen Sie die [IMAPIFormInfo](imapiforminfoimapiprop.md) -Schnittstelle für dieses Objekt, und verwenden Sie GetProps, um die **PR_ICON** ([pidtagicon (](pidtagicon-canonical-property.md)) oder **PR_MINI_ICON** ([pidtagminiicon (](pidtagminiicon-canonical-property.md))-Eigenschaft abzurufen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e0a3a-120">A client application needing to render an attached message should obtain its **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property, call [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) for a pointer to the corresponding form information object, open the [IMAPIFormInfo](imapiforminfoimapiprop.md) interface on that object, and use **GetProps** to retrieve the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="e0a3a-121">Bei einem eingebetteten statischen OLE-Objekt enthält diese Eigenschaft eine Microsoft Windows-Metadatei, die zum Zeichnen der Anlagendarstellung in einem Fenster verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e0a3a-121">For an embedded static OLE object, this property contains a Microsoft Windows metafile that can be used to draw the attachment representation in a window.</span></span> 
  
<span data-ttu-id="e0a3a-122">Bei einem eingebetteten dynamischen OLE-Objekt sollte der Client die OLE-Daten verwenden, um die Renderinginformationen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="e0a3a-122">For an embedded dynamic OLE object, the client should use the OLE data to generate the rendering information.</span></span> 
  
<span data-ttu-id="e0a3a-123">In allen Fällen sollte die Clientanwendung beachten, dass diese Eigenschaft in der Regel mehrere hundert Bytes groß ist und in der Attachment-Tabelle abgeschnitten wird.</span><span class="sxs-lookup"><span data-stu-id="e0a3a-123">In all cases, the client application should be aware that this property is usually several hundred bytes in size and is subject to truncation in the attachment table.</span></span> <span data-ttu-id="e0a3a-124">Wenn ein Client die Anlage aus dieser Eigenschaft Rendern möchte, ohne die Anlage selbst zu öffnen, muss Sie innerhalb der Tabellen Kürzungs Regel funktionieren.</span><span class="sxs-lookup"><span data-stu-id="e0a3a-124">If a client wishes to render the attachment from this property without opening the attachment itself, it must work within the table truncation rule.</span></span> <span data-ttu-id="e0a3a-125">Weitere Informationen finden Sie unter [Arbeiten mit umfangreichen Spalten](working-with-large-columns.md).</span><span class="sxs-lookup"><span data-stu-id="e0a3a-125">For more information, see [Working with Large Columns](working-with-large-columns.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e0a3a-126">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e0a3a-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e0a3a-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e0a3a-127">Protocol specifications</span></span>

<span data-ttu-id="e0a3a-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0a3a-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0a3a-129">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="e0a3a-129">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e0a3a-130">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="e0a3a-130">Header files</span></span>

<span data-ttu-id="e0a3a-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e0a3a-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="e0a3a-132">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="e0a3a-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="e0a3a-133">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e0a3a-133">Mapitags.h</span></span>
  
> <span data-ttu-id="e0a3a-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e0a3a-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e0a3a-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0a3a-135">See also</span></span>



[<span data-ttu-id="e0a3a-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e0a3a-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e0a3a-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e0a3a-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e0a3a-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e0a3a-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e0a3a-139">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e0a3a-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

