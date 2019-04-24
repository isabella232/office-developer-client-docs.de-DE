---
title: Kanonische Pidtagservicedeletefiles (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: da01385f83d9af9ad02eeb2fed08e3bc22d4df84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336400"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a><span data-ttu-id="cc8d5-103">Kanonische Pidtagservicedeletefiles (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cc8d5-103">PidTagServiceDeleteFiles Canonical Property</span></span>

  
  
<span data-ttu-id="cc8d5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc8d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc8d5-105">Enthält eine Liste von Dateinamen, die gelöscht werden sollen, wenn der Nachrichtendienst deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-105">Contains a list of filenames that are to be deleted when the message service is uninstalled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cc8d5-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="cc8d5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cc8d5-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span><span class="sxs-lookup"><span data-stu-id="cc8d5-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span></span>  <br/> |
|<span data-ttu-id="cc8d5-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="cc8d5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cc8d5-109">0x3D10</span><span class="sxs-lookup"><span data-stu-id="cc8d5-109">0x3D10</span></span>  <br/> |
|<span data-ttu-id="cc8d5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="cc8d5-110">Data type:</span></span>  <br/> |<span data-ttu-id="cc8d5-111">PT_MV_STRING8, PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cc8d5-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="cc8d5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="cc8d5-112">Area:</span></span>  <br/> |<span data-ttu-id="cc8d5-113">MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="cc8d5-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc8d5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc8d5-114">Remarks</span></span>

<span data-ttu-id="cc8d5-115">Die Dateinamen in der Liste, die in diesen Eigenschaften enthalten sind, werden auf dem Computer gelöscht, wenn der Nachrichtendienst mithilfe der Systemsteuerung deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-115">The filenames in the list contained in these properties are deleted from the computer when using the control panel to uninstall the message service.</span></span> <span data-ttu-id="cc8d5-116">Fügen Sie nicht in die Liste eine DLL ein, die mehrere Nachrichtendienste unterstützt, oder weitere Nachrichtendienste können versehentlich entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-116">Do not include in the list any DLL that supports multiple message services, or additional message services could be inadvertently removed.</span></span>
  
<span data-ttu-id="cc8d5-117">MAPI kann nur mit Dateinamen und anderen Zeichenfolgen im ANSI-Zeichensatz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-117">MAPI works only with filenames, and other strings passed to it, in the ANSI character set.</span></span> <span data-ttu-id="cc8d5-118">Anwendungen, die Dateinamen in einem OEM-Zeichensatz verwenden, müssen Sie vor dem Aufrufen von MAPI in ANSI konvertieren.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-118">Applications that use filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cc8d5-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cc8d5-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="cc8d5-120">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="cc8d5-120">Header files</span></span>

<span data-ttu-id="cc8d5-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="cc8d5-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="cc8d5-122">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="cc8d5-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="cc8d5-123">Mapitags.h</span></span>
  
> <span data-ttu-id="cc8d5-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cc8d5-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc8d5-125">See also</span></span>



[<span data-ttu-id="cc8d5-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cc8d5-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cc8d5-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cc8d5-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cc8d5-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="cc8d5-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cc8d5-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="cc8d5-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

