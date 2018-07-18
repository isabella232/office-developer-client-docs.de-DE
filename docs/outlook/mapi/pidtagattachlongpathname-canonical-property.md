---
title: PidTagAttachLongPathname (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachLongPathname
api_type:
- HeaderDef
ms.assetid: 3262cf95-48b5-4764-a96e-d752ce35b2dc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a2230f2c2b1d4793c425694f76bb79fb7284c479
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794088"
---
# <a name="pidtagattachlongpathname-canonical-property"></a><span data-ttu-id="f92e3-103">PidTagAttachLongPathname (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f92e3-103">PidTagAttachLongPathname Canonical Property</span></span>

  
  
<span data-ttu-id="f92e3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f92e3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f92e3-105">Enthält einer Anlage voll qualifizierte lange Pfad- und Dateiname.</span><span class="sxs-lookup"><span data-stu-id="f92e3-105">Contains an attachment's fully-qualified long path and filename.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f92e3-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f92e3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f92e3-107">PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W</span><span class="sxs-lookup"><span data-stu-id="f92e3-107">PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W</span></span>  <br/> |
|<span data-ttu-id="f92e3-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="f92e3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f92e3-109">0x370D</span><span class="sxs-lookup"><span data-stu-id="f92e3-109">0x370D</span></span>  <br/> |
|<span data-ttu-id="f92e3-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f92e3-110">Data type:</span></span>  <br/> |<span data-ttu-id="f92e3-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f92e3-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f92e3-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f92e3-112">Area:</span></span>  <br/> |<span data-ttu-id="f92e3-113">E-Mail-Anlage</span><span class="sxs-lookup"><span data-stu-id="f92e3-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f92e3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f92e3-114">Remarks</span></span>

<span data-ttu-id="f92e3-115">Diese Eigenschaften sind anwendbar, wenn Sie einen der Werte der **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))-Eigenschaft verwenden, die Anlage per Verweis angeben: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**oder **ATTACH_BY _REF_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="f92e3-115">These properties are applicable when you use any of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property's values that indicate attachment by reference: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, or **ATTACH_BY_REF_ONLY**.</span></span> <span data-ttu-id="f92e3-116">Plattformen, die Unterstützung von langen Dateinamen fest **PR_ATTACH_LONG_PATHNAME** oder zugeordnete Eigenschaften und **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) Eigenschaften beim Senden und **PR_ATTACH_LONG_PATHNAME sollten überprüfen **oder Eigenschaften zuerst beim empfangen.</span><span class="sxs-lookup"><span data-stu-id="f92e3-116">Platforms that support long filenames should set both **PR_ATTACH_LONG_PATHNAME** or associated properties and **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) properties when sending, and should check **PR_ATTACH_LONG_PATHNAME** or associated properties first when receiving.</span></span> 
  
<span data-ttu-id="f92e3-117">Die Clientanwendung sollte legen diese Eigenschaften einer vorgeschlagenen lange Pfad und Dateinamen für verwendet werden, wenn das Hostsystem Empfangen einer Nachricht lange Dateinamen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f92e3-117">The client application should set these properties to a suggested long path and filename to be used if the host machine receiving a message supports long filenames.</span></span> <span data-ttu-id="f92e3-118">Festlegen dieser Eigenschaften gibt an, dass die Anlagedaten nicht mit der Nachrichten enthalten ist, aber auf einem gemeinsamen Dateiserver verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f92e3-118">Setting these properties indicates that the attachment data is not included with the message but is available on a common file server.</span></span> 
  
<span data-ttu-id="f92e3-119">Im Gegensatz zu den Verzeichnissen und Dateinamen von **PR_ATTACH_PATHNAME**bereitgestellt sind diese Verzeichnisse und Dateinamen nicht auf ein Verzeichnis acht Zeichen oder Filename plus Erweiterung aus drei Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="f92e3-119">Unlike the directories and filenames provided by **PR_ATTACH_PATHNAME**, these directories and filenames are not restricted to an eight-character directory or filename plus three-character extension.</span></span> <span data-ttu-id="f92e3-120">Stattdessen kann jede Verzeichnis oder Filename werden bis zu 256 Zeichen lange, einschließlich Name, Erweiterung und Trennzeichen Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="f92e3-120">Instead, each directory or filename can be up to 256 characters long, including the name, extension, and separator period.</span></span> <span data-ttu-id="f92e3-121">Jedoch ist der gesamte Pfad auf 256 Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="f92e3-121">However, the overall path is limited to 256 characters.</span></span> 
  
<span data-ttu-id="f92e3-122">Clients sollten in den meisten Fällen eine universelle Benennungskonvention (UNC) verwenden, wenn die Datei gemeinsam verwendet wird und einen absoluten Pfad verwenden sollte, wenn die Datei lokal ist.</span><span class="sxs-lookup"><span data-stu-id="f92e3-122">Clients should use a universal naming convention (UNC) in most cases when the file is shared, and should use an absolute path when the file is local.</span></span>
  
<span data-ttu-id="f92e3-123">MAPI-funktioniert nur mit Pfaden und Dateinamen des ANSI-Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="f92e3-123">MAPI works only with paths and filenames in the ANSI character set.</span></span> <span data-ttu-id="f92e3-124">Clientanwendungen, die Pfade und Dateinamen in einem OEM-Zeichensatz verwenden, müssen diese in ANSI konvertieren, vor dem Aufruf von MAPI.</span><span class="sxs-lookup"><span data-stu-id="f92e3-124">Client applications that use paths and filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f92e3-125">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f92e3-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f92e3-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f92e3-126">Protocol specifications</span></span>

<span data-ttu-id="f92e3-127">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f92e3-127">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f92e3-128">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="f92e3-128">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="f92e3-129">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f92e3-129">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f92e3-130">Gibt die Eigenschaften der codierten Nachrichten, deren Rechte verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="f92e3-130">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f92e3-131">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="f92e3-131">Header files</span></span>

<span data-ttu-id="f92e3-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f92e3-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="f92e3-133">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f92e3-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="f92e3-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f92e3-134">Mapitags.h</span></span>
  
> <span data-ttu-id="f92e3-135">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f92e3-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f92e3-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f92e3-136">See also</span></span>



[<span data-ttu-id="f92e3-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f92e3-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f92e3-138">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f92e3-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f92e3-139">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f92e3-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f92e3-140">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f92e3-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

