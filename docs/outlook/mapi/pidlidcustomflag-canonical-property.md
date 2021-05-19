---
title: PidLidCustomFlag (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCustomFlag
api_type:
- COM
ms.assetid: bfb7fd1e-774f-9a2f-fbbe-ba7f68ed8663
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9a131c633b8dcf9b0e5070f01de8fcab90a18ade
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357617"
---
# <a name="pidlidcustomflag-canonical-property"></a><span data-ttu-id="4677b-103">PidLidCustomFlag (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4677b-103">PidLidCustomFlag Canonical Property</span></span>

  
  
<span data-ttu-id="4677b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4677b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4677b-105">Eine Bitmaske, die angibt, wie eine Nachricht angepasst wird, z. B. mit benutzerdefinierten Eigenschaften gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="4677b-105">A bitmask that specifies how a message is customized, for example, saved with custom properties.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="4677b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4677b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4677b-107">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="4677b-107">dispidCustomFlag</span></span>  <br/> |
|<span data-ttu-id="4677b-108">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="4677b-108">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4677b-109">0x00008251</span><span class="sxs-lookup"><span data-stu-id="4677b-109">0x00008251</span></span>  <br/> |
|<span data-ttu-id="4677b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4677b-110">Data type:</span></span>  <br/> |<span data-ttu-id="4677b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4677b-111">PT_LONG</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4677b-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4677b-112">Remarks</span></span>

<span data-ttu-id="4677b-113">Um den Wert dieser Eigenschaft abzurufen, verwenden Sie zunächst **[IMAPIProp::GetIDsFromNames,](imapiprop-getidsfromnames.md)** um das Eigenschaftstag abzurufen, und geben Sie dann dieses Eigenschaftstag in **[IMAPIProp::GetProps](imapiprop-getprops.md)** an, um den Wert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4677b-113">To retrieve the value of this property, first use **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** to obtain the property tag, and then specify this property tag in **[IMAPIProp::GetProps](imapiprop-getprops.md)** to get the value.</span></span> 
  
<span data-ttu-id="4677b-114">Mögliche Flags sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4677b-114">Possible Flags are as follows:</span></span>
  
****

|<span data-ttu-id="4677b-115">**Konstante**</span><span class="sxs-lookup"><span data-stu-id="4677b-115">**Constant**</span></span>|<span data-ttu-id="4677b-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="4677b-116">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4677b-117">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="4677b-117">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="4677b-118">0x0D000000</span><span class="sxs-lookup"><span data-stu-id="4677b-118">0x0D000000</span></span>  <br/> |
|<span data-ttu-id="4677b-119">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="4677b-119">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="4677b-120">0x02000000</span><span class="sxs-lookup"><span data-stu-id="4677b-120">0x02000000</span></span>  <br/> |
   
<span data-ttu-id="4677b-121">Geben Sie beim Aufrufen von **IMAPIProp::GetIDsFromNames** die folgenden Werte für die **[MAPINAMEID-Struktur](mapinameid.md)** an, auf die der Eingabeparameter *lppPropNames verweist.*</span><span class="sxs-lookup"><span data-stu-id="4677b-121">When calling **IMAPIProp::GetIDsFromNames**, specify the following values for the **[MAPINAMEID](mapinameid.md)** structure pointed to by the input parameter  *lppPropNames*  .</span></span> 
  
****

|<span data-ttu-id="4677b-122">**Member**</span><span class="sxs-lookup"><span data-stu-id="4677b-122">**Member**</span></span>|<span data-ttu-id="4677b-123">**Value**</span><span class="sxs-lookup"><span data-stu-id="4677b-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4677b-124">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="4677b-124">lpGuid:</span></span>  <br/> |<span data-ttu-id="4677b-125">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="4677b-125">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="4677b-126">ulKind:</span><span class="sxs-lookup"><span data-stu-id="4677b-126">ulKind:</span></span>  <br/> |<span data-ttu-id="4677b-127">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="4677b-127">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="4677b-128">Kind.lID:</span><span class="sxs-lookup"><span data-stu-id="4677b-128">Kind.lID:</span></span>  <br/> |<span data-ttu-id="4677b-129">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="4677b-129">dispidCustomFlag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="4677b-130">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4677b-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4677b-131">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4677b-131">Protocol specifications</span></span>

<span data-ttu-id="4677b-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4677b-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4677b-133">Stellt Eigenschaftensatzdefinitionen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="4677b-133">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4677b-134">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="4677b-134">Header files</span></span>

<span data-ttu-id="4677b-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4677b-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="4677b-136">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4677b-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="4677b-137">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4677b-137">Mapitags.h</span></span>
  
> <span data-ttu-id="4677b-138">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="4677b-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4677b-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4677b-139">See also</span></span>



[<span data-ttu-id="4677b-140">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4677b-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4677b-141">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="4677b-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4677b-142">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4677b-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4677b-143">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4677b-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

