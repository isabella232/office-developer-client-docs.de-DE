---
title: HrOpenABEntryWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83821a86-abff-460c-bb8e-9fd9d232dc6b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 20344185ffcbd90017fa3c3493218bd9b3ddfd74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408894"
---
# <a name="hropenabentrywithprovideruid"></a><span data-ttu-id="ee189-103">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="ee189-103">HrOpenABEntryWithProviderUID</span></span>

  
  
<span data-ttu-id="ee189-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee189-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee189-105">Öffnet die **Eintrags** -Nr. mit dem von _PEmsabpUID_identifizierten Exchange-Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="ee189-105">Opens the **entryID** using the Exchange Address Book identified by  _pEmsabpUID_.</span></span> <span data-ttu-id="ee189-106">Diese Funktion funktioniert ähnlich wie [IAddrBook:: OpenEntry](iaddrbook-openentry.md) , mit der Ausnahme, dass mit dieser Funktion sichergestellt wird, dass [IAddrBook:: OpenEntry](iaddrbook-openentry.md) unter Verwendung des erwarteten Exchange-Adressbuch Anbieters geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="ee189-106">This function works similarly to [IAddrBook::OpenEntry](iaddrbook-openentry.md) except that using this function ensures that [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ee189-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ee189-107">Header file:</span></span>  <br/> |<span data-ttu-id="ee189-108">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="ee189-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="ee189-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="ee189-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="ee189-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="ee189-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="ee189-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="ee189-111">Called by:</span></span>  <br/> |<span data-ttu-id="ee189-112">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="ee189-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithProviderUID(
  const MAPIUID *pEmsabpUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="ee189-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee189-113">Parameters</span></span>

 <span data-ttu-id="ee189-114">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="ee189-114">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="ee189-115">in Ein Zeiger auf ein **emsmdbUID** , das den Exchange-Dienst identifiziert, der den Exchange-Adressbuchanbieter enthält, den diese Funktion verwenden sollte, um Details zur Eintrags-ID anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ee189-115">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="ee189-116">Wenn die ID des eingehenden Eintrags kein Exchange-Adressbuchanbieter ist, wird dieser Parameter ignoriert, und der Funktionsaufruf verhält sich wie [IAddrBook::D ails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="ee189-116">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="ee189-117">Wenn dieser Parameter NULL oder eine NULL-MAPIUID ist, verhält sich diese Funktion wie [IAddrBook::D ails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="ee189-117">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="ee189-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="ee189-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="ee189-119">in Das zum Öffnen des Eintrags Bezeichners verwendete Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="ee189-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="ee189-120">Er darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="ee189-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="ee189-121">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ee189-121">_cbEntryID_</span></span>
  
> <span data-ttu-id="ee189-122">in Die Bytezahl der vom _lpEntryID_ -Parameter angegebenen Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="ee189-122">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ee189-123">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="ee189-123">_lpEntryID_</span></span>
  
>  <span data-ttu-id="ee189-124">in Ein Zeiger auf die Eintrags-ID, die den zu öffnenden Adressbucheintrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="ee189-124">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="ee189-125">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="ee189-125">_lpInterface_</span></span>
  
> <span data-ttu-id="ee189-126">in Ein Zeiger auf die Schnittstellen-ID (IID) der Schnittstelle, die für den Zugriff auf den geöffneten Eintrag verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ee189-126">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="ee189-127">Beim Übergeben von NULL wird die Standardschnittstelle des Objekts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ee189-127">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="ee189-128">Für Messagingbenutzer ist die Standardschnittstelle [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="ee189-128">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="ee189-129">Für Verteilerlisten ist es [IDistList: IMAPIContainer](idistlistimapicontainer.md)und für Container ist es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="ee189-129">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="ee189-130">Anrufer können _lpInterface_ auf die entsprechende Standardschnittstelle oder eine Schnittstelle in der Vererbungshierarchie festlegen.</span><span class="sxs-lookup"><span data-stu-id="ee189-130">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="ee189-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ee189-131">_ulFlags_</span></span>
  
> <span data-ttu-id="ee189-132">in Eine Bitmaske von Flags, die das Öffnen des Eintrags steuert, können die folgenden Flags festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="ee189-132">[in] A bitmask of flags that controls the how the entry is opened, The following flags can be set:</span></span>
    
<span data-ttu-id="ee189-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ee189-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="ee189-134">Fordert, dass der Eintrag mit den maximal zulässigen Netzwerk-und Clientberechtigungen geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="ee189-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="ee189-135">Wenn der Client beispielsweise über Lese-und Schreibberechtigungen verfügt, versucht der Adressbuchanbieter, den Eintrag mit Lese-und Schreibberechtigung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ee189-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="ee189-136">Der Client kann die Zugriffsebene abrufen, die durch Aufrufen der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des geöffneten Eintrags und Abrufen der PR_ACCESS_LEVEL (pidtagaccesslevel ()-Eigenschaft erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="ee189-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="ee189-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="ee189-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="ee189-138">Verwenden Sie nur das Offlineadressbuch, um die Namensauflösung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="ee189-138">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="ee189-139">Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung die globale Adressliste (GAL) im Exchange-Cache-Modus zu öffnen und auf einen Eintrag in diesem Adressbuch aus dem Cache zuzugreifen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ee189-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="ee189-140">Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ee189-140">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="ee189-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="ee189-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="ee189-142">Der Aufruf kann erfolgreich ausgeführt werden, bevor der Eintrag vollständig geöffnet und verfügbar ist, was bedeutet, dass nachfolgende Aufrufe des Eintrags möglicherweise einen Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ee189-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="ee189-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="ee189-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="ee189-144">Verwenden Sie nur die GAL zum Durchführen der Namensauflösung.</span><span class="sxs-lookup"><span data-stu-id="ee189-144">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="ee189-145">Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ee189-145">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="ee189-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="ee189-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="ee189-147">Fordert, dass der Eintrag mit Lese-und Schreibberechtigung geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="ee189-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="ee189-148">Da Einträge standardmäßig mit schreibgeschütztem Zugriff geöffnet werden, sollten Clients nicht davon ausgehen, dass Lese-und Schreibberechtigungen erteilt wurden, unabhängig davon, ob MAPI_MODIFY festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ee189-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="ee189-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="ee189-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="ee189-150">Verwenden Sie das Offlineadressbuch nicht zum Ausführen der Namensauflösung.</span><span class="sxs-lookup"><span data-stu-id="ee189-150">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="ee189-151">Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ee189-151">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="ee189-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="ee189-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="ee189-153">Out Ein Zeiger auf den Typ des geöffneten Eintrags.</span><span class="sxs-lookup"><span data-stu-id="ee189-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="ee189-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="ee189-154">_lppUnk_</span></span>
  
> <span data-ttu-id="ee189-155">Out Ein Zeiger auf einen Zeiger des geöffneten Eintrags.</span><span class="sxs-lookup"><span data-stu-id="ee189-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

