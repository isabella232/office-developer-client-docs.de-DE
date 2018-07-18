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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4cc97647c60322783050abbebd18726434632a43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794583"
---
# <a name="pidtagmailpermission-canonical-property"></a><span data-ttu-id="2e6a0-103">PidTagMailPermission (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2e6a0-103">PidTagMailPermission Canonical Property</span></span>

  
  
<span data-ttu-id="2e6a0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2e6a0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2e6a0-105">Enthält True, wenn der messaging-Benutzer senden und Empfangen von Nachrichten zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="2e6a0-105">Contains TRUE if the messaging user is allowed to send and receive messages.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2e6a0-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2e6a0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2e6a0-107">PR_MAIL_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="2e6a0-107">PR_MAIL_PERMISSION</span></span>  <br/> |
|<span data-ttu-id="2e6a0-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="2e6a0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2e6a0-109">0x3A0E</span><span class="sxs-lookup"><span data-stu-id="2e6a0-109">0x3A0E</span></span>  <br/> |
|<span data-ttu-id="2e6a0-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2e6a0-110">Data type:</span></span>  <br/> |<span data-ttu-id="2e6a0-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="2e6a0-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="2e6a0-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2e6a0-112">Area:</span></span>  <br/> |<span data-ttu-id="2e6a0-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="2e6a0-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e6a0-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e6a0-114">Remarks</span></span>

<span data-ttu-id="2e6a0-115">Wenn diese Eigenschaft nicht festgelegt ist, wird Sie MAPI wie mit dem Wert TRUE behandelt.</span><span class="sxs-lookup"><span data-stu-id="2e6a0-115">If this property is not set, MAPI treats it as having a TRUE value.</span></span> 
  
<span data-ttu-id="2e6a0-116">Legen Sie diese Eigenschaft auf false festgelegt, in ein Unternehmensverzeichnis, wo sind einige der Einträge nicht e-Mail-aktivierte.</span><span class="sxs-lookup"><span data-stu-id="2e6a0-116">Set this property to FALSE in a corporate directory where some of the entries are not email-enabled.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2e6a0-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2e6a0-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2e6a0-118">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="2e6a0-118">Header files</span></span>

<span data-ttu-id="2e6a0-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2e6a0-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="2e6a0-120">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="2e6a0-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="2e6a0-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2e6a0-121">Mapitags.h</span></span>
  
> <span data-ttu-id="2e6a0-122">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2e6a0-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2e6a0-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e6a0-123">See also</span></span>



[<span data-ttu-id="2e6a0-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2e6a0-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2e6a0-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2e6a0-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2e6a0-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2e6a0-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2e6a0-127">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2e6a0-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

