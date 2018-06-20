---
title: Kanonische PidLidSharingInitiatorSmtp-Eigenschaft
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
ms.openlocfilehash: 188424fc67534ea5df6ed5eb209909731e12c73c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793786"
---
# <a name="pidlidsharinginitiatorsmtp-canonical-property"></a><span data-ttu-id="d15ec-103">Kanonische PidLidSharingInitiatorSmtp-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d15ec-103">PidLidSharingInitiatorSmtp Canonical Property</span></span>

  
  
<span data-ttu-id="d15ec-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d15ec-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d15ec-105">Gibt die SMTP-Adresse des Benutzers, der die Freigabenachricht initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="d15ec-105">Specifies the SMTP address of the user who initiated the sharing message.</span></span> <span data-ttu-id="d15ec-106">Dies ist eine Eigenschaft eines eine Freigabenachricht.</span><span class="sxs-lookup"><span data-stu-id="d15ec-106">This is a property of a sharing message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d15ec-107">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d15ec-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="d15ec-108">dispidSharingInitiatorSmtp</span><span class="sxs-lookup"><span data-stu-id="d15ec-108">dispidSharingInitiatorSmtp</span></span>  <br/> |
|<span data-ttu-id="d15ec-109">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="d15ec-109">Property set:</span></span>  <br/> |<span data-ttu-id="d15ec-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="d15ec-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="d15ec-111">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="d15ec-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d15ec-112">0x00008A08</span><span class="sxs-lookup"><span data-stu-id="d15ec-112">0x00008A08</span></span>  <br/> |
|<span data-ttu-id="d15ec-113">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d15ec-113">Data type:</span></span>  <br/> |<span data-ttu-id="d15ec-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d15ec-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d15ec-115">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d15ec-115">Area:</span></span>  <br/> |<span data-ttu-id="d15ec-116">Freigabe</span><span class="sxs-lookup"><span data-stu-id="d15ec-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d15ec-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d15ec-117">Remarks</span></span>

<span data-ttu-id="d15ec-118">Diese Eigenschaft muss auf den Wert der Eigenschaft **PR_SMTP_ADDRESS** ([PidTagSmtpAddress](pidtagsmtpaddress-canonical-property.md)) aus dem Adressbuch identifiziert durch die **DispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md))-Eigenschaft festgelegt und werden sollten ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d15ec-118">This property must be set to the value of the **PR_SMTP_ADDRESS** ([PidTagSmtpAddress](pidtagsmtpaddress-canonical-property.md)) property from the Address Book identified by the **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) property and should be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d15ec-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d15ec-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d15ec-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d15ec-120">Protocol specifications</span></span>

<span data-ttu-id="d15ec-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d15ec-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d15ec-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="d15ec-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d15ec-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d15ec-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d15ec-124">Teilt Postfachordner zwischen Clients.</span><span class="sxs-lookup"><span data-stu-id="d15ec-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d15ec-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="d15ec-125">Header files</span></span>

<span data-ttu-id="d15ec-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d15ec-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d15ec-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d15ec-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d15ec-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d15ec-128">See also</span></span>



[<span data-ttu-id="d15ec-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d15ec-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d15ec-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d15ec-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d15ec-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d15ec-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d15ec-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d15ec-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

