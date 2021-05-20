---
title: PidTagMailPermission (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMailPermission
api_type:
- HeaderDef
ms.assetid: f8270ef2-56d4-4b47-bdda-a39c966bbcba
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b396cd326dd25fd72346f9f8037e8a712b84a196
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430175"
---
# <a name="pidtagmailpermission-canonical-property"></a><span data-ttu-id="d151b-103">PidTagMailPermission (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d151b-103">PidTagMailPermission Canonical Property</span></span>

  
  
<span data-ttu-id="d151b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d151b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d151b-105">Enthält TRUE, wenn der Messagingbenutzer Nachrichten senden und empfangen darf.</span><span class="sxs-lookup"><span data-stu-id="d151b-105">Contains TRUE if the messaging user is allowed to send and receive messages.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d151b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d151b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d151b-107">PR_MAIL_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="d151b-107">PR_MAIL_PERMISSION</span></span>  <br/> |
|<span data-ttu-id="d151b-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="d151b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d151b-109">0x3A0E</span><span class="sxs-lookup"><span data-stu-id="d151b-109">0x3A0E</span></span>  <br/> |
|<span data-ttu-id="d151b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d151b-110">Data type:</span></span>  <br/> |<span data-ttu-id="d151b-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d151b-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="d151b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d151b-112">Area:</span></span>  <br/> |<span data-ttu-id="d151b-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="d151b-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d151b-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d151b-114">Remarks</span></span>

<span data-ttu-id="d151b-115">Wenn diese Eigenschaft nicht festgelegt ist, wird sie von MAPI als TRUE-Wert behandelt.</span><span class="sxs-lookup"><span data-stu-id="d151b-115">If this property is not set, MAPI treats it as having a TRUE value.</span></span> 
  
<span data-ttu-id="d151b-116">Legen Sie diese Eigenschaft auf FALSE in einem Unternehmensverzeichnis, in dem einige Einträge nicht E-Mail-aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="d151b-116">Set this property to FALSE in a corporate directory where some of the entries are not email-enabled.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d151b-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d151b-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d151b-118">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="d151b-118">Header files</span></span>

<span data-ttu-id="d151b-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d151b-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="d151b-120">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d151b-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="d151b-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d151b-121">Mapitags.h</span></span>
  
> <span data-ttu-id="d151b-122">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d151b-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d151b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d151b-123">See also</span></span>



[<span data-ttu-id="d151b-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d151b-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d151b-125">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="d151b-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d151b-126">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d151b-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d151b-127">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d151b-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

