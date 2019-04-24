---
title: Kanonische Pidtagattachlongpathname (-Eigenschaft
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
ms.openlocfilehash: d8fe8525cf4fc11ac17ed6d73fb5d97e4f2d003e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339368"
---
# <a name="pidtagattachlongpathname-canonical-property"></a><span data-ttu-id="416e6-103">Kanonische Pidtagattachlongpathname (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="416e6-103">PidTagAttachLongPathname Canonical Property</span></span>

  
  
<span data-ttu-id="416e6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="416e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="416e6-105">Enthält den vollqualifizierten Long-Pfad und Dateinamen einer Anlage.</span><span class="sxs-lookup"><span data-stu-id="416e6-105">Contains an attachment's fully-qualified long path and filename.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="416e6-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="416e6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="416e6-107">PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W</span><span class="sxs-lookup"><span data-stu-id="416e6-107">PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W</span></span>  <br/> |
|<span data-ttu-id="416e6-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="416e6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="416e6-109">0x370D</span><span class="sxs-lookup"><span data-stu-id="416e6-109">0x370D</span></span>  <br/> |
|<span data-ttu-id="416e6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="416e6-110">Data type:</span></span>  <br/> |<span data-ttu-id="416e6-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="416e6-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="416e6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="416e6-112">Area:</span></span>  <br/> |<span data-ttu-id="416e6-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="416e6-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="416e6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="416e6-114">Remarks</span></span>

<span data-ttu-id="416e6-115">Diese Eigenschaften sind anwendbar, wenn Sie einen der Werte der **PR_ATTACH_METHOD** ([pidtagattachmethod (](pidtagattachmethod-canonical-property.md))-Eigenschaft verwenden, die die Anlage anhand des Verweises anzeigen: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**oder **ATTACH_BY _REF_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="416e6-115">These properties are applicable when you use any of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property's values that indicate attachment by reference: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, or **ATTACH_BY_REF_ONLY**.</span></span> <span data-ttu-id="416e6-116">Plattformen, die lange Dateinamen unterstützen, sollten sowohl **PR_ATTACH_LONG_PATHNAME** -als auch zugehörige Eigenschaften und **PR_ATTACH_PATHNAME** ([pidtagattachpathname (](pidtagattachpathname-canonical-property.md))-Eigenschaften beim Senden festlegen und PR_ATTACH_LONG_PATHNAME überprüfen. \*\* \*\*oder zugeordnete Eigenschaften beim Empfang.</span><span class="sxs-lookup"><span data-stu-id="416e6-116">Platforms that support long filenames should set both **PR_ATTACH_LONG_PATHNAME** or associated properties and **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) properties when sending, and should check **PR_ATTACH_LONG_PATHNAME** or associated properties first when receiving.</span></span> 
  
<span data-ttu-id="416e6-117">Die Clientanwendung sollte diese Eigenschaften auf einen vorgeschlagenen Long-Pfad und Dateinamen festlegen, die verwendet werden sollen, wenn der Hostcomputer, der eine Nachricht empfängt, lange filenames unterstützt.</span><span class="sxs-lookup"><span data-stu-id="416e6-117">The client application should set these properties to a suggested long path and filename to be used if the host machine receiving a message supports long filenames.</span></span> <span data-ttu-id="416e6-118">Durch Festlegen dieser Eigenschaften wird angegeben, dass die Anlagendaten nicht in der Nachricht enthalten sind, aber auf einem gemeinsamen Dateiserver verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="416e6-118">Setting these properties indicates that the attachment data is not included with the message but is available on a common file server.</span></span> 
  
<span data-ttu-id="416e6-119">Im Gegensatz zu den von **PR_ATTACH_PATHNAME**bereitgestellten Verzeichnissen und Dateinamen sind diese Verzeichnisse und filenames nicht auf ein Verzeichnis oder einen filename mit acht Zeichen und eine Erweiterung mit drei Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="416e6-119">Unlike the directories and filenames provided by **PR_ATTACH_PATHNAME**, these directories and filenames are not restricted to an eight-character directory or filename plus three-character extension.</span></span> <span data-ttu-id="416e6-120">Stattdessen kann jedes Verzeichnis oder jeder Dateiname bis zu 256 Zeichen lang sein, einschließlich des Namens, der Erweiterung und des Trenn Zeitraums.</span><span class="sxs-lookup"><span data-stu-id="416e6-120">Instead, each directory or filename can be up to 256 characters long, including the name, extension, and separator period.</span></span> <span data-ttu-id="416e6-121">Der Gesamt Pfad ist jedoch auf 256 Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="416e6-121">However, the overall path is limited to 256 characters.</span></span> 
  
<span data-ttu-id="416e6-122">Clients sollten in den meisten Fällen eine Universal Naming Convention (UNC) verwenden, wenn die Datei freigegeben ist, und einen absoluten Pfad verwenden, wenn die Datei lokal ist.</span><span class="sxs-lookup"><span data-stu-id="416e6-122">Clients should use a universal naming convention (UNC) in most cases when the file is shared, and should use an absolute path when the file is local.</span></span>
  
<span data-ttu-id="416e6-123">MAPI kann nur mit Pfaden und Dateinamen im ANSI-Zeichensatz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="416e6-123">MAPI works only with paths and filenames in the ANSI character set.</span></span> <span data-ttu-id="416e6-124">Client Anwendungen, die Pfade und Dateinamen in einem OEM-Zeichensatz verwenden, müssen Sie vor dem Aufrufen von MAPI in ANSI konvertieren.</span><span class="sxs-lookup"><span data-stu-id="416e6-124">Client applications that use paths and filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="416e6-125">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="416e6-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="416e6-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="416e6-126">Protocol specifications</span></span>

<span data-ttu-id="416e6-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="416e6-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="416e6-128">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="416e6-128">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="416e6-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="416e6-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="416e6-130">Gibt die Eigenschaften von Nachrichten mit verwalteten Rechten an.</span><span class="sxs-lookup"><span data-stu-id="416e6-130">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="416e6-131">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="416e6-131">Header files</span></span>

<span data-ttu-id="416e6-132">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="416e6-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="416e6-133">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="416e6-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="416e6-134">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="416e6-134">Mapitags.h</span></span>
  
> <span data-ttu-id="416e6-135">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="416e6-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="416e6-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="416e6-136">See also</span></span>



[<span data-ttu-id="416e6-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="416e6-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="416e6-138">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="416e6-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="416e6-139">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="416e6-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="416e6-140">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="416e6-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

