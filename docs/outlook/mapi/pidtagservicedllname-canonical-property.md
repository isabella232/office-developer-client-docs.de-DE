---
title: PidTagServiceDllName (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d2917f2119fde38686397b65956113bc430b2e31
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570814"
---
# <a name="pidtagservicedllname-canonical-property"></a><span data-ttu-id="9c86b-103">PidTagServiceDllName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9c86b-103">PidTagServiceDllName Canonical Property</span></span>

  
  
<span data-ttu-id="9c86b-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c86b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c86b-105">Enthält den Dateinamen der DLL Nachricht Service Provider Entry Point-Funktion, die für die Konfiguration aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9c86b-105">Contains the filename of the DLL containing the message service provider entry point function to call for configuration.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9c86b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9c86b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9c86b-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="9c86b-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="9c86b-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="9c86b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9c86b-109">0x3D0A</span><span class="sxs-lookup"><span data-stu-id="9c86b-109">0x3D0A</span></span>  <br/> |
|<span data-ttu-id="9c86b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9c86b-110">Data type:</span></span>  <br/> |<span data-ttu-id="9c86b-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9c86b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9c86b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9c86b-112">Area:</span></span>  <br/> |<span data-ttu-id="9c86b-113">MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="9c86b-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9c86b-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="9c86b-114">Remarks</span></span>

<span data-ttu-id="9c86b-115">Wenn der Eintrag Punkt Funktionsname in der Methode **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) angezeigt wird, bedeutet dies, dass der Einstiegspunkt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9c86b-115">When the entry point function name appears in the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) method, it indicates that the entry point exists.</span></span>
  
<span data-ttu-id="9c86b-116">MAPI verwendet eine DLL-Datei Namenskonvention fest.</span><span class="sxs-lookup"><span data-stu-id="9c86b-116">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="9c86b-117">Die Basis Dateiname enthält maximal sechs Zeichen, die die DLL eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9c86b-117">The base filename contains up to six characters that uniquely identify the DLL.</span></span> <span data-ttu-id="9c86b-118">MAPI fügt die Zeichenfolge 32 an den Basisnamen der DLL-Datei zum Ermitteln der Version, die auf 32-Bit-Plattformen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9c86b-118">MAPI appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="9c86b-119">Beispielsweise, wenn der Name MAPI. DLL-Datei angegeben wird, MAPI erstellt den Namen MAPI32. DLL, um die entsprechenden 32-Bit-Version der DLL darstellen.</span><span class="sxs-lookup"><span data-stu-id="9c86b-119">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="9c86b-120">Diese Eigenschaften sollten den Basisnamen angeben.</span><span class="sxs-lookup"><span data-stu-id="9c86b-120">These properties should specify the base name.</span></span> <span data-ttu-id="9c86b-121">MAPI fügt die Zeichenfolge 32 entsprechend an.</span><span class="sxs-lookup"><span data-stu-id="9c86b-121">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="9c86b-122">Einschließlich der Zeichenfolge 32 im Rahmen dieser Eigenschaften führt zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="9c86b-122">Including the string 32 as part of these properties result in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9c86b-123">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9c86b-123">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9c86b-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="9c86b-124">Header files</span></span>

<span data-ttu-id="9c86b-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9c86b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="9c86b-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9c86b-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="9c86b-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9c86b-127">Mapitags.h</span></span>
  
> <span data-ttu-id="9c86b-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9c86b-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9c86b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c86b-129">See also</span></span>



[<span data-ttu-id="9c86b-130">PidTagProviderDllName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9c86b-130">PidTagProviderDllName Canonical Property</span></span>](pidtagproviderdllname-canonical-property.md)


[<span data-ttu-id="9c86b-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9c86b-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9c86b-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9c86b-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9c86b-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9c86b-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9c86b-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9c86b-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

