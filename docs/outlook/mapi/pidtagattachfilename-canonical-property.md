---
title: PidTagAttachFilename (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFilename
api_type:
- HeaderDef
ms.assetid: cbf34dd6-7733-47f6-9c41-9d82656ca9dc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4468ecd5946c95fab62d0885d9c0b3343a1508dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794100"
---
# <a name="pidtagattachfilename-canonical-property"></a><span data-ttu-id="ab456-103">PidTagAttachFilename (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ab456-103">PidTagAttachFilename Canonical Property</span></span>

  
  
<span data-ttu-id="ab456-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ab456-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ab456-105">Enthält einer Anlage Basis Dateiname und-Erweiterung, ohne Pfad.</span><span class="sxs-lookup"><span data-stu-id="ab456-105">Contains an attachment's base file name and extension, excluding path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ab456-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ab456-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ab456-107">PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W</span><span class="sxs-lookup"><span data-stu-id="ab456-107">PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W</span></span>  <br/> |
|<span data-ttu-id="ab456-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="ab456-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ab456-109">0x3704</span><span class="sxs-lookup"><span data-stu-id="ab456-109">0x3704</span></span>  <br/> |
|<span data-ttu-id="ab456-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ab456-110">Data type:</span></span>  <br/> |<span data-ttu-id="ab456-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ab456-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ab456-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ab456-112">Area:</span></span>  <br/> |<span data-ttu-id="ab456-113">E-Mail-Anlage</span><span class="sxs-lookup"><span data-stu-id="ab456-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab456-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab456-114">Remarks</span></span>

<span data-ttu-id="ab456-115">Es wird empfohlen, dass Attachment-Objekte diese Eigenschaften verfügbar machen, die mit den Werten **ATTACH_BY_VALUE**, **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**und **ATTACH_BY_REF_ONLY** , der die **PR_ATTACH_METHOD** beziehen ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ab456-115">It is recommended that attachment objects expose these properties which pertain to the **ATTACH_BY_VALUE**, **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, and **ATTACH_BY_REF_ONLY** values of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property.</span></span> <span data-ttu-id="ab456-116">**PR_ATTACH_FILENAME** und zugeordneten Eigenschaften sind erforderlich wann diese Werte wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="ab456-116">**PR_ATTACH_FILENAME** and associated properties are required when any of these values is used.</span></span> 
  
<span data-ttu-id="ab456-117">Zum Speichern der Anlage und die Dateinamenerweiterung angeben, wenn die Eigenschaft **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) nicht verfügbar ist, können diese Eigenschaften als einen vorgeschlagenen Dateinamen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab456-117">These properties can be used as a suggested file name for saving the attachment and to supply the file name extension if the **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) property is not provided.</span></span> 
  
<span data-ttu-id="ab456-118">Der Dateiname ist auf acht Zeichen und einer Erweiterung aus drei Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="ab456-118">The file name is restricted to eight characters plus a three-character extension.</span></span> <span data-ttu-id="ab456-119">Legen Sie für eine Plattform, die langer Dateinamen unterstützt diese Eigenschaft und die **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ab456-119">For a platform that supports long file names, set both this property and the **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="ab456-120">MAPI funktioniert nur mit Dateinamen und andere Zeichenfolgen übergeben wurden, in den Zeichensatz amerikanischen National Standards Institute (ANSI).</span><span class="sxs-lookup"><span data-stu-id="ab456-120">MAPI works only with file names, and other strings passed to it, in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="ab456-121">Clientanwendungen, die Dateinamen in einem Zeichensatz OEM (Original Equipment Manufacturer) verwenden, müssen sie in ANSI zu konvertieren vor dem Aufruf von MAPI.</span><span class="sxs-lookup"><span data-stu-id="ab456-121">Client applications that use file names in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ab456-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ab456-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ab456-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ab456-123">Protocol specifications</span></span>

<span data-ttu-id="ab456-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab456-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab456-125">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="ab456-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="ab456-126">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab456-126">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab456-127">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="ab456-127">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="ab456-128">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab456-128">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab456-129">Gibt die Eigenschaften der codierten Nachrichten, deren Rechte verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="ab456-129">Specifies the properties of rights-managed encoded messages.</span></span>
    
<span data-ttu-id="ab456-130">[[MS-OXOSMIME]](http://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab456-130">[[MS-OXOSMIME]](http://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab456-131">Gibt an, S/MIME signiert und verschlüsselt Nachrichteneigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ab456-131">Specifies S/MIME signed and encrypted message properties.</span></span>
    
<span data-ttu-id="ab456-132">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab456-132">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab456-133">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="ab456-133">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ab456-134">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="ab456-134">Header files</span></span>

<span data-ttu-id="ab456-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ab456-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="ab456-136">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ab456-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="ab456-137">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ab456-137">Mapitags.h</span></span>
  
> <span data-ttu-id="ab456-138">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ab456-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ab456-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab456-139">See also</span></span>



[<span data-ttu-id="ab456-140">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab456-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ab456-141">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab456-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ab456-142">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ab456-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ab456-143">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ab456-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

