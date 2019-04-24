---
title: Kanonische Pidlidcustomflag (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9a131c633b8dcf9b0e5070f01de8fcab90a18ade
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357617"
---
# <a name="pidlidcustomflag-canonical-property"></a><span data-ttu-id="1873c-103">Kanonische Pidlidcustomflag (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1873c-103">PidLidCustomFlag Canonical Property</span></span>

  
  
<span data-ttu-id="1873c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1873c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1873c-105">Eine Bitmaske, die angibt, wie eine Nachricht angepasst wird, beispielsweise mit benutzerdefinierten Eigenschaften gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1873c-105">A bitmask that specifies how a message is customized, for example, saved with custom properties.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="1873c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1873c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1873c-107">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="1873c-107">dispidCustomFlag</span></span>  <br/> |
|<span data-ttu-id="1873c-108">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="1873c-108">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1873c-109">0x00008251</span><span class="sxs-lookup"><span data-stu-id="1873c-109">0x00008251</span></span>  <br/> |
|<span data-ttu-id="1873c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1873c-110">Data type:</span></span>  <br/> |<span data-ttu-id="1873c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1873c-111">PT_LONG</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1873c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1873c-112">Remarks</span></span>

<span data-ttu-id="1873c-113">Um den Wert dieser Eigenschaft abzurufen, verwenden Sie zuerst **[IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md)** , um das Property-Tag abzurufen, und geben Sie dann dieses Property-Tag in **[IMAPIProp::](imapiprop-getprops.md)** GetProps an, um den Wert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1873c-113">To retrieve the value of this property, first use **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** to obtain the property tag, and then specify this property tag in **[IMAPIProp::GetProps](imapiprop-getprops.md)** to get the value.</span></span> 
  
<span data-ttu-id="1873c-114">Mögliche Flags sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1873c-114">Possible Flags are as follows:</span></span>
  
****

|<span data-ttu-id="1873c-115">**Konstante**</span><span class="sxs-lookup"><span data-stu-id="1873c-115">**Constant**</span></span>|<span data-ttu-id="1873c-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="1873c-116">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1873c-117">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="1873c-117">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="1873c-118">0x0D000000</span><span class="sxs-lookup"><span data-stu-id="1873c-118">0x0D000000</span></span>  <br/> |
|<span data-ttu-id="1873c-119">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="1873c-119">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="1873c-120">0x02000000</span><span class="sxs-lookup"><span data-stu-id="1873c-120">0x02000000</span></span>  <br/> |
   
<span data-ttu-id="1873c-121">Geben Sie beim Aufrufen von **IMAPIProp:: GetIDsFromNames**die folgenden Werte für die **[MAPINAMEID](mapinameid.md)** -Struktur an, auf die durch den Eingabeparameter *lppPropNames* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1873c-121">When calling **IMAPIProp::GetIDsFromNames**, specify the following values for the **[MAPINAMEID](mapinameid.md)** structure pointed to by the input parameter  *lppPropNames*  .</span></span> 
  
****

|<span data-ttu-id="1873c-122">**Member**</span><span class="sxs-lookup"><span data-stu-id="1873c-122">**Member**</span></span>|<span data-ttu-id="1873c-123">**Value**</span><span class="sxs-lookup"><span data-stu-id="1873c-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1873c-124">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="1873c-124">lpGuid:</span></span>  <br/> |<span data-ttu-id="1873c-125">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="1873c-125">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="1873c-126">ulKind:</span><span class="sxs-lookup"><span data-stu-id="1873c-126">ulKind:</span></span>  <br/> |<span data-ttu-id="1873c-127">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="1873c-127">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="1873c-128">Art. lID:</span><span class="sxs-lookup"><span data-stu-id="1873c-128">Kind.lID:</span></span>  <br/> |<span data-ttu-id="1873c-129">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="1873c-129">dispidCustomFlag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1873c-130">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1873c-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1873c-131">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1873c-131">Protocol specifications</span></span>

<span data-ttu-id="1873c-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1873c-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1873c-133">Stellt Definitionen für Eigenschaftensätze bereit.</span><span class="sxs-lookup"><span data-stu-id="1873c-133">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1873c-134">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="1873c-134">Header files</span></span>

<span data-ttu-id="1873c-135">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1873c-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="1873c-136">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="1873c-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="1873c-137">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="1873c-137">Mapitags.h</span></span>
  
> <span data-ttu-id="1873c-138">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="1873c-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1873c-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1873c-139">See also</span></span>



[<span data-ttu-id="1873c-140">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1873c-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1873c-141">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1873c-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1873c-142">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1873c-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1873c-143">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1873c-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

