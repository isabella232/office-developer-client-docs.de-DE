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
ms.openlocfilehash: fb0b66cbf0de1ac351bb2026a48e0154de779206
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571192"
---
# <a name="pidtagmailpermission-canonical-property"></a><span data-ttu-id="7c270-103">PidTagMailPermission (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7c270-103">PidTagMailPermission Canonical Property</span></span>

  
  
<span data-ttu-id="7c270-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c270-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c270-105">Enthält True, wenn der messaging-Benutzer senden und Empfangen von Nachrichten zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="7c270-105">Contains TRUE if the messaging user is allowed to send and receive messages.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7c270-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7c270-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7c270-107">PR_MAIL_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="7c270-107">PR_MAIL_PERMISSION</span></span>  <br/> |
|<span data-ttu-id="7c270-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="7c270-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7c270-109">0x3A0E</span><span class="sxs-lookup"><span data-stu-id="7c270-109">0x3A0E</span></span>  <br/> |
|<span data-ttu-id="7c270-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7c270-110">Data type:</span></span>  <br/> |<span data-ttu-id="7c270-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="7c270-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="7c270-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7c270-112">Area:</span></span>  <br/> |<span data-ttu-id="7c270-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="7c270-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c270-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="7c270-114">Remarks</span></span>

<span data-ttu-id="7c270-115">Wenn diese Eigenschaft nicht festgelegt ist, wird Sie MAPI wie mit dem Wert TRUE behandelt.</span><span class="sxs-lookup"><span data-stu-id="7c270-115">If this property is not set, MAPI treats it as having a TRUE value.</span></span> 
  
<span data-ttu-id="7c270-116">Legen Sie diese Eigenschaft auf false festgelegt, in ein Unternehmensverzeichnis, wo sind einige der Einträge nicht e-Mail-aktivierte.</span><span class="sxs-lookup"><span data-stu-id="7c270-116">Set this property to FALSE in a corporate directory where some of the entries are not email-enabled.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7c270-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7c270-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7c270-118">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="7c270-118">Header files</span></span>

<span data-ttu-id="7c270-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7c270-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="7c270-120">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7c270-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="7c270-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7c270-121">Mapitags.h</span></span>
  
> <span data-ttu-id="7c270-122">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7c270-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7c270-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c270-123">See also</span></span>



[<span data-ttu-id="7c270-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7c270-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7c270-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7c270-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7c270-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7c270-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7c270-127">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7c270-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

