---
title: Kopieren von Adressbucheinträgen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 285abeb4-45c8-4e82-9a16-b935b4651afe
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 190c4bf12c8f5aaaf8143f59239bb53fb68046f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333068"
---
# <a name="copying-address-book-entries"></a><span data-ttu-id="69e98-103">Kopieren von Adressbucheinträgen</span><span class="sxs-lookup"><span data-stu-id="69e98-103">Copying Address Book Entries</span></span>

  
  
<span data-ttu-id="69e98-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69e98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69e98-105">Die [IABContainer:: CopyEntries](iabcontainer-copyentries.md) -Methode des Containers wird aufgerufen, wenn ein oder mehrere Empfänger aus demselben oder einem anderen Container in diesen Container kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="69e98-105">Your container's [IABContainer::CopyEntries](iabcontainer-copyentries.md) method is called when one or more recipients from the same or another container are to be copied into this container.</span></span> <span data-ttu-id="69e98-106">**CopyEntries** verfügt über vier Eingabeparameter: ein Array von Eintrags-IDs, das die zu kopierenden Empfänger darstellt, ein Fensterhandle für die Statusanzeige, einen Statusobjekt Zeiger und einen Flags-Wert.</span><span class="sxs-lookup"><span data-stu-id="69e98-106">**CopyEntries** has four input parameters: an array of entry identifiers representing the recipients to be copied, a window handle for the progress indicator, a progress object pointer, and a flags value.</span></span> <span data-ttu-id="69e98-107">Ihr Anbieter sollte den Fortschrittanzeigen, wenn das AB_NO_DIALOG-Flag nicht festgelegt ist, und das Progress-Objekt aus dem _lpProgress_ -Parameter verwenden, wenn es nicht NULL ist.</span><span class="sxs-lookup"><span data-stu-id="69e98-107">Your provider should display progress if the AB_NO_DIALOG flag is not set and use the progress object from the  _lpProgress_ parameter if it is not NULL.</span></span> <span data-ttu-id="69e98-108">Wenn _lpProgress_ ist, rufen Sie [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) auf, um das MAPI-Progress-Objekt zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="69e98-108">If  _lpProgress_ is NULL, call [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) to use the MAPI progress object.</span></span> <span data-ttu-id="69e98-109">Weitere Informationen zum Anzeigen des Fortschritts finden Sie unter [Anzeigen einer Statusanzeige](mapi-progress-indicators.md).</span><span class="sxs-lookup"><span data-stu-id="69e98-109">For more information about displaying progress, see [Displaying a Progress Indicator](mapi-progress-indicators.md).</span></span>
  
<span data-ttu-id="69e98-110">Zusätzlich zu AB_NO_DIALOG, um eine Statusanzeige zu unterdrücken, kann eine der beiden anderen Flags so festgelegt werden, dass ein Typ doppelter Eintrags Überprüfung angefordert wird: CREATE_CHECK_DUP_LOOSE oder CREATE_CHECK_DUP_STRICT.</span><span class="sxs-lookup"><span data-stu-id="69e98-110">In addition to AB_NO_DIALOG to suppress a progress indicator, one of two other flags can be set to request a type of duplicate entry checking: CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT.</span></span> <span data-ttu-id="69e98-111">Die Flags CREATE_CHECK_DUP_LOOSE und CREATE_CHECK_DUP_STRICT sind nur Vorschläge, wie Ihr Anbieter doppelte Einträge bestimmt und ignoriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="69e98-111">The CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags are only suggestions as to how your provider determines duplicate entries and can be ignored.</span></span> <span data-ttu-id="69e98-112">MAPI schlägt vor, dass Ihr Anbieter die Unterstützung für diese Flags wie folgt implementiert.</span><span class="sxs-lookup"><span data-stu-id="69e98-112">MAPI suggests that your provider implement support for these flags as follows.</span></span>
  
|<span data-ttu-id="69e98-113">**Flag für doppelten Eintrag**</span><span class="sxs-lookup"><span data-stu-id="69e98-113">**Duplicate entry flag**</span></span>|<span data-ttu-id="69e98-114">**Vorgeschlagene Implementierung**</span><span class="sxs-lookup"><span data-stu-id="69e98-114">**Suggested implementation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="69e98-115">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="69e98-115">CREATE_CHECK_DUP_LOOSE</span></span>  <br/> |<span data-ttu-id="69e98-116">Überprüfen Sie, ob der Anzeigename im zu erstellenden Eintrag mit dem Anzeigenamen eines Eintrags übereinstimmt, der sich bereits im Container befindet.</span><span class="sxs-lookup"><span data-stu-id="69e98-116">Check if the display name in the entry to be created matches the display name of an entry already in the container.</span></span>  <br/> |
|<span data-ttu-id="69e98-117">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="69e98-117">CREATE_CHECK_DUP_STRICT</span></span>  <br/> |<span data-ttu-id="69e98-118">Überprüfen Sie, ob der Anzeigename und der Suchschlüssel im zu erstellenden Eintrag mit dem Anzeigenamen und dem Suchschlüssel eines Container Eintrags übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="69e98-118">Check if both the display name and the search key in the entry to be created match the display name and search key of a container entry.</span></span>  <br/> |
   
<span data-ttu-id="69e98-119">Das letzte Flag, CREATE_REPLACE, gibt an, dass der neue Eintrag die vorhandene ersetzen soll, wenn Ihr Anbieter festgestellt hat, dass ein zu Erstell ender Eintrag ein Duplikat eines Eintrags in Ihrem Container ist.</span><span class="sxs-lookup"><span data-stu-id="69e98-119">The last flag, CREATE_REPLACE, indicates that the new entry should replace the existing one if your provider has determined that an entry to be created is a duplicate of an entry already in your container.</span></span> 
  
<span data-ttu-id="69e98-120">Wenn es sich bei Ihrem Anbieter um ein persönliches Adressbuch handelt, schließen Sie die **PR_DETAILS_TABLE** ([pidtagdetailstable (](pidtagdetailstable-canonical-property.md))-Eigenschaft in jeden Kopiervorgang ein.</span><span class="sxs-lookup"><span data-stu-id="69e98-120">If your provider is a personal address book, include the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property in every copy operation.</span></span> <span data-ttu-id="69e98-121">Das Einschließen der Details-Anzeigetabelle eines kopierten Empfängers ermöglicht es Ihrem Container, die Details des Empfängers anzuzeigen, statt den ursprünglichen Container aufrufen zu müssen, um die Anzeige zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="69e98-121">Including the details display table of a copied recipient enables your container to display the details of the recipient rather than having to call the original container to create the display.</span></span>
  
 <span data-ttu-id="69e98-122">**So implementieren Sie IABContainer:: CopyEntries**</span><span class="sxs-lookup"><span data-stu-id="69e98-122">**To implement IABContainer::CopyEntries**</span></span>
  
1. <span data-ttu-id="69e98-123">Bestimmen Sie, ob sich jede Eintrags-ID im _lpEntries_ -Parameter in einem Format befindet, das Ihr Anbieter verarbeitet, und wenn dies nicht der Fall ist, und geben Sie MAPI_E_INVALID_ENTRYID zurück.</span><span class="sxs-lookup"><span data-stu-id="69e98-123">Determine if each entry identifier in the  _lpEntries_ parameter is in a format that your provider handles and if it is not, fail and return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="69e98-124">Wenn eine Eintrags-ID einen Messagingbenutzer, eine Verteilerliste oder einen Container darstellt, die der Anbieter behandelt:</span><span class="sxs-lookup"><span data-stu-id="69e98-124">If an entry identifier represents a messaging user, distribution list, or container that your provider handles:</span></span>
    
1. <span data-ttu-id="69e98-125">Rufen Sie Ihre [IMAPISupport:: OpenEntry](imapisupport-openentry.md) -Methode auf, um den entsprechenden Empfänger zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="69e98-125">Call your [IMAPISupport::OpenEntry](imapisupport-openentry.md) method to open the corresponding recipient.</span></span> 
    
2. <span data-ttu-id="69e98-126">Kopieren Sie den Empfänger in ihren Container.</span><span class="sxs-lookup"><span data-stu-id="69e98-126">Copy the recipient to your container.</span></span> 
    
3. <span data-ttu-id="69e98-127">Wenn die Eintrags-ID einen fremden Empfänger darstellt:</span><span class="sxs-lookup"><span data-stu-id="69e98-127">If the entry identifier represents a foreign recipient:</span></span>
    
1. <span data-ttu-id="69e98-128">Rufen Sie die [IABContainer:: CreateEntry](iabcontainer-createentry.md) -Methode ihres Containers auf, um einen neuen Empfänger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="69e98-128">Call your container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new recipient.</span></span> 
    
2. <span data-ttu-id="69e98-129">Legen Sie die anfänglichen Eigenschaften für den neuen Empfänger fest.</span><span class="sxs-lookup"><span data-stu-id="69e98-129">Set initial properties on the new recipient.</span></span>
    
4. <span data-ttu-id="69e98-130">Rufen Sie die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode des neuen Objekts auf, um Sie zu speichern.</span><span class="sxs-lookup"><span data-stu-id="69e98-130">Call the new object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it.</span></span> 
    
5. <span data-ttu-id="69e98-131">Aktualisieren Sie die Inhaltstabelle des Containers entsprechend dem neuen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="69e98-131">Update the container's contents table to reflect the new recipient.</span></span> 
    
6. <span data-ttu-id="69e98-132">Rufen [Sie IMAPISupport:: notify](imapisupport-notify.md) auf, um eine Tabellenbenachrichtigung an registrierte Clients zu senden.</span><span class="sxs-lookup"><span data-stu-id="69e98-132">Call [IMAPISupport::Notify](imapisupport-notify.md) to send a table notification to registered clients.</span></span> 
    

