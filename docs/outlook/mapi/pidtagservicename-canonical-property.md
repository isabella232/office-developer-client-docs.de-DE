---
title: PidTagServiceName (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceName
api_type:
- COM
ms.assetid: 9a63d647-7504-42fc-b317-6b02b89070eb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 260a35af11b76b1867c693723c1a7fa8133082fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795159"
---
# <a name="pidtagservicename-canonical-property"></a><span data-ttu-id="48703-103">PidTagServiceName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="48703-103">PidTagServiceName Canonical Property</span></span>

  
  
<span data-ttu-id="48703-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="48703-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="48703-105">Enthält den Namen eines Diensts Nachricht als vom Benutzer in der Datei "MapiSvc.inf" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="48703-105">Contains the name of a message service as set by the user in the MapiSvc.inf file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="48703-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="48703-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="48703-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span><span class="sxs-lookup"><span data-stu-id="48703-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="48703-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="48703-108">Identifier:</span></span>  <br/> |<span data-ttu-id="48703-109">0x3D09</span><span class="sxs-lookup"><span data-stu-id="48703-109">0x3D09</span></span>  <br/> |
|<span data-ttu-id="48703-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="48703-110">Data type:</span></span>  <br/> |<span data-ttu-id="48703-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="48703-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="48703-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="48703-112">Area:</span></span>  <br/> |<span data-ttu-id="48703-113">MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="48703-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48703-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48703-114">Remarks</span></span>

<span data-ttu-id="48703-115">Der Name dieser Eigenschaften enthalten ist speziell für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="48703-115">The name contained in these properties is specific to the message service.</span></span> <span data-ttu-id="48703-116">Es geht in MapiSvc.inf aktivieren Sie im Abschnitt [Services].</span><span class="sxs-lookup"><span data-stu-id="48703-116">It comes from the [Services] section in MapiSvc.inf.</span></span>
  
<span data-ttu-id="48703-117">Diese Eigenschaften werden als eine Spalte in der Tabelle der Dienste angezeigt und können verwendet werden, um die Dienste zu filtern.</span><span class="sxs-lookup"><span data-stu-id="48703-117">These properties appear as a column in the message service table and can be used to filter services.</span></span> <span data-ttu-id="48703-118">Da es zu identifizieren und Filtern von Services verwendet wird, sollte der Wert nicht lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="48703-118">Because it is used to identify and filter services, the value should not be localized.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="48703-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="48703-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="48703-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="48703-120">Header files</span></span>

<span data-ttu-id="48703-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="48703-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="48703-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="48703-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="48703-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="48703-123">Mapitags.h</span></span>
  
> <span data-ttu-id="48703-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="48703-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="48703-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48703-125">See also</span></span>



[<span data-ttu-id="48703-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="48703-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="48703-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="48703-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="48703-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="48703-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="48703-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="48703-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

