---
title: PidTagAddressBookChooseDirectoryAutomatically Canonical Property
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecd0679-4bc2-4399-8f89-a4e17bb909a0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 41fdaf333084b7d567f4e67ae9fd2638a1731349
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409664"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a><span data-ttu-id="51889-103">PidTagAddressBookChooseDirectoryAutomatically Canonical Property</span><span class="sxs-lookup"><span data-stu-id="51889-103">PidTagAddressBookChooseDirectoryAutomatically Canonical Property</span></span>

  
  
<span data-ttu-id="51889-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51889-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51889-105">Ermöglicht Microsoft Outlook 2010 und Microsoft Outlook 2013, die am besten geeignete globale Adressliste (GAL) oder den Kontaktordner für das aktuelle Postfach zu wählen.</span><span class="sxs-lookup"><span data-stu-id="51889-105">Enables Microsoft Outlook 2010 and Microsoft Outlook 2013 to choose the most appropriate global address list (GAL) or contact folder for the current mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="51889-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="51889-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="51889-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span><span class="sxs-lookup"><span data-stu-id="51889-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span></span>  <br/> |
|<span data-ttu-id="51889-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="51889-108">Identifier:</span></span>  <br/> |<span data-ttu-id="51889-109">0x3D1C000B</span><span class="sxs-lookup"><span data-stu-id="51889-109">0x3D1C000B</span></span>  <br/> |
|<span data-ttu-id="51889-110">Eigenschaftstyp:</span><span class="sxs-lookup"><span data-stu-id="51889-110">Property type:</span></span>  <br/> |<span data-ttu-id="51889-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="51889-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="51889-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="51889-112">Area:</span></span>  <br/> |<span data-ttu-id="51889-113">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="51889-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51889-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="51889-114">Remarks</span></span>

<span data-ttu-id="51889-115">Diese Eigenschaft entspricht der Einstellung **Automatisch auswählen** im Dialogfeld Adressbuchoptionen.</span><span class="sxs-lookup"><span data-stu-id="51889-115">This property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="51889-116">Wenn diese Eigenschaft im Abschnitt IID_CAPONE_PROF-Profil vorhanden ist und auf **true** festgelegt ist, wird im Adressbuchdialogfeld nicht mehr standardmäßig der von der [SetDefaultDir-Methode](iaddrbook-setdefaultdir.md) angegebene Container verwendet, sondern ein Adressbuch ausgewählt, das Outlook 2010 oder Outlook 2013 für den Kontext geeignet ist, in dem das Dialogfeld angezeigt wurde.</span><span class="sxs-lookup"><span data-stu-id="51889-116">When this property exists in the IID_CAPONE_PROF profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by the [SetDefaultDir](iaddrbook-setdefaultdir.md) method, but chooses an address book that Outlook 2010 or Outlook 2013 considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="51889-117">Beachten Sie, dass dies zu einer schlechten Erfahrung für Adressbuchanbieter von Drittanbietern führen kann.</span><span class="sxs-lookup"><span data-stu-id="51889-117">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="51889-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="51889-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="51889-119">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="51889-119">Header files</span></span>

<span data-ttu-id="51889-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="51889-120">Mapitags.h</span></span>
  
> <span data-ttu-id="51889-121">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="51889-121">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="51889-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="51889-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="51889-123">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="51889-123">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="51889-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51889-124">See also</span></span>



[<span data-ttu-id="51889-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51889-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="51889-126">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="51889-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="51889-127">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="51889-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="51889-128">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="51889-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="51889-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="51889-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

