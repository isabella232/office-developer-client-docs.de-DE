---
title: Kanonische Pidtagaddressbookchoosedirectoryautomatically (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecd0679-4bc2-4399-8f89-a4e17bb909a0
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 41fdaf333084b7d567f4e67ae9fd2638a1731349
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359788"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a><span data-ttu-id="2d87b-103">Kanonische Pidtagaddressbookchoosedirectoryautomatically (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2d87b-103">PidTagAddressBookChooseDirectoryAutomatically Canonical Property</span></span>

  
  
<span data-ttu-id="2d87b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d87b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d87b-105">Ermöglicht Microsoft Outlook 2010 und Microsoft Outlook 2013, die am besten geeignete globale Adressliste (GAL) oder den Kontaktordner für das aktuelle Postfach auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="2d87b-105">Enables Microsoft Outlook 2010 and Microsoft Outlook 2013 to choose the most appropriate global address list (GAL) or contact folder for the current mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2d87b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2d87b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2d87b-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span><span class="sxs-lookup"><span data-stu-id="2d87b-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span></span>  <br/> |
|<span data-ttu-id="2d87b-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="2d87b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2d87b-109">0x3D1C000B</span><span class="sxs-lookup"><span data-stu-id="2d87b-109">0x3D1C000B</span></span>  <br/> |
|<span data-ttu-id="2d87b-110">Eigenschafts:</span><span class="sxs-lookup"><span data-stu-id="2d87b-110">Property type:</span></span>  <br/> |<span data-ttu-id="2d87b-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="2d87b-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="2d87b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2d87b-112">Area:</span></span>  <br/> |<span data-ttu-id="2d87b-113">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="2d87b-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d87b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d87b-114">Remarks</span></span>

<span data-ttu-id="2d87b-115">Diese Eigenschaft entspricht der Einstellung **automatisch auswählen** im Dialogfeld Adressbuchoptionen.</span><span class="sxs-lookup"><span data-stu-id="2d87b-115">This property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="2d87b-116">Wenn diese Eigenschaft im Abschnitt IID_CAPONE_PROF vorhanden ist und auf **true**festgelegt ist, ist das Adressbuch-Dialogfeld nicht mehr standardmäßig der Container von der [SetDefaultDir](iaddrbook-setdefaultdir.md) -Methode angegeben, aber wählt ein adressbuch, outlook 2010 oder Outlook 2013 ist für den Kontext geeignet, in dem das Dialogfeld angezeigt wurde.</span><span class="sxs-lookup"><span data-stu-id="2d87b-116">When this property exists in the IID_CAPONE_PROF profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by the [SetDefaultDir](iaddrbook-setdefaultdir.md) method, but chooses an address book that Outlook 2010 or Outlook 2013 considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="2d87b-117">Beachten Sie, dass dies zu einer schlechten Erfahrung für Drittanbieter-Adressbuchanbieter führen kann.</span><span class="sxs-lookup"><span data-stu-id="2d87b-117">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2d87b-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2d87b-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2d87b-119">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="2d87b-119">Header files</span></span>

<span data-ttu-id="2d87b-120">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="2d87b-120">Mapitags.h</span></span>
  
> <span data-ttu-id="2d87b-121">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="2d87b-121">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="2d87b-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2d87b-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="2d87b-123">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="2d87b-123">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2d87b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d87b-124">See also</span></span>



[<span data-ttu-id="2d87b-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2d87b-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2d87b-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2d87b-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2d87b-127">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="2d87b-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="2d87b-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2d87b-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2d87b-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2d87b-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

