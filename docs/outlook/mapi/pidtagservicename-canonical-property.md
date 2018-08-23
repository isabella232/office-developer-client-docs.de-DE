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
ms.openlocfilehash: d950ee21c0c4c41e84c0fe1f8104219e63f84cec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592675"
---
# <a name="pidtagservicename-canonical-property"></a><span data-ttu-id="15069-103">PidTagServiceName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="15069-103">PidTagServiceName Canonical Property</span></span>

  
  
<span data-ttu-id="15069-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15069-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15069-105">Enthält den Namen eines Diensts Nachricht als vom Benutzer in der Datei "MapiSvc.inf" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="15069-105">Contains the name of a message service as set by the user in the MapiSvc.inf file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="15069-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="15069-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="15069-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span><span class="sxs-lookup"><span data-stu-id="15069-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="15069-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="15069-108">Identifier:</span></span>  <br/> |<span data-ttu-id="15069-109">0x3D09</span><span class="sxs-lookup"><span data-stu-id="15069-109">0x3D09</span></span>  <br/> |
|<span data-ttu-id="15069-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="15069-110">Data type:</span></span>  <br/> |<span data-ttu-id="15069-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="15069-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="15069-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="15069-112">Area:</span></span>  <br/> |<span data-ttu-id="15069-113">MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="15069-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15069-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="15069-114">Remarks</span></span>

<span data-ttu-id="15069-115">Der Name dieser Eigenschaften enthalten ist speziell für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="15069-115">The name contained in these properties is specific to the message service.</span></span> <span data-ttu-id="15069-116">Es geht in MapiSvc.inf aktivieren Sie im Abschnitt [Services].</span><span class="sxs-lookup"><span data-stu-id="15069-116">It comes from the [Services] section in MapiSvc.inf.</span></span>
  
<span data-ttu-id="15069-117">Diese Eigenschaften werden als eine Spalte in der Tabelle der Dienste angezeigt und können verwendet werden, um die Dienste zu filtern.</span><span class="sxs-lookup"><span data-stu-id="15069-117">These properties appear as a column in the message service table and can be used to filter services.</span></span> <span data-ttu-id="15069-118">Da es zu identifizieren und Filtern von Services verwendet wird, sollte der Wert nicht lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="15069-118">Because it is used to identify and filter services, the value should not be localized.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="15069-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="15069-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="15069-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="15069-120">Header files</span></span>

<span data-ttu-id="15069-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="15069-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="15069-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="15069-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="15069-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="15069-123">Mapitags.h</span></span>
  
> <span data-ttu-id="15069-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="15069-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="15069-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15069-125">See also</span></span>



[<span data-ttu-id="15069-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="15069-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="15069-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="15069-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="15069-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="15069-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="15069-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="15069-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

