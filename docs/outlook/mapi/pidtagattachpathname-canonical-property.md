---
title: Kanonische Pidtagattachpathname (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 05df7fe04f511de9310edc7a8ef09130e6354ad2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327230"
---
# <a name="pidtagattachpathname-canonical-property"></a><span data-ttu-id="b58f6-103">Kanonische Pidtagattachpathname (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b58f6-103">PidTagAttachPathname Canonical Property</span></span>

  
  
<span data-ttu-id="b58f6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b58f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b58f6-105">Enthält den vollqualifizierten Pfad und Dateinamen einer Anlage.</span><span class="sxs-lookup"><span data-stu-id="b58f6-105">Contains an attachment's fully-qualified path and filename.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b58f6-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b58f6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b58f6-107">PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A, PR_ATTACH_PATHNAME_W</span><span class="sxs-lookup"><span data-stu-id="b58f6-107">PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A, PR_ATTACH_PATHNAME_W</span></span>  <br/> |
|<span data-ttu-id="b58f6-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b58f6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b58f6-109">0x3708</span><span class="sxs-lookup"><span data-stu-id="b58f6-109">0x3708</span></span>  <br/> |
|<span data-ttu-id="b58f6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b58f6-110">Data type:</span></span>  <br/> |<span data-ttu-id="b58f6-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b58f6-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b58f6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b58f6-112">Area:</span></span>  <br/> |<span data-ttu-id="b58f6-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="b58f6-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b58f6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b58f6-114">Remarks</span></span>

<span data-ttu-id="b58f6-115">Es wird empfohlen, dass Attachment-unter Objekte diese Eigenschaften verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="b58f6-115">It is recommended that attachment subobjects expose these properties.</span></span> <span data-ttu-id="b58f6-116">Diese Einstellung gibt an, dass die Anlagendaten nicht in der Nachricht enthalten sind, aber auf einem gemeinsamen Dateiserver verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b58f6-116">Setting them indicates that the attachment data is not included with the message but is available on a common file server.</span></span> <span data-ttu-id="b58f6-117">Diese Eigenschaften sind in Verbindung mit einem der **PR_ATTACH_METHOD** ([pidtagattachmethod (](pidtagattachmethod-canonical-property.md))-Flags erforderlich, die die Anlage anhand des Verweises anzeigen: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**oder **ATTACH_BY_REF_ NUR**.</span><span class="sxs-lookup"><span data-stu-id="b58f6-117">These properties are required in conjunction with any of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) flags that indicate attachment by reference: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, or **ATTACH_BY_REF_ONLY**.</span></span> 
  
<span data-ttu-id="b58f6-118">Jedes Verzeichnis oder jeder Dateiname ist auf einen achtstelligen Namen und eine dreistellige Durchwahlnummer beschränkt.</span><span class="sxs-lookup"><span data-stu-id="b58f6-118">Each directory or filename is restricted to an eight-character name plus a three-character extension.</span></span> <span data-ttu-id="b58f6-119">Der Gesamt Pfad ist auf 256 Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="b58f6-119">The overall path is restricted to 256 characters.</span></span> <span data-ttu-id="b58f6-120">Legen Sie für eine Plattform, die lange Dateinamen unterstützt, sowohl diese Eigenschaften als auch **PR_ATTACH_LONG_PATHNAME** ([pidtagattachlongpathname (](pidtagattachlongpathname-canonical-property.md)) fest.</span><span class="sxs-lookup"><span data-stu-id="b58f6-120">For a platform that supports long filenames, set both these properties and **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)).</span></span> 
  
<span data-ttu-id="b58f6-121">Client Anwendungen sollten in den meisten Fällen eine UNC (Universal Naming Convention) verwenden, wenn die Datei freigegeben ist und einen absoluten Pfad verwenden sollte, wenn die Datei lokal ist.</span><span class="sxs-lookup"><span data-stu-id="b58f6-121">Client applications should use a universal naming convention (UNC) in most cases when the file is shared, and should use an absolute path when the file is local.</span></span>
  
<span data-ttu-id="b58f6-122">MAPI kann nur mit Pfaden und Dateinamen im ANSI-Zeichensatz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b58f6-122">MAPI works only with paths and filenames in the ANSI character set.</span></span> <span data-ttu-id="b58f6-123">Clients, die Pfade und Dateinamen in einem OEM-Zeichensatz verwenden, müssen Sie vor dem Aufrufen von MAPI in ANSI konvertieren.</span><span class="sxs-lookup"><span data-stu-id="b58f6-123">Clients that use paths and filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b58f6-124">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b58f6-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b58f6-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b58f6-125">Protocol specifications</span></span>

<span data-ttu-id="b58f6-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b58f6-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b58f6-127">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="b58f6-127">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="b58f6-128">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b58f6-128">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b58f6-129">Gibt die Eigenschaften von Nachrichten mit verwalteten Rechten an.</span><span class="sxs-lookup"><span data-stu-id="b58f6-129">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b58f6-130">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="b58f6-130">Header files</span></span>

<span data-ttu-id="b58f6-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b58f6-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="b58f6-132">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="b58f6-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="b58f6-133">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="b58f6-133">Mapitags.h</span></span>
  
> <span data-ttu-id="b58f6-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b58f6-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b58f6-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b58f6-135">See also</span></span>



[<span data-ttu-id="b58f6-136">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="b58f6-136">ScLocalPathFromUNC</span></span>](sclocalpathfromunc.md)
  
[<span data-ttu-id="b58f6-137">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="b58f6-137">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)


[<span data-ttu-id="b58f6-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b58f6-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b58f6-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b58f6-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b58f6-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b58f6-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b58f6-141">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b58f6-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

