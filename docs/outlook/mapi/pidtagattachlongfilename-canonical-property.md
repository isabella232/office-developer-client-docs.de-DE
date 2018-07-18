---
title: PidTagAttachLongFilename (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachLongFilename
api_type:
- HeaderDef
ms.assetid: 83b69e8f-0b5a-4992-b5b8-160d3bdfa22a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0debee5d480c4ea0c0a8fb4b54d9fa5d92a45987
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794098"
---
# <a name="pidtagattachlongfilename-canonical-property"></a><span data-ttu-id="6fd87-103">PidTagAttachLongFilename (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6fd87-103">PidTagAttachLongFilename Canonical Property</span></span>

  
  
<span data-ttu-id="6fd87-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6fd87-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6fd87-105">Enthält einer Anlage langer Dateiname und Erweiterung, ohne Pfad.</span><span class="sxs-lookup"><span data-stu-id="6fd87-105">Contains an attachment's long filename and extension, excluding path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6fd87-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6fd87-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6fd87-107">PR_ATTACH_LONG_FILENAME, PR_ATTACH_LONG_FILENAME_A, PR_ATTACH_LONG_FILENAME_W</span><span class="sxs-lookup"><span data-stu-id="6fd87-107">PR_ATTACH_LONG_FILENAME, PR_ATTACH_LONG_FILENAME_A, PR_ATTACH_LONG_FILENAME_W</span></span>  <br/> |
|<span data-ttu-id="6fd87-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="6fd87-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6fd87-109">0x3707</span><span class="sxs-lookup"><span data-stu-id="6fd87-109">0x3707</span></span>  <br/> |
|<span data-ttu-id="6fd87-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6fd87-110">Data type:</span></span>  <br/> |<span data-ttu-id="6fd87-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6fd87-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6fd87-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6fd87-112">Area:</span></span>  <br/> |<span data-ttu-id="6fd87-113">E-Mail-Anlage</span><span class="sxs-lookup"><span data-stu-id="6fd87-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6fd87-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6fd87-114">Remarks</span></span>

<span data-ttu-id="6fd87-115">Diese Eigenschaften beziehen sich auf die Werte ATTACH_BY_VALUE, ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE und ATTACH_BY_REF_ONLY der **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6fd87-115">These properties pertain to the ATTACH_BY_VALUE, ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE, and ATTACH_BY_REF_ONLY values of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property.</span></span> <span data-ttu-id="6fd87-116">Plattformen, die lange Dateinamen unterstützen sollte Festlegen der **PR_ATTACH_LONG_FILENAME** und die Eigenschaften **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) beim Senden, und überprüfen **PR_ATTACH_LONG_FILENAME** zuerst bei empfangen.</span><span class="sxs-lookup"><span data-stu-id="6fd87-116">Platforms that support long filenames should set both the **PR_ATTACH_LONG_FILENAME** and **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) properties when sending, and should check **PR_ATTACH_LONG_FILENAME** first when receiving.</span></span> 
  
<span data-ttu-id="6fd87-117">Die Clientanwendung sollte diese Eigenschaft auf einen vorgeschlagenen langen Dateinamen verwendet werden, wenn der Hostcomputer Empfangen einer Nachricht lange Dateinamen unterstützt festlegen.</span><span class="sxs-lookup"><span data-stu-id="6fd87-117">The client application should set this property to a suggested long filename to be used if the host computer receiving a message supports long filenames.</span></span> <span data-ttu-id="6fd87-118">**PR_ATTACH_LONG_FILENAME** kann verwendet werden, als einen Dateinamen für die Anlage speichern und die Erweiterung Filename angeben, wenn die Eigenschaft **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6fd87-118">**PR_ATTACH_LONG_FILENAME** can be used as a filename for saving the attachment, and to supply the filename extension if the **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) property is not provided.</span></span> 
  
<span data-ttu-id="6fd87-119">Im Gegensatz zu den Dateinamen von **PR_ATTACH_FILENAME**bereitgestellt wird ist dieser Name nicht auf ein Dateiname acht Zeichen und einer Erweiterung aus drei Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="6fd87-119">Unlike the filename provided by **PR_ATTACH_FILENAME**, this name is not restricted to an eight-character filename plus a three-character extension.</span></span> <span data-ttu-id="6fd87-120">In diesem Fall kann es bis zu 256 Zeichen lange, einschließlich des Punkts Dateiname, Erweiterung und Trennzeichen sein.</span><span class="sxs-lookup"><span data-stu-id="6fd87-120">Instead, it can be up to 256 characters long, including the filename, extension, and separator period.</span></span> 
  
<span data-ttu-id="6fd87-121">MAPI funktioniert nur mit Dateinamen im ANSI-Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="6fd87-121">MAPI works only with filenames in the ANSI character set.</span></span> <span data-ttu-id="6fd87-122">Clientanwendungen, die Dateinamen in einem OEM-Zeichensatz verwenden, müssen diese in ANSI konvertieren, vor dem Aufruf von MAPI.</span><span class="sxs-lookup"><span data-stu-id="6fd87-122">Client applications that use filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6fd87-123">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6fd87-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6fd87-124">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="6fd87-124">Protocol specifications</span></span>

<span data-ttu-id="6fd87-125">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6fd87-125">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6fd87-126">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="6fd87-126">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="6fd87-127">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6fd87-127">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6fd87-128">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="6fd87-128">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="6fd87-129">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6fd87-129">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6fd87-130">Gibt die Eigenschaften der codierten Nachrichten, deren Rechte verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="6fd87-130">Specifies the properties of rights-managed encoded messages.</span></span>
    
<span data-ttu-id="6fd87-131">[[MS-OXOUM]](http://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6fd87-131">[[MS-OXOUM]](http://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6fd87-132">Gibt die Eigenschaften und Operationen, die für das Darstellen von Voicemail- und Sprachnachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="6fd87-132">Specifies the properties and operations that are permissible for representing voice mail and fax messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6fd87-133">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="6fd87-133">Header files</span></span>

<span data-ttu-id="6fd87-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6fd87-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="6fd87-135">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6fd87-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="6fd87-136">Mmapitags.h</span><span class="sxs-lookup"><span data-stu-id="6fd87-136">Mmapitags.h</span></span>
  
> <span data-ttu-id="6fd87-137">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6fd87-137">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6fd87-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fd87-138">See also</span></span>



[<span data-ttu-id="6fd87-139">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6fd87-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6fd87-140">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6fd87-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6fd87-141">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6fd87-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6fd87-142">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6fd87-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

