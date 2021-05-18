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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f5dcf90e8224f1bf2e96042a7344109293cc2c3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319222"
---
# <a name="pidtagattachfilename-canonical-property"></a><span data-ttu-id="17ed3-103">PidTagAttachFilename (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="17ed3-103">PidTagAttachFilename Canonical Property</span></span>

  
  
<span data-ttu-id="17ed3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17ed3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17ed3-105">Enthält den Basisdateinamen und die Erweiterung einer Anlage, mit Ausnahme des Pfads.</span><span class="sxs-lookup"><span data-stu-id="17ed3-105">Contains an attachment's base file name and extension, excluding path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="17ed3-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="17ed3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="17ed3-107">PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W</span><span class="sxs-lookup"><span data-stu-id="17ed3-107">PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W</span></span>  <br/> |
|<span data-ttu-id="17ed3-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="17ed3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="17ed3-109">0x3704</span><span class="sxs-lookup"><span data-stu-id="17ed3-109">0x3704</span></span>  <br/> |
|<span data-ttu-id="17ed3-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="17ed3-110">Data type:</span></span>  <br/> |<span data-ttu-id="17ed3-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="17ed3-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="17ed3-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="17ed3-112">Area:</span></span>  <br/> |<span data-ttu-id="17ed3-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="17ed3-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17ed3-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="17ed3-114">Remarks</span></span>

<span data-ttu-id="17ed3-115">Es wird empfohlen, dass Anlagenobjekte diese Eigenschaften verfügbar machen, die sich auf die **ATTACH_BY_VALUE-,** **ATTACH_BY_REFERENCE-,** **ATTACH_BY_REF_RESOLVE-** und **ATTACH_BY_REF_ONLY-Werte** der **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))-Eigenschaft bezieht.</span><span class="sxs-lookup"><span data-stu-id="17ed3-115">It is recommended that attachment objects expose these properties which pertain to the **ATTACH_BY_VALUE**, **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, and **ATTACH_BY_REF_ONLY** values of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property.</span></span> <span data-ttu-id="17ed3-116">**PR_ATTACH_FILENAME** und zugeordnete Eigenschaften sind erforderlich, wenn einer dieser Werte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="17ed3-116">**PR_ATTACH_FILENAME** and associated properties are required when any of these values is used.</span></span> 
  
<span data-ttu-id="17ed3-117">Diese Eigenschaften können als vorgeschlagener Dateiname zum Speichern der Anlage und zum Eingeben der Dateinamenerweiterung verwendet werden, wenn die **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) -Eigenschaft nicht bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="17ed3-117">These properties can be used as a suggested file name for saving the attachment and to supply the file name extension if the **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) property is not provided.</span></span> 
  
<span data-ttu-id="17ed3-118">Der Dateiname ist auf acht Zeichen plus eine Drei-Zeichen-Erweiterung beschränkt.</span><span class="sxs-lookup"><span data-stu-id="17ed3-118">The file name is restricted to eight characters plus a three-character extension.</span></span> <span data-ttu-id="17ed3-119">Legen Sie für eine Plattform, die lange Dateinamen unterstützt, sowohl diese Eigenschaft als auch die **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="17ed3-119">For a platform that supports long file names, set both this property and the **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="17ed3-120">MAPI kann nur mit Dateinamen und anderen Zeichenfolgen verwendet werden, die im Zeichensatz American National Standards Institute (ANSI) übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="17ed3-120">MAPI works only with file names, and other strings passed to it, in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="17ed3-121">Clientanwendungen, die Dateinamen in einem OEM-Zeichensatz (Original Equipment Manufacturer) verwenden, müssen sie vor dem Aufrufen von MAPI in ANSI konvertieren.</span><span class="sxs-lookup"><span data-stu-id="17ed3-121">Client applications that use file names in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="17ed3-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="17ed3-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="17ed3-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="17ed3-123">Protocol specifications</span></span>

<span data-ttu-id="17ed3-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17ed3-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17ed3-125">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="17ed3-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="17ed3-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17ed3-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17ed3-127">Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="17ed3-127">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="17ed3-128">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17ed3-128">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17ed3-129">Gibt die Eigenschaften von mit Rechten verwalteten codierten Nachrichten an.</span><span class="sxs-lookup"><span data-stu-id="17ed3-129">Specifies the properties of rights-managed encoded messages.</span></span>
    
<span data-ttu-id="17ed3-130">[[MS-OXOSMIME]](https://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17ed3-130">[[MS-OXOSMIME]](https://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17ed3-131">Gibt signierte und verschlüsselte S/MIME-Nachrichteneigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="17ed3-131">Specifies S/MIME signed and encrypted message properties.</span></span>
    
<span data-ttu-id="17ed3-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17ed3-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17ed3-133">Codiert und decodiert Nachrichten- und Anlagenobjekte in eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="17ed3-133">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="17ed3-134">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="17ed3-134">Header files</span></span>

<span data-ttu-id="17ed3-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="17ed3-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="17ed3-136">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="17ed3-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="17ed3-137">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="17ed3-137">Mapitags.h</span></span>
  
> <span data-ttu-id="17ed3-138">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="17ed3-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="17ed3-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17ed3-139">See also</span></span>



[<span data-ttu-id="17ed3-140">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="17ed3-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="17ed3-141">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="17ed3-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="17ed3-142">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="17ed3-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="17ed3-143">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="17ed3-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

