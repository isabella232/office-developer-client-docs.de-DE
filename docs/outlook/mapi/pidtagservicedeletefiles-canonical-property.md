---
title: PidTagServiceDeleteFiles (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDeleteFiles
api_type:
- COM
ms.assetid: 9ec80a93-9e8f-46be-a1d4-7648aae47fec
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8f90d72e842df62c19c5aeeaf6c398c5db469560
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795167"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a><span data-ttu-id="74954-103">PidTagServiceDeleteFiles (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="74954-103">PidTagServiceDeleteFiles Canonical Property</span></span>

  
  
<span data-ttu-id="74954-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="74954-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="74954-105">Enthält eine Liste der Dateinamen, die bei der Deinstallation von Message-Dienst gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="74954-105">Contains a list of filenames that are to be deleted when the message service is uninstalled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="74954-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="74954-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="74954-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span><span class="sxs-lookup"><span data-stu-id="74954-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span></span>  <br/> |
|<span data-ttu-id="74954-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="74954-108">Identifier:</span></span>  <br/> |<span data-ttu-id="74954-109">0x3D10</span><span class="sxs-lookup"><span data-stu-id="74954-109">0x3D10</span></span>  <br/> |
|<span data-ttu-id="74954-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="74954-110">Data type:</span></span>  <br/> |<span data-ttu-id="74954-111">PT_MV_STRING8 PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="74954-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="74954-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="74954-112">Area:</span></span>  <br/> |<span data-ttu-id="74954-113">MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="74954-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74954-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74954-114">Remarks</span></span>

<span data-ttu-id="74954-115">Die Dateinamen in der Liste in diese Eigenschaften werden vom Computer gelöscht, wenn die Systemsteuerung verwenden, um den Dienst zu deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="74954-115">The filenames in the list contained in these properties are deleted from the computer when using the control panel to uninstall the message service.</span></span> <span data-ttu-id="74954-116">Schließen Sie nicht in der Liste eine DLL, die mehrere Nachrichtendienste für die unterstützt oder zusätzliche Message Dienste konnte versehentlich entfernt.</span><span class="sxs-lookup"><span data-stu-id="74954-116">Do not include in the list any DLL that supports multiple message services, or additional message services could be inadvertently removed.</span></span>
  
<span data-ttu-id="74954-117">MAPI funktioniert nur mit Dateinamen und andere Zeichenfolgen übergeben wurden, im ANSI-Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="74954-117">MAPI works only with filenames, and other strings passed to it, in the ANSI character set.</span></span> <span data-ttu-id="74954-118">Anwendungen, die in einem OEM-Zeichensatz Dateinamen verwenden, müssen diese in ANSI konvertieren, vor dem Aufruf von MAPI.</span><span class="sxs-lookup"><span data-stu-id="74954-118">Applications that use filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="74954-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="74954-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="74954-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="74954-120">Header files</span></span>

<span data-ttu-id="74954-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="74954-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="74954-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="74954-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="74954-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="74954-123">Mapitags.h</span></span>
  
> <span data-ttu-id="74954-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="74954-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="74954-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74954-125">See also</span></span>



[<span data-ttu-id="74954-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="74954-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="74954-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="74954-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="74954-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="74954-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="74954-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="74954-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

