---
title: Kanonische Pidtagservicename (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e5659113b1c6579913042ae0c8dfcd03e9802621
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359479"
---
# <a name="pidtagservicename-canonical-property"></a><span data-ttu-id="4e015-103">Kanonische Pidtagservicename (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4e015-103">PidTagServiceName Canonical Property</span></span>

  
  
<span data-ttu-id="4e015-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e015-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e015-105">Enthält den Namen eines Nachrichtendiensts, der vom Benutzer in der Datei MapiSvc. inf festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="4e015-105">Contains the name of a message service as set by the user in the MapiSvc.inf file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4e015-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4e015-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4e015-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span><span class="sxs-lookup"><span data-stu-id="4e015-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="4e015-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="4e015-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4e015-109">0x3D09</span><span class="sxs-lookup"><span data-stu-id="4e015-109">0x3D09</span></span>  <br/> |
|<span data-ttu-id="4e015-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4e015-110">Data type:</span></span>  <br/> |<span data-ttu-id="4e015-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4e015-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4e015-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4e015-112">Area:</span></span>  <br/> |<span data-ttu-id="4e015-113">MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="4e015-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e015-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e015-114">Remarks</span></span>

<span data-ttu-id="4e015-115">Der Name, der in diesen Eigenschaften enthalten ist, ist für den Nachrichtendienst spezifisch.</span><span class="sxs-lookup"><span data-stu-id="4e015-115">The name contained in these properties is specific to the message service.</span></span> <span data-ttu-id="4e015-116">Sie stammt aus dem Abschnitt [Services] in MapiSvc. inf.</span><span class="sxs-lookup"><span data-stu-id="4e015-116">It comes from the [Services] section in MapiSvc.inf.</span></span>
  
<span data-ttu-id="4e015-117">Diese Eigenschaften werden als Spalte in der Nachrichtendienst Tabelle angezeigt und können zum Filtern von Diensten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e015-117">These properties appear as a column in the message service table and can be used to filter services.</span></span> <span data-ttu-id="4e015-118">Da Sie zum Identifizieren und Filtern von Diensten verwendet wird, sollte der Wert nicht lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="4e015-118">Because it is used to identify and filter services, the value should not be localized.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4e015-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4e015-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4e015-120">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="4e015-120">Header files</span></span>

<span data-ttu-id="4e015-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4e015-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="4e015-122">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="4e015-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="4e015-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="4e015-123">Mapitags.h</span></span>
  
> <span data-ttu-id="4e015-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="4e015-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4e015-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e015-125">See also</span></span>



[<span data-ttu-id="4e015-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4e015-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4e015-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4e015-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4e015-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4e015-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4e015-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4e015-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

