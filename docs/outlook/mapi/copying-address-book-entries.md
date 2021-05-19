---
title: Kopieren von Adressbucheinträgen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 285abeb4-45c8-4e82-9a16-b935b4651afe
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 190c4bf12c8f5aaaf8143f59239bb53fb68046f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418743"
---
# <a name="copying-address-book-entries"></a><span data-ttu-id="37759-103">Kopieren von Adressbucheinträgen</span><span class="sxs-lookup"><span data-stu-id="37759-103">Copying Address Book Entries</span></span>

  
  
<span data-ttu-id="37759-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37759-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37759-105">Die [IABContainer::CopyEntries-Methode](iabcontainer-copyentries.md) Ihres Containers wird aufgerufen, wenn ein oder mehrere Empfänger aus demselben oder einem anderen Container in diesen Container kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="37759-105">Your container's [IABContainer::CopyEntries](iabcontainer-copyentries.md) method is called when one or more recipients from the same or another container are to be copied into this container.</span></span> <span data-ttu-id="37759-106">**CopyEntries** verfügt über vier Eingabeparameter: ein Array von Eintragsbezeichnern, die die zu kopierenden Empfänger darstellen, ein Fensterhandle für die Statusanzeige, einen Statusobjektzeiger und einen Flagswert.</span><span class="sxs-lookup"><span data-stu-id="37759-106">**CopyEntries** has four input parameters: an array of entry identifiers representing the recipients to be copied, a window handle for the progress indicator, a progress object pointer, and a flags value.</span></span> <span data-ttu-id="37759-107">Ihr Anbieter sollte den Fortschritt anzeigen, wenn AB_NO_DIALOG nicht festgelegt ist, und das Progress-Objekt aus dem  _lpProgress-Parameter_ verwenden, wenn es nicht NULL ist.</span><span class="sxs-lookup"><span data-stu-id="37759-107">Your provider should display progress if the AB_NO_DIALOG flag is not set and use the progress object from the  _lpProgress_ parameter if it is not NULL.</span></span> <span data-ttu-id="37759-108">Wenn  _lpProgress_ NULL ist, rufen [Sie IMAPISupport::D oProgressDialog auf,](imapisupport-doprogressdialog.md) um das MAPI-Progress-Objekt zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="37759-108">If  _lpProgress_ is NULL, call [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) to use the MAPI progress object.</span></span> <span data-ttu-id="37759-109">Weitere Informationen zum Anzeigen des Fortschritts finden Sie unter [Displaying a Progress Indicator](mapi-progress-indicators.md).</span><span class="sxs-lookup"><span data-stu-id="37759-109">For more information about displaying progress, see [Displaying a Progress Indicator](mapi-progress-indicators.md).</span></span>
  
<span data-ttu-id="37759-110">Zusätzlich zu AB_NO_DIALOG, um einen Fortschrittsindikator zu unterdrücken, kann eines von zwei anderen Flags so festgelegt werden, dass eine Art doppelter Eintragsprüfungen CREATE_CHECK_DUP_LOOSE oder CREATE_CHECK_DUP_STRICT.</span><span class="sxs-lookup"><span data-stu-id="37759-110">In addition to AB_NO_DIALOG to suppress a progress indicator, one of two other flags can be set to request a type of duplicate entry checking: CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT.</span></span> <span data-ttu-id="37759-111">Die CREATE_CHECK_DUP_LOOSE und CREATE_CHECK_DUP_STRICT sind nur Vorschläge, wie Ihr Anbieter doppelte Einträge bestimmt und ignoriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="37759-111">The CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags are only suggestions as to how your provider determines duplicate entries and can be ignored.</span></span> <span data-ttu-id="37759-112">MAPI schlägt vor, dass Ihr Anbieter die Unterstützung für diese Flags wie folgt implementiert.</span><span class="sxs-lookup"><span data-stu-id="37759-112">MAPI suggests that your provider implement support for these flags as follows.</span></span>
  
|<span data-ttu-id="37759-113">**Doppeltes Eintragsflag**</span><span class="sxs-lookup"><span data-stu-id="37759-113">**Duplicate entry flag**</span></span>|<span data-ttu-id="37759-114">**Vorgeschlagene Implementierung**</span><span class="sxs-lookup"><span data-stu-id="37759-114">**Suggested implementation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="37759-115">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="37759-115">CREATE_CHECK_DUP_LOOSE</span></span>  <br/> |<span data-ttu-id="37759-116">Überprüfen Sie, ob der Anzeigename im zu erstellende Eintrag dem Anzeigenamen eines Eintrags entspricht, der bereits im Container vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="37759-116">Check if the display name in the entry to be created matches the display name of an entry already in the container.</span></span>  <br/> |
|<span data-ttu-id="37759-117">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="37759-117">CREATE_CHECK_DUP_STRICT</span></span>  <br/> |<span data-ttu-id="37759-118">Überprüfen Sie, ob sowohl der Anzeigename als auch der Suchschlüssel im zu erstellende Eintrag mit dem Anzeigenamen und dem Suchschlüssel eines Containereintrags übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="37759-118">Check if both the display name and the search key in the entry to be created match the display name and search key of a container entry.</span></span>  <br/> |
   
<span data-ttu-id="37759-119">Das letzte Flag, CREATE_REPLACE, gibt an, dass der neue Eintrag den vorhandenen eintrag ersetzen soll, wenn Ihr Anbieter festgestellt hat, dass ein zu erstellende Eintrag ein Duplikat eines Eintrags ist, der bereits in Ihrem Container vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="37759-119">The last flag, CREATE_REPLACE, indicates that the new entry should replace the existing one if your provider has determined that an entry to be created is a duplicate of an entry already in your container.</span></span> 
  
<span data-ttu-id="37759-120">Wenn Ihr Anbieter ein persönliches Adressbuch ist, fügen Sie **die PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) -Eigenschaft in jeden Kopiervorgang ein.</span><span class="sxs-lookup"><span data-stu-id="37759-120">If your provider is a personal address book, include the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property in every copy operation.</span></span> <span data-ttu-id="37759-121">Wenn Sie die Detailanzeigetabelle eines kopierten Empfängers verwenden, kann ihr Container die Details des Empfängers anzeigen, anstatt den ursprünglichen Container aufrufen zu müssen, um die Anzeige zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="37759-121">Including the details display table of a copied recipient enables your container to display the details of the recipient rather than having to call the original container to create the display.</span></span>
  
 <span data-ttu-id="37759-122">**So implementieren Sie IABContainer::CopyEntries**</span><span class="sxs-lookup"><span data-stu-id="37759-122">**To implement IABContainer::CopyEntries**</span></span>
  
1. <span data-ttu-id="37759-123">Ermitteln Sie, ob sich jeder Eintragsbezeichner im  _lpEntries-Parameter_ in einem Format befindet, das von Ihrem Anbieter verarbeitet wird, und falls nicht, führen Sie fehler- und MAPI_E_INVALID_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="37759-123">Determine if each entry identifier in the  _lpEntries_ parameter is in a format that your provider handles and if it is not, fail and return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="37759-124">Wenn ein Eintragsbezeichner einen Messagingbenutzer, eine Verteilerliste oder einen Container darstellt, den Ihr Anbieter verarbeitet:</span><span class="sxs-lookup"><span data-stu-id="37759-124">If an entry identifier represents a messaging user, distribution list, or container that your provider handles:</span></span>
    
1. <span data-ttu-id="37759-125">Rufen Sie [Ihre IMAPISupport::OpenEntry-Methode](imapisupport-openentry.md) auf, um den entsprechenden Empfänger zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="37759-125">Call your [IMAPISupport::OpenEntry](imapisupport-openentry.md) method to open the corresponding recipient.</span></span> 
    
2. <span data-ttu-id="37759-126">Kopieren Sie den Empfänger in Ihren Container.</span><span class="sxs-lookup"><span data-stu-id="37759-126">Copy the recipient to your container.</span></span> 
    
3. <span data-ttu-id="37759-127">Wenn der Eintragsbezeichner einen fremden Empfänger darstellt:</span><span class="sxs-lookup"><span data-stu-id="37759-127">If the entry identifier represents a foreign recipient:</span></span>
    
1. <span data-ttu-id="37759-128">Rufen Sie die [IABContainer::CreateEntry-Methode](iabcontainer-createentry.md) ihres Containers auf, um einen neuen Empfänger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="37759-128">Call your container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new recipient.</span></span> 
    
2. <span data-ttu-id="37759-129">Legen Sie die anfänglichen Eigenschaften für den neuen Empfänger ein.</span><span class="sxs-lookup"><span data-stu-id="37759-129">Set initial properties on the new recipient.</span></span>
    
4. <span data-ttu-id="37759-130">Rufen Sie die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) des neuen Objekts auf, um es zu speichern.</span><span class="sxs-lookup"><span data-stu-id="37759-130">Call the new object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it.</span></span> 
    
5. <span data-ttu-id="37759-131">Aktualisieren Sie die Inhaltstabelle des Containers so, dass sie den neuen Empfänger wiederspiegelt.</span><span class="sxs-lookup"><span data-stu-id="37759-131">Update the container's contents table to reflect the new recipient.</span></span> 
    
6. <span data-ttu-id="37759-132">Rufen [Sie IMAPISupport::Notify auf,](imapisupport-notify.md) um eine Tabellenbenachrichtigung an registrierte Clients zu senden.</span><span class="sxs-lookup"><span data-stu-id="37759-132">Call [IMAPISupport::Notify](imapisupport-notify.md) to send a table notification to registered clients.</span></span> 
    

