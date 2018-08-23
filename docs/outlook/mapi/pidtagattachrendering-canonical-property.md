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
ms.openlocfilehash: 45d4b0bfe7f902ee2cfe1d735c990d80f8fbb60d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588944"
---
# <a name="pidtagattachrendering-canonical-property"></a><span data-ttu-id="56545-103">PidTagAttachRendering (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="56545-103">PidTagAttachRendering Canonical Property</span></span>

  
  
<span data-ttu-id="56545-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56545-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56545-105">Eine Microsoft Windows-Metadatei mit Informationen für eine Anlage enthält.</span><span class="sxs-lookup"><span data-stu-id="56545-105">Contains a Microsoft Windows metafile with rendering information for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="56545-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="56545-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="56545-107">PR_ATTACH_RENDERING</span><span class="sxs-lookup"><span data-stu-id="56545-107">PR_ATTACH_RENDERING</span></span>  <br/> |
|<span data-ttu-id="56545-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="56545-108">Identifier:</span></span>  <br/> |<span data-ttu-id="56545-109">0x3709</span><span class="sxs-lookup"><span data-stu-id="56545-109">0x3709</span></span>  <br/> |
|<span data-ttu-id="56545-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="56545-110">Data type:</span></span>  <br/> |<span data-ttu-id="56545-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="56545-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="56545-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="56545-112">Area:</span></span>  <br/> |<span data-ttu-id="56545-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="56545-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56545-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="56545-114">Remarks</span></span>

<span data-ttu-id="56545-115">Der Zweck dieser Eigenschaft ist ein Symbol oder andere bildliche Darstellung, die innerhalb der übergeordneten Nachricht zum Zeitpunkt der Anlage angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="56545-115">The purpose of this property is to provide an icon or other pictorial representation that can be displayed within the parent message at the point of attachment.</span></span> <span data-ttu-id="56545-116">Diese Darstellung umfasst in der Regel den Namen der Anlage, falls vorhanden, und die Art der Anlage, wie beispielsweise Microsoft Office Word-Dokument.</span><span class="sxs-lookup"><span data-stu-id="56545-116">Such representation typically includes the name of the attachment, if any, and the nature of the attachment, such as a Microsoft Office Word document.</span></span> <span data-ttu-id="56545-117">Eine Clientanwendung können diese Darstellung in der Anzeige der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="56545-117">A client application can use this representation in the display of the message.</span></span> 
  
<span data-ttu-id="56545-118">Bei einer Anlage dargestellt ist diese Eigenschaft in der Regel ein Symbol für die Datei.</span><span class="sxs-lookup"><span data-stu-id="56545-118">For an attached file, this property usually portrays an icon for the file.</span></span> 
  
<span data-ttu-id="56545-119">Diese Eigenschaft ist für eine angefügte Nachricht in der Regel nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="56545-119">For an attached message, this property is typically not set.</span></span> <span data-ttu-id="56545-120">Eine Clientanwendung zum Rendern einer angefügten Nachricht benötigen sollte seine Eigenschaft **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) zu erhalten, rufen Sie [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) für einen Zeiger auf das entsprechende Informationen Formularobjekt, Öffnen Sie die [IMAPIFormInfo](imapiforminfoimapiprop.md) -Benutzeroberfläche für dieses Objekt und verwenden Sie **GetProps** zum Abrufen des **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) oder **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="56545-120">A client application needing to render an attached message should obtain its **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property, call [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) for a pointer to the corresponding form information object, open the [IMAPIFormInfo](imapiforminfoimapiprop.md) interface on that object, and use **GetProps** to retrieve the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="56545-121">Bei einem eingebetteten statische OLE-Objekt enthält diese Eigenschaft eine Microsoft Windows-Metadatei, die verwendet werden kann, um die Darstellung der Anlage in einem Fenster zeichnen.</span><span class="sxs-lookup"><span data-stu-id="56545-121">For an embedded static OLE object, this property contains a Microsoft Windows metafile that can be used to draw the attachment representation in a window.</span></span> 
  
<span data-ttu-id="56545-122">Der Client sollte für ein eingebettetes dynamische OLE-Objekt OLE-Daten verwenden, um die Wiedergabe von Informationen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="56545-122">For an embedded dynamic OLE object, the client should use the OLE data to generate the rendering information.</span></span> 
  
<span data-ttu-id="56545-123">In allen Fällen beachten die Clientanwendung Sie, dass diese Eigenschaft in der Regel mehrere hundert Bytes in Größe ist und Abschneiden in der Tabelle Dateianhang unterliegt.</span><span class="sxs-lookup"><span data-stu-id="56545-123">In all cases, the client application should be aware that this property is usually several hundred bytes in size and is subject to truncation in the attachment table.</span></span> <span data-ttu-id="56545-124">Wenn ein Client die Anlage aus dieser Eigenschaft Rendern möchte, ohne die Anlage selbst zu öffnen, müssen sie innerhalb der Tabelle abschneiden Regel arbeiten.</span><span class="sxs-lookup"><span data-stu-id="56545-124">If a client wishes to render the attachment from this property without opening the attachment itself, it must work within the table truncation rule.</span></span> <span data-ttu-id="56545-125">Weitere Informationen finden Sie unter [Arbeiten mit großen Spalten](working-with-large-columns.md).</span><span class="sxs-lookup"><span data-stu-id="56545-125">For more information, see [Working with Large Columns](working-with-large-columns.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="56545-126">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="56545-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="56545-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="56545-127">Protocol specifications</span></span>

<span data-ttu-id="56545-128">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56545-128">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56545-129">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="56545-129">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="56545-130">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="56545-130">Header files</span></span>

<span data-ttu-id="56545-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="56545-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="56545-132">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="56545-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="56545-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="56545-133">Mapitags.h</span></span>
  
> <span data-ttu-id="56545-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="56545-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="56545-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56545-135">See also</span></span>



[<span data-ttu-id="56545-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="56545-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="56545-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="56545-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="56545-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="56545-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="56545-139">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="56545-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

