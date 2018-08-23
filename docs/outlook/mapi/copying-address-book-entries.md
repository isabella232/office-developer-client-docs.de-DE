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
ms.openlocfilehash: eca0c9f63a4efaaa7f9fd066cf5dce451b8f6175
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565886"
---
# <a name="copying-address-book-entries"></a><span data-ttu-id="761e5-103">Kopieren von Adressbucheinträgen</span><span class="sxs-lookup"><span data-stu-id="761e5-103">Copying Address Book Entries</span></span>

  
  
<span data-ttu-id="761e5-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="761e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="761e5-105">[IABContainer::CopyEntries](iabcontainer-copyentries.md) -Methode des Containers wird aufgerufen, wenn eine oder mehrere Empfänger aus der gleichen oder einen anderen Container sind in diesen Container kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="761e5-105">Your container's [IABContainer::CopyEntries](iabcontainer-copyentries.md) method is called when one or more recipients from the same or another container are to be copied into this container.</span></span> <span data-ttu-id="761e5-106">**CopyEntries** hat vier Eingabeparameter: ein Array von Eintragsbezeichner, die die Empfänger zu kopierenden darstellt, die ein Fensterhandle für die Statusanzeige, einem Objektverweis Fortschritt und ein Flagwert.</span><span class="sxs-lookup"><span data-stu-id="761e5-106">**CopyEntries** has four input parameters: an array of entry identifiers representing the recipients to be copied, a window handle for the progress indicator, a progress object pointer, and a flags value.</span></span> <span data-ttu-id="761e5-107">Der Anbieter sollte Fortschritt angezeigt werden, wenn das Flag AB_NO_DIALOG nicht festgelegt ist und das Fortschritt-Objekt aus der _LpProgress_ -Parameter verwenden, wenn es nicht NULL ist.</span><span class="sxs-lookup"><span data-stu-id="761e5-107">Your provider should display progress if the AB_NO_DIALOG flag is not set and use the progress object from the  _lpProgress_ parameter if it is not NULL.</span></span> <span data-ttu-id="761e5-108">Wenn _LpProgress_ NULL ist, rufen Sie [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) zum Verwenden des MAPI-Objekts ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="761e5-108">If  _lpProgress_ is NULL, call [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) to use the MAPI progress object.</span></span> <span data-ttu-id="761e5-109">Weitere Informationen zum Anzeigen des Fortschritts finden Sie unter [eine Statusanzeige anzeigen](mapi-progress-indicators.md).</span><span class="sxs-lookup"><span data-stu-id="761e5-109">For more information about displaying progress, see [Displaying a Progress Indicator](mapi-progress-indicators.md).</span></span>
  
<span data-ttu-id="761e5-110">Zusätzlich zu AB_NO_DIALOG unterdrückt werden, eine Statusanzeige, kann eines der beiden anderen Kennzeichen auf ein doppelter Eintrag überprüfen angefordert festgelegt werden: CREATE_CHECK_DUP_LOOSE oder CREATE_CHECK_DUP_STRICT.</span><span class="sxs-lookup"><span data-stu-id="761e5-110">In addition to AB_NO_DIALOG to suppress a progress indicator, one of two other flags can be set to request a type of duplicate entry checking: CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT.</span></span> <span data-ttu-id="761e5-111">Die Flags CREATE_CHECK_DUP_LOOSE und CREATE_CHECK_DUP_STRICT sind nur Vorschläge, wie vom Dienstanbieter doppelte Einträge bestimmt und können ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="761e5-111">The CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags are only suggestions as to how your provider determines duplicate entries and can be ignored.</span></span> <span data-ttu-id="761e5-112">MAPI impliziert, dass der Anbieter Unterstützung für diese Flags wie folgt implementieren.</span><span class="sxs-lookup"><span data-stu-id="761e5-112">MAPI suggests that your provider implement support for these flags as follows.</span></span>
  
|<span data-ttu-id="761e5-113">**Doppelter Eintrag Kennzeichnung**</span><span class="sxs-lookup"><span data-stu-id="761e5-113">**Duplicate entry flag**</span></span>|<span data-ttu-id="761e5-114">**Vorgeschlagene Implementierung**</span><span class="sxs-lookup"><span data-stu-id="761e5-114">**Suggested implementation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="761e5-115">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="761e5-115">CREATE_CHECK_DUP_LOOSE</span></span>  <br/> |<span data-ttu-id="761e5-116">Überprüfen Sie, ob der Anzeigename in den Eintrag zu erstellenden den Anzeigenamen eines Eintrags bereits im Container entspricht.</span><span class="sxs-lookup"><span data-stu-id="761e5-116">Check if the display name in the entry to be created matches the display name of an entry already in the container.</span></span>  <br/> |
|<span data-ttu-id="761e5-117">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="761e5-117">CREATE_CHECK_DUP_STRICT</span></span>  <br/> |<span data-ttu-id="761e5-118">Überprüfen Sie, ob den Anzeigenamen und die suchen-Taste in den Eintrag erstellt werden mit dem Display Name, und suchen Sie Key eines Eintrags Container übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="761e5-118">Check if both the display name and the search key in the entry to be created match the display name and search key of a container entry.</span></span>  <br/> |
   
<span data-ttu-id="761e5-119">Das letzte-Flag CREATE_REPLACE, gibt an, dass der neue Eintrag vorhandenen ersetzen soll, falls es sich bei Ihrem Anbieter festgestellt hat, dass ein Eintrag erstellt werden soll ein Duplikat des Eintrags bereits in Ihrer Container ist.</span><span class="sxs-lookup"><span data-stu-id="761e5-119">The last flag, CREATE_REPLACE, indicates that the new entry should replace the existing one if your provider has determined that an entry to be created is a duplicate of an entry already in your container.</span></span> 
  
<span data-ttu-id="761e5-120">Wenn Ihr Anbieter ein persönliches Adressbuch ist, fügen Sie die **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))-Eigenschaft in jedem Kopiervorgang.</span><span class="sxs-lookup"><span data-stu-id="761e5-120">If your provider is a personal address book, include the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property in every copy operation.</span></span> <span data-ttu-id="761e5-121">Zeigt die Tabelle die Details eines Empfängers kopierten einschließlich ermöglicht den Container zum Anzeigen der Details der Empfänger und erspart den ursprünglichen Container aufrufen, um die Anzeige zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="761e5-121">Including the details display table of a copied recipient enables your container to display the details of the recipient rather than having to call the original container to create the display.</span></span>
  
 <span data-ttu-id="761e5-122">**Implementieren von IABContainer::CopyEntries**</span><span class="sxs-lookup"><span data-stu-id="761e5-122">**To implement IABContainer::CopyEntries**</span></span>
  
1. <span data-ttu-id="761e5-123">Ermitteln Sie, ob jede Eintrags-ID in der _LpEntries_ -Parameter in einem Format, die vom Dienstanbieter behandelt und wird ist dies nicht, ein Fehler auftritt und MAPI_E_INVALID_ENTRYID zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="761e5-123">Determine if each entry identifier in the  _lpEntries_ parameter is in a format that your provider handles and if it is not, fail and return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="761e5-124">Wenn eine Eintrags-ID darstellt, eine messaging-Benutzer, Verteilerliste oder Container für die Behandlung von Ihrem Anbieter:</span><span class="sxs-lookup"><span data-stu-id="761e5-124">If an entry identifier represents a messaging user, distribution list, or container that your provider handles:</span></span>
    
1. <span data-ttu-id="761e5-125">Rufen Sie eine [IMAPISupport::OpenEntry](imapisupport-openentry.md) -Methode, um den entsprechenden Empfänger zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="761e5-125">Call your [IMAPISupport::OpenEntry](imapisupport-openentry.md) method to open the corresponding recipient.</span></span> 
    
2. <span data-ttu-id="761e5-126">Kopieren Sie den Empfänger in den Container.</span><span class="sxs-lookup"><span data-stu-id="761e5-126">Copy the recipient to your container.</span></span> 
    
3. <span data-ttu-id="761e5-127">Wenn die Eintrags-ID einen fremden Empfänger darstellt:</span><span class="sxs-lookup"><span data-stu-id="761e5-127">If the entry identifier represents a foreign recipient:</span></span>
    
1. <span data-ttu-id="761e5-128">Aufrufen des Containers [IABContainer::CreateEntry](iabcontainer-createentry.md) -Methode, um einen neuen Empfänger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="761e5-128">Call your container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new recipient.</span></span> 
    
2. <span data-ttu-id="761e5-129">Festlegen von ursprünglichen Eigenschaften für den neuen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="761e5-129">Set initial properties on the new recipient.</span></span>
    
4. <span data-ttu-id="761e5-130">Rufen Sie das neue Objekt [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode, um es zu speichern.</span><span class="sxs-lookup"><span data-stu-id="761e5-130">Call the new object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it.</span></span> 
    
5. <span data-ttu-id="761e5-131">Aktualisieren Sie den Container Inhaltstabelle entsprechend den neuen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="761e5-131">Update the container's contents table to reflect the new recipient.</span></span> 
    
6. <span data-ttu-id="761e5-132">Rufen Sie [IMAPISupport::Notify](imapisupport-notify.md) , um eine Tabelle Benachrichtigung an registrierte Clients zu senden.</span><span class="sxs-lookup"><span data-stu-id="761e5-132">Call [IMAPISupport::Notify](imapisupport-notify.md) to send a table notification to registered clients.</span></span> 
    

