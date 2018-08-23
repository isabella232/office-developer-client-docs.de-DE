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
ms.openlocfilehash: 3bf6347102fc0865b081847a0b66763ba2654665
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589483"
---
# <a name="pidtagproviderdllname-canonical-property"></a><span data-ttu-id="100ff-103">PidTagProviderDllName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="100ff-103">PidTagProviderDllName Canonical Property</span></span>

  
  
<span data-ttu-id="100ff-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="100ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="100ff-105">Der Name der Basisdatei von MAPI Service Provider Dynamic Link Library (DLL) enthält.</span><span class="sxs-lookup"><span data-stu-id="100ff-105">Contains the base file name of the MAPI service provider dynamic-link library (DLL).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="100ff-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="100ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="100ff-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="100ff-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="100ff-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="100ff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="100ff-109">0x300A</span><span class="sxs-lookup"><span data-stu-id="100ff-109">0x300A</span></span>  <br/> |
|<span data-ttu-id="100ff-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="100ff-110">Data type:</span></span>  <br/> |<span data-ttu-id="100ff-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="100ff-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="100ff-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="100ff-112">Area:</span></span>  <br/> |<span data-ttu-id="100ff-113">Allgemeine MAPI</span><span class="sxs-lookup"><span data-stu-id="100ff-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="100ff-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="100ff-114">Remarks</span></span>

<span data-ttu-id="100ff-115">MAPI verwendet eine DLL-Datei Namenskonvention fest.</span><span class="sxs-lookup"><span data-stu-id="100ff-115">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="100ff-116">Die Basis Dateiname enthält maximal sechs Zeichen, die die DLL eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="100ff-116">The base filename contains up to six characters that uniquely identify the DLL.</span></span> <span data-ttu-id="100ff-117">MAPI fügt die Zeichenfolge 32 an den Basisnamen der DLL-Datei zum Ermitteln der Version, die auf 32-Bit-Plattformen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="100ff-117">MAPI appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="100ff-118">Beispielsweise, wenn der Name MAPI. DLL-Datei angegeben wird, MAPI erstellt den Namen MAPI32. DLL, um die entsprechenden 32-Bit-Version der DLL darstellen.</span><span class="sxs-lookup"><span data-stu-id="100ff-118">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="100ff-119">Diese Eigenschaften sollten den Basisnamen angeben.</span><span class="sxs-lookup"><span data-stu-id="100ff-119">These properties should specify the base name.</span></span> <span data-ttu-id="100ff-120">MAPI fügt die Zeichenfolge 32 entsprechend an.</span><span class="sxs-lookup"><span data-stu-id="100ff-120">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="100ff-121">Einschließlich der Zeichenfolge 32 im Rahmen dieser Eigenschaft ein Fehler ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="100ff-121">Including the string 32 as part of this property results in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="100ff-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="100ff-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="100ff-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="100ff-123">Header files</span></span>

<span data-ttu-id="100ff-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="100ff-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="100ff-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="100ff-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="100ff-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="100ff-126">Mapitags.h</span></span>
  
> <span data-ttu-id="100ff-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="100ff-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="100ff-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="100ff-128">See also</span></span>



[<span data-ttu-id="100ff-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="100ff-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="100ff-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="100ff-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="100ff-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="100ff-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="100ff-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="100ff-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

