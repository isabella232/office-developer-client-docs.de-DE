---
title: PidTagAddressBookChooseDirectoryAutomatically (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecd0679-4bc2-4399-8f89-a4e17bb909a0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 48dfced07a8fd78a1af22679759effbd3c6da343
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794056"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a><span data-ttu-id="843a7-103">PidTagAddressBookChooseDirectoryAutomatically (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="843a7-103">PidTagAddressBookChooseDirectoryAutomatically Canonical Property</span></span>

  
  
<span data-ttu-id="843a7-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="843a7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="843a7-105">Können Microsoft Outlook 2010 und Microsoft Outlook 2013, zum Auswählen der am besten geeigneten globale Adressliste (GAL) oder Kontakteordner für das aktuelle Postfach.</span><span class="sxs-lookup"><span data-stu-id="843a7-105">Enables Microsoft Outlook 2010 and Microsoft Outlook 2013 to choose the most appropriate global address list (GAL) or contact folder for the current mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="843a7-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="843a7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="843a7-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span><span class="sxs-lookup"><span data-stu-id="843a7-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span></span>  <br/> |
|<span data-ttu-id="843a7-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="843a7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="843a7-109">0x3D1C000B</span><span class="sxs-lookup"><span data-stu-id="843a7-109">0x3D1C000B</span></span>  <br/> |
|<span data-ttu-id="843a7-110">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="843a7-110">Property type:</span></span>  <br/> |<span data-ttu-id="843a7-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="843a7-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="843a7-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="843a7-112">Area:</span></span>  <br/> |<span data-ttu-id="843a7-113">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="843a7-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="843a7-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="843a7-114">Remarks</span></span>

<span data-ttu-id="843a7-115">Diese Eigenschaft entspricht der Einstellung **automatisch wählen Sie** im Dialogfeld Optionen für das Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="843a7-115">This property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="843a7-116">Wenn diese Eigenschaft im Abschnitt IID_CAPONE_PROF Profile vorhanden ist und auf **"true"**, das Adressbuch Dialogfeld nicht mehr standardmäßig auf den Container, die von der [SetDefaultDir](iaddrbook-setdefaultdir.md) -Methode angegeben, aber wählt ein Adressbuch, die festgelegt ist, Outlook 2010 oder Outlook 2013 hält entsprechenden für den Kontext, in dem das Dialogfeld angezeigt wurde.</span><span class="sxs-lookup"><span data-stu-id="843a7-116">When this property exists in the IID_CAPONE_PROF profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by the [SetDefaultDir](iaddrbook-setdefaultdir.md) method, but chooses an address book that Outlook 2010 or Outlook 2013 considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="843a7-117">Beachten Sie, dass dies eine schlechte Erfahrung für Drittanbieter-adressbuchanbietern implementierte führen kann.</span><span class="sxs-lookup"><span data-stu-id="843a7-117">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="843a7-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="843a7-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="843a7-119">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="843a7-119">Header files</span></span>

<span data-ttu-id="843a7-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="843a7-120">Mapitags.h</span></span>
  
> <span data-ttu-id="843a7-121">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="843a7-121">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="843a7-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="843a7-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="843a7-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="843a7-123">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="843a7-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="843a7-124">See also</span></span>



[<span data-ttu-id="843a7-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="843a7-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="843a7-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="843a7-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="843a7-127">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="843a7-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="843a7-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="843a7-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="843a7-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="843a7-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

