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
ms.openlocfilehash: adf24bcd02d7efc303f911ee01a64325150339ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330065"
---
# <a name="pidtagservicedllname-canonical-property"></a><span data-ttu-id="89acf-103">PidTagServiceDllName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="89acf-103">PidTagServiceDllName Canonical Property</span></span>

  
  
<span data-ttu-id="89acf-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89acf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89acf-105">Enthält den Dateinamen der DLL, die die Einstiegspunktfunktion des Nachrichtendienstanbieters zum Aufrufen der Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="89acf-105">Contains the filename of the DLL containing the message service provider entry point function to call for configuration.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="89acf-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="89acf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="89acf-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="89acf-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="89acf-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="89acf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="89acf-109">0x3D0A</span><span class="sxs-lookup"><span data-stu-id="89acf-109">0x3D0A</span></span>  <br/> |
|<span data-ttu-id="89acf-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="89acf-110">Data type:</span></span>  <br/> |<span data-ttu-id="89acf-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="89acf-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="89acf-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="89acf-112">Area:</span></span>  <br/> |<span data-ttu-id="89acf-113">MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="89acf-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89acf-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="89acf-114">Remarks</span></span>

<span data-ttu-id="89acf-115">Wenn der Name der Einstiegspunktfunktion in der **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) -Methode angezeigt wird, gibt er an, dass der Einstiegspunkt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="89acf-115">When the entry point function name appears in the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) method, it indicates that the entry point exists.</span></span>
  
<span data-ttu-id="89acf-116">MAPI verwendet eine DLL-Dateibenennungskonvention.</span><span class="sxs-lookup"><span data-stu-id="89acf-116">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="89acf-117">Sie fügt die Zeichenfolge 32 an den Basis-DLL-Namen an, um die Version zu identifizieren, die auf 32-Bit-Plattformen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="89acf-117">It appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="89acf-118">Wenn beispielsweise der Name MAPI.DLL angegeben wird, erstellt MAPI den Namen MAPI32.DLL, um die entsprechende 32-Bit-Version der DLL zu repräsentieren.</span><span class="sxs-lookup"><span data-stu-id="89acf-118">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="89acf-119">Diese Eigenschaften sollten den Basisnamen angeben.</span><span class="sxs-lookup"><span data-stu-id="89acf-119">These properties should specify the base name.</span></span> <span data-ttu-id="89acf-120">MAPI fügt die Zeichenfolge 32 an.</span><span class="sxs-lookup"><span data-stu-id="89acf-120">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="89acf-121">Das Einschleingen der Zeichenfolge 32 als Teil dieser Eigenschaften führt zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="89acf-121">Including the string 32 as part of these properties result in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="89acf-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="89acf-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="89acf-123">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="89acf-123">Header files</span></span>

<span data-ttu-id="89acf-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="89acf-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="89acf-125">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="89acf-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="89acf-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="89acf-126">Mapitags.h</span></span>
  
> <span data-ttu-id="89acf-127">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="89acf-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="89acf-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89acf-128">See also</span></span>



[<span data-ttu-id="89acf-129">PidTagProviderDllName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="89acf-129">PidTagProviderDllName Canonical Property</span></span>](pidtagproviderdllname-canonical-property.md)


[<span data-ttu-id="89acf-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="89acf-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="89acf-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="89acf-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="89acf-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="89acf-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="89acf-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="89acf-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

