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
ms.openlocfilehash: 236349a6b53eeb2f5c18c841c05cfb80a3fce824
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580222"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a><span data-ttu-id="43473-103">PidTagServiceDeleteFiles (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="43473-103">PidTagServiceDeleteFiles Canonical Property</span></span>

  
  
<span data-ttu-id="43473-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43473-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43473-105">Enthält eine Liste der Dateinamen, die bei der Deinstallation von Message-Dienst gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="43473-105">Contains a list of filenames that are to be deleted when the message service is uninstalled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43473-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="43473-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="43473-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span><span class="sxs-lookup"><span data-stu-id="43473-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span></span>  <br/> |
|<span data-ttu-id="43473-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="43473-108">Identifier:</span></span>  <br/> |<span data-ttu-id="43473-109">0x3D10</span><span class="sxs-lookup"><span data-stu-id="43473-109">0x3D10</span></span>  <br/> |
|<span data-ttu-id="43473-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="43473-110">Data type:</span></span>  <br/> |<span data-ttu-id="43473-111">PT_MV_STRING8 PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="43473-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="43473-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="43473-112">Area:</span></span>  <br/> |<span data-ttu-id="43473-113">MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="43473-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43473-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="43473-114">Remarks</span></span>

<span data-ttu-id="43473-115">Die Dateinamen in der Liste in diese Eigenschaften werden vom Computer gelöscht, wenn die Systemsteuerung verwenden, um den Dienst zu deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="43473-115">The filenames in the list contained in these properties are deleted from the computer when using the control panel to uninstall the message service.</span></span> <span data-ttu-id="43473-116">Schließen Sie nicht in der Liste eine DLL, die mehrere Nachrichtendienste für die unterstützt oder zusätzliche Message Dienste konnte versehentlich entfernt.</span><span class="sxs-lookup"><span data-stu-id="43473-116">Do not include in the list any DLL that supports multiple message services, or additional message services could be inadvertently removed.</span></span>
  
<span data-ttu-id="43473-117">MAPI funktioniert nur mit Dateinamen und andere Zeichenfolgen übergeben wurden, im ANSI-Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="43473-117">MAPI works only with filenames, and other strings passed to it, in the ANSI character set.</span></span> <span data-ttu-id="43473-118">Anwendungen, die in einem OEM-Zeichensatz Dateinamen verwenden, müssen diese in ANSI konvertieren, vor dem Aufruf von MAPI.</span><span class="sxs-lookup"><span data-stu-id="43473-118">Applications that use filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="43473-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="43473-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="43473-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="43473-120">Header files</span></span>

<span data-ttu-id="43473-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="43473-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="43473-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="43473-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="43473-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="43473-123">Mapitags.h</span></span>
  
> <span data-ttu-id="43473-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="43473-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43473-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43473-125">See also</span></span>



[<span data-ttu-id="43473-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="43473-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="43473-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="43473-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="43473-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="43473-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="43473-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="43473-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

