---
title: Kanonische Pidlidsharinginitiatorsmtp (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingInitiatorSmtp
api_type:
- COM
ms.assetid: 4fb7d91d-4c51-41c1-9cb6-7b837dd12f11
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: eb699b2312064f8ed330238962dd86992c046139
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337121"
---
# <a name="pidlidsharinginitiatorsmtp-canonical-property"></a><span data-ttu-id="03468-103">Kanonische Pidlidsharinginitiatorsmtp (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="03468-103">PidLidSharingInitiatorSmtp Canonical Property</span></span>

  
  
<span data-ttu-id="03468-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03468-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03468-105">Gibt die SMTP-Adresse des Benutzers an, der die Freigabenachricht initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="03468-105">Specifies the SMTP address of the user who initiated the sharing message.</span></span> <span data-ttu-id="03468-106">Dies ist eine Eigenschaft einer Freigabenachricht.</span><span class="sxs-lookup"><span data-stu-id="03468-106">This is a property of a sharing message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="03468-107">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="03468-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="03468-108">dispidSharingInitiatorSmtp</span><span class="sxs-lookup"><span data-stu-id="03468-108">dispidSharingInitiatorSmtp</span></span>  <br/> |
|<span data-ttu-id="03468-109">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="03468-109">Property set:</span></span>  <br/> |<span data-ttu-id="03468-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="03468-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="03468-111">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="03468-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="03468-112">0x00008A08</span><span class="sxs-lookup"><span data-stu-id="03468-112">0x00008A08</span></span>  <br/> |
|<span data-ttu-id="03468-113">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="03468-113">Data type:</span></span>  <br/> |<span data-ttu-id="03468-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="03468-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="03468-115">Bereich:</span><span class="sxs-lookup"><span data-stu-id="03468-115">Area:</span></span>  <br/> |<span data-ttu-id="03468-116">Freigabe</span><span class="sxs-lookup"><span data-stu-id="03468-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03468-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03468-117">Remarks</span></span>

<span data-ttu-id="03468-118">Diese Eigenschaft muss auf den Wert der **PR_SMTP_ADDRESS** ([PidTagSmtpAddress](pidtagsmtpaddress-canonical-property.md))-Eigenschaft aus dem Adressbuch festgelegt werden, das von der **dispidSharingInitiatorEid** ([pidlidsharinginitiatorentryid (](pidlidsharinginitiatorentryid-canonical-property.md))-Eigenschaft identifiziert wird, und sollte ignoriert.</span><span class="sxs-lookup"><span data-stu-id="03468-118">This property must be set to the value of the **PR_SMTP_ADDRESS** ([PidTagSmtpAddress](pidtagsmtpaddress-canonical-property.md)) property from the Address Book identified by the **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) property and should be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="03468-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="03468-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="03468-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="03468-120">Protocol specifications</span></span>

<span data-ttu-id="03468-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03468-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03468-122">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="03468-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="03468-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03468-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03468-124">Freigabe von Postfachordnern zwischen Clients.</span><span class="sxs-lookup"><span data-stu-id="03468-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="03468-125">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="03468-125">Header files</span></span>

<span data-ttu-id="03468-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="03468-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="03468-127">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="03468-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="03468-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03468-128">See also</span></span>



[<span data-ttu-id="03468-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="03468-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="03468-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="03468-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="03468-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="03468-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="03468-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="03468-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

