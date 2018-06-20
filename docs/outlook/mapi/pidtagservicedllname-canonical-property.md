---
title: Kanonische PidTagServiceDllName-Eigenschaft
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
ms.openlocfilehash: 54fe624c98ddb631326853f387372468a61b2f70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795158"
---
# <a name="pidtagservicedllname-canonical-property"></a><span data-ttu-id="bffc5-103">Kanonische PidTagServiceDllName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bffc5-103">PidTagServiceDllName Canonical Property</span></span>

  
  
<span data-ttu-id="bffc5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bffc5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bffc5-105">Enthält den Dateinamen der DLL Nachricht Service Provider Entry Point-Funktion, die für die Konfiguration aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bffc5-105">Contains the filename of the DLL containing the message service provider entry point function to call for configuration.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bffc5-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bffc5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bffc5-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="bffc5-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="bffc5-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="bffc5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bffc5-109">0x3D0A</span><span class="sxs-lookup"><span data-stu-id="bffc5-109">0x3D0A</span></span>  <br/> |
|<span data-ttu-id="bffc5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bffc5-110">Data type:</span></span>  <br/> |<span data-ttu-id="bffc5-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bffc5-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bffc5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bffc5-112">Area:</span></span>  <br/> |<span data-ttu-id="bffc5-113">MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="bffc5-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bffc5-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bffc5-114">Remarks</span></span>

<span data-ttu-id="bffc5-115">Wenn der Eintrag Punkt Funktionsname in der Methode **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) angezeigt wird, bedeutet dies, dass der Einstiegspunkt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="bffc5-115">When the entry point function name appears in the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) method, it indicates that the entry point exists.</span></span>
  
<span data-ttu-id="bffc5-116">MAPI verwendet eine DLL-Datei Namenskonvention fest.</span><span class="sxs-lookup"><span data-stu-id="bffc5-116">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="bffc5-117">Die Basis Dateiname enthält maximal sechs Zeichen, die die DLL eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bffc5-117">The base filename contains up to six characters that uniquely identify the DLL.</span></span> <span data-ttu-id="bffc5-118">MAPI fügt die Zeichenfolge 32 an den Basisnamen der DLL-Datei zum Ermitteln der Version, die auf 32-Bit-Plattformen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bffc5-118">MAPI appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="bffc5-119">Beispielsweise, wenn der Name MAPI. DLL-Datei angegeben wird, MAPI erstellt den Namen MAPI32. DLL, um die entsprechenden 32-Bit-Version der DLL darstellen.</span><span class="sxs-lookup"><span data-stu-id="bffc5-119">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="bffc5-120">Diese Eigenschaften sollten den Basisnamen angeben.</span><span class="sxs-lookup"><span data-stu-id="bffc5-120">These properties should specify the base name.</span></span> <span data-ttu-id="bffc5-121">MAPI fügt die Zeichenfolge 32 entsprechend an.</span><span class="sxs-lookup"><span data-stu-id="bffc5-121">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="bffc5-122">Einschließlich der Zeichenfolge 32 im Rahmen dieser Eigenschaften führt zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="bffc5-122">Including the string 32 as part of these properties result in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bffc5-123">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bffc5-123">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bffc5-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="bffc5-124">Header files</span></span>

<span data-ttu-id="bffc5-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bffc5-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="bffc5-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="bffc5-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="bffc5-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bffc5-127">Mapitags.h</span></span>
  
> <span data-ttu-id="bffc5-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="bffc5-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bffc5-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bffc5-129">See also</span></span>



[<span data-ttu-id="bffc5-130">Kanonische PidTagProviderDllName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bffc5-130">PidTagProviderDllName Canonical Property</span></span>](pidtagproviderdllname-canonical-property.md)


[<span data-ttu-id="bffc5-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bffc5-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bffc5-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bffc5-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bffc5-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bffc5-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bffc5-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bffc5-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

