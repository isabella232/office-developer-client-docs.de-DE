---
title: PidTagAttachPathname (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPathname
api_type:
- HeaderDef
ms.assetid: e19c7cd1-7c56-4f63-8736-d6971c7c5f4d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: add85bbf9c7608434be045bc30a11b8a28ccaa1e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578409"
---
# <a name="pidtagattachpathname-canonical-property"></a><span data-ttu-id="abed1-103">PidTagAttachPathname (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="abed1-103">PidTagAttachPathname Canonical Property</span></span>

  
  
<span data-ttu-id="abed1-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="abed1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="abed1-105">Enthält einer Anlage vollqualifizierten Pfad und Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="abed1-105">Contains an attachment's fully-qualified path and filename.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="abed1-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="abed1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="abed1-107">PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A, PR_ATTACH_PATHNAME_W</span><span class="sxs-lookup"><span data-stu-id="abed1-107">PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A, PR_ATTACH_PATHNAME_W</span></span>  <br/> |
|<span data-ttu-id="abed1-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="abed1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="abed1-109">0x3708</span><span class="sxs-lookup"><span data-stu-id="abed1-109">0x3708</span></span>  <br/> |
|<span data-ttu-id="abed1-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="abed1-110">Data type:</span></span>  <br/> |<span data-ttu-id="abed1-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="abed1-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="abed1-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="abed1-112">Area:</span></span>  <br/> |<span data-ttu-id="abed1-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="abed1-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="abed1-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="abed1-114">Remarks</span></span>

<span data-ttu-id="abed1-115">Es wird empfohlen, dass Anlage Unterobjekte diese Eigenschaften verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="abed1-115">It is recommended that attachment subobjects expose these properties.</span></span> <span data-ttu-id="abed1-116">Das Festlegen dieser gibt an, dass die Anlagedaten nicht mit der Nachrichten enthalten ist, aber auf einem gemeinsamen Dateiserver verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="abed1-116">Setting them indicates that the attachment data is not included with the message but is available on a common file server.</span></span> <span data-ttu-id="abed1-117">Diese Eigenschaften sind in Verbindung mit einem der **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) Flags, die angeben, Anlage per Verweis erforderlich: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**oder **ATTACH_BY_REF_ NUR**.</span><span class="sxs-lookup"><span data-stu-id="abed1-117">These properties are required in conjunction with any of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) flags that indicate attachment by reference: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, or **ATTACH_BY_REF_ONLY**.</span></span> 
  
<span data-ttu-id="abed1-118">Jedes Verzeichnis oder eine Datei ist auf einen Namen für die acht Zeichen und einer Erweiterung aus drei Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="abed1-118">Each directory or filename is restricted to an eight-character name plus a three-character extension.</span></span> <span data-ttu-id="abed1-119">Der gesamte Pfad ist auf 256 Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="abed1-119">The overall path is restricted to 256 characters.</span></span> <span data-ttu-id="abed1-120">Legen Sie für eine Plattform, die lange Dateinamen unterstützt diese Eigenschaften und die **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="abed1-120">For a platform that supports long filenames, set both these properties and **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)).</span></span> 
  
<span data-ttu-id="abed1-121">-Clientanwendungen sollten in den meisten Fällen eine universelle Benennungskonvention (UNC) verwenden, wenn die Datei gemeinsam verwendet wird und einen absoluten Pfad verwenden sollte, wenn die Datei lokal ist.</span><span class="sxs-lookup"><span data-stu-id="abed1-121">Client applications should use a universal naming convention (UNC) in most cases when the file is shared, and should use an absolute path when the file is local.</span></span>
  
<span data-ttu-id="abed1-122">MAPI-funktioniert nur mit Pfaden und Dateinamen des ANSI-Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="abed1-122">MAPI works only with paths and filenames in the ANSI character set.</span></span> <span data-ttu-id="abed1-123">Clients, die Pfade und Dateinamen in einem OEM-Zeichensatz verwenden, müssen diese in ANSI konvertieren, vor dem Aufruf von MAPI.</span><span class="sxs-lookup"><span data-stu-id="abed1-123">Clients that use paths and filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="abed1-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="abed1-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="abed1-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="abed1-125">Protocol specifications</span></span>

<span data-ttu-id="abed1-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="abed1-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="abed1-127">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="abed1-127">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="abed1-128">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="abed1-128">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="abed1-129">Gibt die Eigenschaften der codierten Nachrichten, deren Rechte verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="abed1-129">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="abed1-130">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="abed1-130">Header files</span></span>

<span data-ttu-id="abed1-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="abed1-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="abed1-132">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="abed1-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="abed1-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="abed1-133">Mapitags.h</span></span>
  
> <span data-ttu-id="abed1-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="abed1-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="abed1-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abed1-135">See also</span></span>



[<span data-ttu-id="abed1-136">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="abed1-136">ScLocalPathFromUNC</span></span>](sclocalpathfromunc.md)
  
[<span data-ttu-id="abed1-137">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="abed1-137">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)


[<span data-ttu-id="abed1-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="abed1-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="abed1-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="abed1-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="abed1-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="abed1-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="abed1-141">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="abed1-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

