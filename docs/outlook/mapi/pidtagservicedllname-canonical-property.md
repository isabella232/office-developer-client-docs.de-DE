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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 54fe624c98ddb631326853f387372468a61b2f70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795158"
---
# <a name="pidtagservicedllname-canonical-property"></a><span data-ttu-id="90cef-103">PidTagServiceDllName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="90cef-103">PidTagServiceDllName Canonical Property</span></span>

  
  
<span data-ttu-id="90cef-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="90cef-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="90cef-105">Enthält den Dateinamen der DLL Nachricht Service Provider Entry Point-Funktion, die für die Konfiguration aufrufen.</span><span class="sxs-lookup"><span data-stu-id="90cef-105">Contains the filename of the DLL containing the message service provider entry point function to call for configuration.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="90cef-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="90cef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="90cef-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="90cef-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="90cef-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="90cef-108">Identifier:</span></span>  <br/> |<span data-ttu-id="90cef-109">0x3D0A</span><span class="sxs-lookup"><span data-stu-id="90cef-109">0x3D0A</span></span>  <br/> |
|<span data-ttu-id="90cef-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="90cef-110">Data type:</span></span>  <br/> |<span data-ttu-id="90cef-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="90cef-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="90cef-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="90cef-112">Area:</span></span>  <br/> |<span data-ttu-id="90cef-113">MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="90cef-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90cef-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90cef-114">Remarks</span></span>

<span data-ttu-id="90cef-115">Wenn der Eintrag Punkt Funktionsname in der Methode **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) angezeigt wird, bedeutet dies, dass der Einstiegspunkt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="90cef-115">When the entry point function name appears in the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) method, it indicates that the entry point exists.</span></span>
  
<span data-ttu-id="90cef-116">MAPI verwendet eine DLL-Datei Namenskonvention fest.</span><span class="sxs-lookup"><span data-stu-id="90cef-116">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="90cef-117">Die Basis Dateiname enthält maximal sechs Zeichen, die die DLL eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="90cef-117">The base filename contains up to six characters that uniquely identify the DLL.</span></span> <span data-ttu-id="90cef-118">MAPI fügt die Zeichenfolge 32 an den Basisnamen der DLL-Datei zum Ermitteln der Version, die auf 32-Bit-Plattformen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90cef-118">MAPI appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="90cef-119">Beispielsweise, wenn der Name MAPI. DLL-Datei angegeben wird, MAPI erstellt den Namen MAPI32. DLL, um die entsprechenden 32-Bit-Version der DLL darstellen.</span><span class="sxs-lookup"><span data-stu-id="90cef-119">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="90cef-120">Diese Eigenschaften sollten den Basisnamen angeben.</span><span class="sxs-lookup"><span data-stu-id="90cef-120">These properties should specify the base name.</span></span> <span data-ttu-id="90cef-121">MAPI fügt die Zeichenfolge 32 entsprechend an.</span><span class="sxs-lookup"><span data-stu-id="90cef-121">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="90cef-122">Einschließlich der Zeichenfolge 32 im Rahmen dieser Eigenschaften führt zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="90cef-122">Including the string 32 as part of these properties result in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="90cef-123">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="90cef-123">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="90cef-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="90cef-124">Header files</span></span>

<span data-ttu-id="90cef-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="90cef-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="90cef-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="90cef-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="90cef-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="90cef-127">Mapitags.h</span></span>
  
> <span data-ttu-id="90cef-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="90cef-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="90cef-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90cef-129">See also</span></span>



[<span data-ttu-id="90cef-130">PidTagProviderDllName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="90cef-130">PidTagProviderDllName Canonical Property</span></span>](pidtagproviderdllname-canonical-property.md)


[<span data-ttu-id="90cef-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="90cef-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="90cef-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="90cef-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="90cef-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="90cef-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="90cef-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="90cef-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

