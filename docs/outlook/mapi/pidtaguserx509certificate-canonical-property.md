---
title: PidTagUserX509Certificate (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4e6446283116c39080271e5c2fb3ec128b25d32e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360718"
---
# <a name="pidtaguserx509certificate-canonical-property"></a><span data-ttu-id="93c99-103">PidTagUserX509Certificate (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="93c99-103">PidTagUserX509Certificate Canonical Property</span></span>

  
  
<span data-ttu-id="93c99-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93c99-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93c99-105">Enthält X.509 Version 3-Sicherheitszertifikate für einen Messagingbenutzer.</span><span class="sxs-lookup"><span data-stu-id="93c99-105">Contains X.509 version 3 security certificates for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="93c99-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="93c99-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="93c99-107">PR_USER_X509_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="93c99-107">PR_USER_X509_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="93c99-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="93c99-108">Identifier:</span></span>  <br/> |<span data-ttu-id="93c99-109">0x3A70</span><span class="sxs-lookup"><span data-stu-id="93c99-109">0x3A70</span></span>  <br/> |
|<span data-ttu-id="93c99-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="93c99-110">Data type:</span></span>  <br/> |<span data-ttu-id="93c99-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="93c99-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="93c99-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="93c99-112">Area:</span></span>  <br/> |<span data-ttu-id="93c99-113">MAPI-E-Mail-Benutzer</span><span class="sxs-lookup"><span data-stu-id="93c99-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93c99-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="93c99-114">Remarks</span></span>

<span data-ttu-id="93c99-115">Diese Eigenschaft wird von Anwendungen verwendet, die Sicherheit mit öffentlichen Schlüsseln verwenden.</span><span class="sxs-lookup"><span data-stu-id="93c99-115">This property is used by applications that utilize public-key security.</span></span> <span data-ttu-id="93c99-116">Es enthält eine binäre Darstellung von einem oder mehreren X.509 Version 3-Sicherheitszertifikaten.</span><span class="sxs-lookup"><span data-stu-id="93c99-116">It holds a binary representation of one or more X.509 version 3 security certificates.</span></span> 
  
<span data-ttu-id="93c99-117">Verschiedene Anwendungen und Clients können diese Eigenschaft für eigene Sicherheitszertifikate verwenden.</span><span class="sxs-lookup"><span data-stu-id="93c99-117">Various applications and clients can use this property for their own security certificates.</span></span> <span data-ttu-id="93c99-118">Das Binärformat der X.509-Daten kann von Anbieter zu Anbieter variieren.</span><span class="sxs-lookup"><span data-stu-id="93c99-118">The binary format of the X.509 data can vary among vendors.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="93c99-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="93c99-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="93c99-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="93c99-120">Protocol specifications</span></span>

<span data-ttu-id="93c99-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93c99-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93c99-122">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="93c99-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="93c99-123">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93c99-123">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93c99-124">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="93c99-124">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="93c99-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="93c99-125">Header files</span></span>

<span data-ttu-id="93c99-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="93c99-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="93c99-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="93c99-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="93c99-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="93c99-128">Mapitags.h</span></span>
  
> <span data-ttu-id="93c99-129">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="93c99-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="93c99-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93c99-130">See also</span></span>



[<span data-ttu-id="93c99-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="93c99-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="93c99-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="93c99-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="93c99-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="93c99-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="93c99-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="93c99-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

