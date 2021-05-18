---
title: PidTagWizardNoPstPage (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagWizardNoPstPage
api_type:
- COM
ms.assetid: 1ac09578-892b-4c72-92f6-c2419ac2efe8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e816af2ce60b4c06ae14f720cf7c36d58468d09d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422887"
---
# <a name="pidtagwizardnopstpage-canonical-property"></a><span data-ttu-id="080dd-103">PidTagWizardNoPstPage (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="080dd-103">PidTagWizardNoPstPage Canonical Property</span></span>

  
  
<span data-ttu-id="080dd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="080dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="080dd-105">Diese Eigenschaft enthält TRUE, wenn der Profil-Assistent die Seite für den persönlichen Nachrichtenspeicher (PST) unterdrücken soll.</span><span class="sxs-lookup"><span data-stu-id="080dd-105">This property contains TRUE if the profile wizard is to suppress the personal message store (PST) page.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="080dd-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="080dd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="080dd-107">PR_WIZARD_NO_PST_PAGE</span><span class="sxs-lookup"><span data-stu-id="080dd-107">PR_WIZARD_NO_PST_PAGE</span></span>  <br/> |
|<span data-ttu-id="080dd-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="080dd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="080dd-109">0x6700</span><span class="sxs-lookup"><span data-stu-id="080dd-109">0x6700</span></span>  <br/> |
|<span data-ttu-id="080dd-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="080dd-110">Data type:</span></span>  <br/> |<span data-ttu-id="080dd-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="080dd-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="080dd-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="080dd-112">Area:</span></span>  <br/> |<span data-ttu-id="080dd-113">Exchange Administrative</span><span class="sxs-lookup"><span data-stu-id="080dd-113">Exchange Administrative</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="080dd-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="080dd-114">Remarks</span></span>

<span data-ttu-id="080dd-115">Dienstanbieter können diese Eigenschaft beim Aufrufen einer Funktion basierend auf dem PROTOTYP der [LAUNCHWIZARDENTRY-Funktion](launchwizardentry.md) festlegen.</span><span class="sxs-lookup"><span data-stu-id="080dd-115">Service providers can set this property when calling a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) function prototype.</span></span> <span data-ttu-id="080dd-116">Diese Eigenschaft teilt dem Profil-Assistenten mit, dass der Anbieter nicht möchte, dass die PST-Seite während des Benutzerdialogfelds angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="080dd-116">This property tells the profile wizard that the provider does not want the PST page to be displayed during the user dialog.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="080dd-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="080dd-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="080dd-118">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="080dd-118">Header files</span></span>

<span data-ttu-id="080dd-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="080dd-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="080dd-120">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="080dd-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="080dd-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="080dd-121">Mapitags.h</span></span>
  
> <span data-ttu-id="080dd-122">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="080dd-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="080dd-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="080dd-123">See also</span></span>



[<span data-ttu-id="080dd-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="080dd-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="080dd-125">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="080dd-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="080dd-126">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="080dd-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="080dd-127">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="080dd-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

