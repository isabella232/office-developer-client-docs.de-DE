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
ms.openlocfilehash: cba4989ec3b1afcadb0caddd4af444cc9c96ebda
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565956"
---
# <a name="pidlidcustomflag-canonical-property"></a><span data-ttu-id="7648d-103">PidLidCustomFlag (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7648d-103">PidLidCustomFlag Canonical Property</span></span>

  
  
<span data-ttu-id="7648d-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7648d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7648d-105">Eine Bitmaske, die angibt, wie eine Nachricht angepasst ist, beispielsweise mit benutzerdefinierten Eigenschaften gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7648d-105">A bitmask that specifies how a message is customized, for example, saved with custom properties.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="7648d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7648d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7648d-107">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="7648d-107">dispidCustomFlag</span></span>  <br/> |
|<span data-ttu-id="7648d-108">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="7648d-108">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7648d-109">0x00008251</span><span class="sxs-lookup"><span data-stu-id="7648d-109">0x00008251</span></span>  <br/> |
|<span data-ttu-id="7648d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7648d-110">Data type:</span></span>  <br/> |<span data-ttu-id="7648d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7648d-111">PT_LONG</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7648d-112">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="7648d-112">Remarks</span></span>

<span data-ttu-id="7648d-113">Um den Wert dieser Eigenschaft abzurufen, zunächst mit dem **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** um das Eigenschafts-Tag zu erhalten, und geben Sie in **[IMAPIProp::GetProps](imapiprop-getprops.md)** zum Abrufen des Werts dieser Eigenschaftentag.</span><span class="sxs-lookup"><span data-stu-id="7648d-113">To retrieve the value of this property, first use **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** to obtain the property tag, and then specify this property tag in **[IMAPIProp::GetProps](imapiprop-getprops.md)** to get the value.</span></span> 
  
<span data-ttu-id="7648d-114">Mögliche Flags lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7648d-114">Possible Flags are as follows:</span></span>
  
****

|<span data-ttu-id="7648d-115">**Konstante**</span><span class="sxs-lookup"><span data-stu-id="7648d-115">**Constant**</span></span>|<span data-ttu-id="7648d-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7648d-116">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7648d-117">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="7648d-117">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="7648d-118">0x0D000000</span><span class="sxs-lookup"><span data-stu-id="7648d-118">0x0D000000</span></span>  <br/> |
|<span data-ttu-id="7648d-119">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="7648d-119">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="7648d-120">0x02000000</span><span class="sxs-lookup"><span data-stu-id="7648d-120">0x02000000</span></span>  <br/> |
   
<span data-ttu-id="7648d-121">Beim Aufruf von **IMAPIProp::GetIDsFromNames**, geben Sie die folgenden Werte für die **[MAPINAMEID](mapinameid.md)** -Struktur, die auf den Eingabeparameter *LppPropNames* zeigt.</span><span class="sxs-lookup"><span data-stu-id="7648d-121">When calling **IMAPIProp::GetIDsFromNames**, specify the following values for the **[MAPINAMEID](mapinameid.md)** structure pointed to by the input parameter  *lppPropNames*  .</span></span> 
  
****

|<span data-ttu-id="7648d-122">**Member**</span><span class="sxs-lookup"><span data-stu-id="7648d-122">**Member**</span></span>|<span data-ttu-id="7648d-123">**Value**</span><span class="sxs-lookup"><span data-stu-id="7648d-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7648d-124">x LpGuid:</span><span class="sxs-lookup"><span data-stu-id="7648d-124">lpGuid:</span></span>  <br/> |<span data-ttu-id="7648d-125">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="7648d-125">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="7648d-126">UlKind:</span><span class="sxs-lookup"><span data-stu-id="7648d-126">ulKind:</span></span>  <br/> |<span data-ttu-id="7648d-127">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="7648d-127">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="7648d-128">Kind.lID:</span><span class="sxs-lookup"><span data-stu-id="7648d-128">Kind.lID:</span></span>  <br/> |<span data-ttu-id="7648d-129">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="7648d-129">dispidCustomFlag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7648d-130">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7648d-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7648d-131">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7648d-131">Protocol specifications</span></span>

<span data-ttu-id="7648d-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7648d-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7648d-133">Enthält Eigenschaftendefinitionen an.</span><span class="sxs-lookup"><span data-stu-id="7648d-133">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7648d-134">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="7648d-134">Header files</span></span>

<span data-ttu-id="7648d-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7648d-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="7648d-136">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7648d-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="7648d-137">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7648d-137">Mapitags.h</span></span>
  
> <span data-ttu-id="7648d-138">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7648d-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7648d-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7648d-139">See also</span></span>



[<span data-ttu-id="7648d-140">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7648d-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7648d-141">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7648d-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7648d-142">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7648d-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7648d-143">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7648d-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

