---
title: Kanonische PidTagUserX509Certificate-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUserX509Certificate
api_type:
- COM
ms.assetid: 278bb9e4-3ff6-4bef-b208-7924f7a5e9b1
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d27ef47a3ba387ae2e7acbcefc75b07ddd794e80
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795288"
---
# <a name="pidtaguserx509certificate-canonical-property"></a><span data-ttu-id="c5039-103">Kanonische PidTagUserX509Certificate-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c5039-103">PidTagUserX509Certificate Canonical Property</span></span>

  
  
<span data-ttu-id="c5039-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c5039-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c5039-105">X. 509 Version 3 Sicherheitszertifikate für ein messaging-Benutzer enthält.</span><span class="sxs-lookup"><span data-stu-id="c5039-105">Contains X.509 version 3 security certificates for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c5039-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c5039-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c5039-107">PR_USER_X509_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="c5039-107">PR_USER_X509_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="c5039-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="c5039-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c5039-109">0x3A70</span><span class="sxs-lookup"><span data-stu-id="c5039-109">0x3A70</span></span>  <br/> |
|<span data-ttu-id="c5039-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c5039-110">Data type:</span></span>  <br/> |<span data-ttu-id="c5039-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="c5039-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="c5039-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c5039-112">Area:</span></span>  <br/> |<span data-ttu-id="c5039-113">MAPI-e-Mail-Benutzer</span><span class="sxs-lookup"><span data-stu-id="c5039-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5039-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c5039-114">Remarks</span></span>

<span data-ttu-id="c5039-115">Diese Eigenschaft wird von Clientanwendungen, die öffentliche Schlüssel Sicherheit zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="c5039-115">This property is used by applications that utilize public-key security.</span></span> <span data-ttu-id="c5039-116">Sie enthält eine binäre Darstellung von einem oder mehreren x. 509 Version 3 Sicherheitszertifikaten.</span><span class="sxs-lookup"><span data-stu-id="c5039-116">It holds a binary representation of one or more X.509 version 3 security certificates.</span></span> 
  
<span data-ttu-id="c5039-117">Verschiedene Anwendungen und Clients können diese Eigenschaft für ihre eigenen Sicherheitszertifikate verwenden.</span><span class="sxs-lookup"><span data-stu-id="c5039-117">Various applications and clients can use this property for their own security certificates.</span></span> <span data-ttu-id="c5039-118">Das Binärformat der x. 509-Daten kann Anbieter unterschiedlich sein.</span><span class="sxs-lookup"><span data-stu-id="c5039-118">The binary format of the X.509 data can vary among vendors.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c5039-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c5039-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c5039-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c5039-120">Protocol specifications</span></span>

<span data-ttu-id="c5039-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5039-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5039-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c5039-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c5039-123">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5039-123">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5039-124">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="c5039-124">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c5039-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="c5039-125">Header files</span></span>

<span data-ttu-id="c5039-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c5039-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c5039-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c5039-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="c5039-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c5039-128">Mapitags.h</span></span>
  
> <span data-ttu-id="c5039-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c5039-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c5039-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5039-130">See also</span></span>



[<span data-ttu-id="c5039-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c5039-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c5039-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c5039-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c5039-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c5039-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c5039-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c5039-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

