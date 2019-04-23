---
title: Kanonische Pidtagservicedllname (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDllName
api_type:
- COM
ms.assetid: a651af84-1711-449e-ba7e-5ce09cafa02b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: adf24bcd02d7efc303f911ee01a64325150339ce
ms.sourcegitcommit: 18f3d9462048859fe040e12136ff66f19066764b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2019
ms.locfileid: "31980454"
---
# <a name="pidtagservicedllname-canonical-property"></a><span data-ttu-id="b2f53-103">Kanonische Pidtagservicedllname (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b2f53-103">PidTagServiceDllName Canonical Property</span></span>

  
  
<span data-ttu-id="b2f53-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2f53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2f53-105">Enthält den Dateinamen der DLL mit der Einstiegspunktfunktion des Nachrichtendienst Anbieters, die für die Konfiguration aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2f53-105">Contains the filename of the DLL containing the message service provider entry point function to call for configuration.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b2f53-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b2f53-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b2f53-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="b2f53-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="b2f53-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b2f53-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b2f53-109">0x3D0A</span><span class="sxs-lookup"><span data-stu-id="b2f53-109">0x3D0A</span></span>  <br/> |
|<span data-ttu-id="b2f53-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b2f53-110">Data type:</span></span>  <br/> |<span data-ttu-id="b2f53-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b2f53-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b2f53-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b2f53-112">Area:</span></span>  <br/> |<span data-ttu-id="b2f53-113">MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="b2f53-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b2f53-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2f53-114">Remarks</span></span>

<span data-ttu-id="b2f53-115">Wenn der Name der Einstiegspunktfunktion in der **PR_SERVICE_ENTRY_NAME** ([pidtagserviceentryname (](pidtagserviceentryname-canonical-property.md))-Methode angezeigt wird, gibt er an, dass der Einstiegspunkt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b2f53-115">When the entry point function name appears in the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) method, it indicates that the entry point exists.</span></span>
  
<span data-ttu-id="b2f53-116">MAPI verwendet eine Benennungskonvention für DLL-Dateien.</span><span class="sxs-lookup"><span data-stu-id="b2f53-116">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="b2f53-117">Sie fügt die Zeichenfolge 32 an den Basis-DLL-Namen an, um die Version zu identifizieren, die auf 32-Bit-Plattformen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2f53-117">It appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="b2f53-118">Wenn beispielsweise der Name "MAPI" lautet. DLL angegeben ist, erstellt MAPI den Namen MAPI32. DLL zur Darstellung der entsprechenden 32-Bit-Version der DLL.</span><span class="sxs-lookup"><span data-stu-id="b2f53-118">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="b2f53-119">Diese Eigenschaften sollten den Basisnamen angeben.</span><span class="sxs-lookup"><span data-stu-id="b2f53-119">These properties should specify the base name.</span></span> <span data-ttu-id="b2f53-120">MAPI fügt die Zeichenfolge 32 entsprechend an.</span><span class="sxs-lookup"><span data-stu-id="b2f53-120">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="b2f53-121">Das Einschließen der Zeichenfolge 32 als Teil dieser Eigenschaften führt zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="b2f53-121">Including the string 32 as part of these properties result in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b2f53-122">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b2f53-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b2f53-123">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="b2f53-123">Header files</span></span>

<span data-ttu-id="b2f53-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b2f53-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="b2f53-125">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="b2f53-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="b2f53-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="b2f53-126">Mapitags.h</span></span>
  
> <span data-ttu-id="b2f53-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b2f53-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b2f53-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2f53-128">See also</span></span>



[<span data-ttu-id="b2f53-129">Kanonische Pidtagproviderdllname (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b2f53-129">PidTagProviderDllName Canonical Property</span></span>](pidtagproviderdllname-canonical-property.md)


[<span data-ttu-id="b2f53-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2f53-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b2f53-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2f53-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b2f53-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b2f53-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b2f53-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b2f53-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

