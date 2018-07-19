---
title: PidTagProviderDllName (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderDllName
api_type:
- COM
ms.assetid: 9ddb38eb-9a32-4dbe-b42c-6ea9db98acd2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d75f22af3f8c9184da55ec57e08cf4db832ed174
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794834"
---
# <a name="pidtagproviderdllname-canonical-property"></a><span data-ttu-id="466ba-103">PidTagProviderDllName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="466ba-103">PidTagProviderDllName Canonical Property</span></span>

  
  
<span data-ttu-id="466ba-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="466ba-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="466ba-105">Der Name der Basisdatei von MAPI Service Provider Dynamic Link Library (DLL) enthält.</span><span class="sxs-lookup"><span data-stu-id="466ba-105">Contains the base file name of the MAPI service provider dynamic-link library (DLL).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="466ba-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="466ba-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="466ba-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="466ba-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="466ba-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="466ba-108">Identifier:</span></span>  <br/> |<span data-ttu-id="466ba-109">0x300A</span><span class="sxs-lookup"><span data-stu-id="466ba-109">0x300A</span></span>  <br/> |
|<span data-ttu-id="466ba-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="466ba-110">Data type:</span></span>  <br/> |<span data-ttu-id="466ba-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="466ba-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="466ba-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="466ba-112">Area:</span></span>  <br/> |<span data-ttu-id="466ba-113">Allgemeine MAPI</span><span class="sxs-lookup"><span data-stu-id="466ba-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="466ba-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="466ba-114">Remarks</span></span>

<span data-ttu-id="466ba-115">MAPI verwendet eine DLL-Datei Namenskonvention fest.</span><span class="sxs-lookup"><span data-stu-id="466ba-115">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="466ba-116">Die Basis Dateiname enthält maximal sechs Zeichen, die die DLL eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="466ba-116">The base filename contains up to six characters that uniquely identify the DLL.</span></span> <span data-ttu-id="466ba-117">MAPI fügt die Zeichenfolge 32 an den Basisnamen der DLL-Datei zum Ermitteln der Version, die auf 32-Bit-Plattformen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="466ba-117">MAPI appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="466ba-118">Beispielsweise, wenn der Name MAPI. DLL-Datei angegeben wird, MAPI erstellt den Namen MAPI32. DLL, um die entsprechenden 32-Bit-Version der DLL darstellen.</span><span class="sxs-lookup"><span data-stu-id="466ba-118">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="466ba-119">Diese Eigenschaften sollten den Basisnamen angeben.</span><span class="sxs-lookup"><span data-stu-id="466ba-119">These properties should specify the base name.</span></span> <span data-ttu-id="466ba-120">MAPI fügt die Zeichenfolge 32 entsprechend an.</span><span class="sxs-lookup"><span data-stu-id="466ba-120">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="466ba-121">Einschließlich der Zeichenfolge 32 im Rahmen dieser Eigenschaft ein Fehler ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="466ba-121">Including the string 32 as part of this property results in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="466ba-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="466ba-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="466ba-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="466ba-123">Header files</span></span>

<span data-ttu-id="466ba-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="466ba-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="466ba-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="466ba-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="466ba-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="466ba-126">Mapitags.h</span></span>
  
> <span data-ttu-id="466ba-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="466ba-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="466ba-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="466ba-128">See also</span></span>



[<span data-ttu-id="466ba-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="466ba-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="466ba-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="466ba-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="466ba-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="466ba-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="466ba-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="466ba-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

