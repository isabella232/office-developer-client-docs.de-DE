---
title: IAddrBookOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.OpenEntry
api_type:
- COM
ms.assetid: bd7746f4-8070-4cc5-8b8e-c527c5847545
description: 'Letzte �nderung: Freitag, 1. Februar 2013'
ms.openlocfilehash: 293fe5a65c760f61ab0073e0eafc1a606c69050f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287021"
---
# <a name="iaddrbookopenentry"></a><span data-ttu-id="7bf53-103">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="7bf53-103">IAddrBook::OpenEntry</span></span>

<span data-ttu-id="7bf53-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7bf53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7bf53-105">Öffnet einen Adressbucheintrag und gibt einen Zeiger auf eine Schnittstelle zurück, die für den Zugriff auf den Eintrag verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7bf53-105">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="7bf53-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bf53-106">Parameters</span></span>

<span data-ttu-id="7bf53-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="7bf53-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="7bf53-108">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7bf53-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="7bf53-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="7bf53-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="7bf53-110">in Ein Zeiger auf die Eintrags-ID, die den zu öffnenden Adressbucheintrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="7bf53-110">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
<span data-ttu-id="7bf53-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="7bf53-111">_lpInterface_</span></span>
  
> <span data-ttu-id="7bf53-112">in Ein Zeiger auf die Schnittstellen-ID (IID) der Schnittstelle, die für den Zugriff auf den geöffneten Eintrag verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7bf53-112">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="7bf53-113">Durch das Übergeben von NULL wird die Standardschnittstelle des Objekts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7bf53-113">Passing NULL returns the object's standard interface.</span></span> <span data-ttu-id="7bf53-114">Für Messagingbenutzer ist die Standardschnittstelle [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="7bf53-114">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="7bf53-115">Für Verteilerlisten ist es [IDistList: IMAPIContainer](idistlistimapicontainer.md) und für Container ist es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="7bf53-115">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md) and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="7bf53-116">Anrufer können _lpInterface_ auf die entsprechende Standardschnittstelle oder eine Schnittstelle in der Vererbungshierarchie festlegen.</span><span class="sxs-lookup"><span data-stu-id="7bf53-116">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
<span data-ttu-id="7bf53-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7bf53-117">_ulFlags_</span></span>
  
> <span data-ttu-id="7bf53-118">in Eine Bitmaske von Flags, die steuert, wie der Eintrag geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="7bf53-118">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="7bf53-119">Die folgenden Flags können festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7bf53-119">The following flags can be set.</span></span>
    
<span data-ttu-id="7bf53-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="7bf53-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="7bf53-121">Fordert, dass der Eintrag mit den maximal zulässigen Netzwerk-und Clientberechtigungen geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="7bf53-121">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="7bf53-122">Wenn der Client beispielsweise über Lese-/Schreibzugriff verfügt, sollte der Adressbuchanbieter versuchen, den Eintrag mit Berechtigung zum Lesen/Schreiben zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7bf53-122">For example, if the client has read/write permission, the address book provider should attempt to open the entry with read/write permission.</span></span> <span data-ttu-id="7bf53-123">Der Client kann die Zugriffsebene abrufen, die durch Aufrufen der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des Open-Eintrags und Abrufen der **PR_ACCESS_LEVEL** ([pidtagaccesslevel (](pidtagaccesslevel-canonical-property.md))-Eigenschaft erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="7bf53-123">The client can retrieve the access level that was granted by calling the open entry's [IMAPIProp::GetProps](imapiprop-getprops.md) method and retrieving the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="7bf53-124">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="7bf53-124">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="7bf53-125">Öffnet einen Adressbucheintrag und greift nur über den Cache auf ihn zu.</span><span class="sxs-lookup"><span data-stu-id="7bf53-125">Opens an address book entry and accesses it only from the cache.</span></span> <span data-ttu-id="7bf53-126">Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung die globale Adressliste (GAL) im Exchange-Cache-Modus zu öffnen und auf einen Eintrag in diesem Adressbuch aus dem Cache zuzugreifen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7bf53-126">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="7bf53-127">Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7bf53-127">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="7bf53-128">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="7bf53-128">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="7bf53-129">Der Aufruf kann erfolgreich ausgeführt werden, bevor der Eintrag vollständig geöffnet und verfügbar ist, was bedeutet, dass spätere Aufrufe des Eintrags möglicherweise einen Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="7bf53-129">Allows the call to succeed, potentially before the entry is fully open and available, implying that later calls to the entry might return an error.</span></span>
    
<span data-ttu-id="7bf53-130">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="7bf53-130">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="7bf53-131">Verwenden Sie nur die GAL zum Durchführen der Namensauflösung.</span><span class="sxs-lookup"><span data-stu-id="7bf53-131">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="7bf53-132">Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7bf53-132">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="7bf53-133">Der _ulFlags_ -MAPI_GAL_ONLY ist möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben, in diesem Fall können Sie ihn mithilfe des folgenden Werts zu Ihrem Code hinzufügen: >`#define MAPI_GAL_ONLY (0x00000080)`</span><span class="sxs-lookup"><span data-stu-id="7bf53-133">The  _ulFlags_ MAPI_GAL_ONLY might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define MAPI_GAL_ONLY (0x00000080)`</span></span>
  
<span data-ttu-id="7bf53-134">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="7bf53-134">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="7bf53-135">Fordert, dass der Eintrag mit Lese-/Schreibzugriff geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="7bf53-135">Requests that the entry be opened with read/write permission.</span></span> <span data-ttu-id="7bf53-136">Da Einträge standardmäßig mit schreibgeschütztem Zugriff geöffnet werden, sollten Clients nicht davon ausgehen, dass Lese-/Schreibzugriff erteilt wurde, unabhängig davon, ob MAPI_MODIFY festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7bf53-136">Because entries are opened with read-only access by default, clients should not assume that read/write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="7bf53-137">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="7bf53-137">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="7bf53-138">Verwenden Sie das Offlineadressbuch nicht zum Ausführen der Namensauflösung.</span><span class="sxs-lookup"><span data-stu-id="7bf53-138">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="7bf53-139">Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7bf53-139">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="7bf53-140">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="7bf53-140">_lpulObjType_</span></span>
  
> <span data-ttu-id="7bf53-141">Out Ein Zeiger auf den Typ des geöffneten Eintrags.</span><span class="sxs-lookup"><span data-stu-id="7bf53-141">[out] A pointer to the type of the opened entry.</span></span>
    
<span data-ttu-id="7bf53-142">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="7bf53-142">_lppUnk_</span></span>
  
> <span data-ttu-id="7bf53-143">Out Ein Zeiger auf einen Zeiger auf den geöffneten Eintrag.</span><span class="sxs-lookup"><span data-stu-id="7bf53-143">[out] A pointer to a pointer to the opened entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7bf53-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7bf53-144">Return value</span></span>

<span data-ttu-id="7bf53-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="7bf53-145">S_OK</span></span> 
  
> <span data-ttu-id="7bf53-146">Der Eintrag wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="7bf53-146">The entry was successfully opened.</span></span>
    
<span data-ttu-id="7bf53-147">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="7bf53-147">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="7bf53-148">Es wurde versucht, einen Eintrag zu öffnen, für den der Benutzer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="7bf53-148">An attempt was made to open an entry for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="7bf53-149">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="7bf53-149">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="7bf53-150">Der durch _lpEntryID_ dargestellte Eintrag ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7bf53-150">The entry represented by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="7bf53-151">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7bf53-151">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="7bf53-152">Die in _lpEntryID_ angegebene Eintrags-ID wird nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="7bf53-152">The entry identifier specified in  _lpEntryID_ is not recognized.</span></span> <span data-ttu-id="7bf53-153">Dieser Wert wird in der Regel zurückgegeben, wenn der für den entsprechenden Eintrag zuständige Adressbuchanbieter nicht geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="7bf53-153">This value is typically returned if the address book provider responsible for the corresponding entry is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7bf53-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7bf53-154">Remarks</span></span>

<span data-ttu-id="7bf53-155">Clients und Dienstanbieter rufen die **IAddrBook:: OpenEntry** -Methode auf, um einen Adressbucheintrag zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7bf53-155">Clients and service providers call the **IAddrBook::OpenEntry** method to open an address book entry.</span></span> <span data-ttu-id="7bf53-156">MAPI leitet den Anruf an den entsprechenden Adressbuchanbieter weiter, basierend auf der [MAPIUID](mapiuid.md) -Struktur, die in der im _lpEntryID_ -Parameter übergebenen Eintrags-ID enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="7bf53-156">MAPI forwards the call to the appropriate address book provider, based on the [MAPIUID](mapiuid.md) structure included in the entry identifier passed in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="7bf53-157">Der Adressbuchanbieter öffnet den Eintrag schreibgeschützt, es sei denn, das MAPI_MODIFY-oder MAPI_BEST_ACCESS-Flag im _ulFlags_ -Parameter ist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7bf53-157">The address book provider opens the entry as read-only unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter is set.</span></span> <span data-ttu-id="7bf53-158">Diese Flags sind jedoch Vorschläge.</span><span class="sxs-lookup"><span data-stu-id="7bf53-158">However, these flags are suggestions.</span></span> <span data-ttu-id="7bf53-159">Wenn der Adressbuchanbieter die Änderung für den angeforderten Eintrag nicht zulässt, wird MAPI_E_NO_ACCESS zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7bf53-159">If the address book provider does not allow modification for the entry requested, it returns MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="7bf53-160">Der Parameter _lpInterface_ gibt an, welche Schnittstelle für den Zugriff auf den geöffneten Eintrag verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7bf53-160">The  _lpInterface_ parameter indicates which interface should be used to access the opened entry.</span></span> <span data-ttu-id="7bf53-161">Durch das Übergeben von NULL in _lpInterface_ wird angegeben, dass die standardmäßige MAPI-Schnittstelle für diesen Eintragstyp verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7bf53-161">Passing NULL in  _lpInterface_ indicates the standard MAPI interface for that type of entry should be used.</span></span> <span data-ttu-id="7bf53-162">Da der Adressbuchanbieter eine andere Schnittstelle als die vom _lpInterface_ -Parameter vorgeschlagene zurückgeben kann, sollte der Aufrufer den im _lpulObjType_ -Parameter zurückgegebenen Wert überprüfen, um zu bestimmen, ob der zurückgegebene Objekttyp erwartete.</span><span class="sxs-lookup"><span data-stu-id="7bf53-162">Because the address book provider might return a different interface than the one suggested by the  _lpInterface_ parameter, the caller should check the value returned in the  _lpulObjType_ parameter to determine whether the object type returned is what was expected.</span></span> <span data-ttu-id="7bf53-163">Wenn der Objekttyp nicht vom erwarteten Typ ist, kann der Aufrufer den Parameter _lppUnk_ in einen geeigneten Typ umwandeln.</span><span class="sxs-lookup"><span data-stu-id="7bf53-163">If the object type is not of the type expected, the caller can cast the  _lppUnk_ parameter to a type that is more appropriate.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7bf53-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7bf53-164">See also</span></span>

- [<span data-ttu-id="7bf53-165">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7bf53-165">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

