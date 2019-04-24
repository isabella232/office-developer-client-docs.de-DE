---
title: HrOpenABEntryWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b640a5aa-4e36-4983-bf11-9428809e830b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 415d108f7fd9e84ba2a9090658bc0923550390f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347789"
---
# <a name="hropenabentrywithexchangecontext"></a><span data-ttu-id="61567-103">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="61567-103">HrOpenABEntryWithExchangeContext</span></span>

  
  
<span data-ttu-id="61567-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61567-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61567-105">Öffnet die **Eintrags** -Nr. mit dem von **PEmsmdbUID**identifizierten Exchange-Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="61567-105">Opens the **entryID** using the Exchange Address Book identified by **pEmsmdbUID**.</span></span> <span data-ttu-id="61567-106">Diese Funktion funktioniert ähnlich wie [IAddrBook::D ails](iaddrbook-details.md) , mit der Ausnahme, dass mit dieser Funktion sichergestellt wird, dass der [IAddrBook:: OpenEntry](iaddrbook-openentry.md) mithilfe des erwarteten Exchange-Adressbuch Anbieters geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="61567-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) except that using this function ensures that the [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book Provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="61567-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="61567-107">Header file:</span></span>  <br/> |<span data-ttu-id="61567-108">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="61567-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="61567-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="61567-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="61567-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="61567-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="61567-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="61567-111">Called by:</span></span>  <br/> |<span data-ttu-id="61567-112">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="61567-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDoABDetailsWithExchangeContext(
  LPMAPISESSION pmsess,
  const MAPIUID *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="61567-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="61567-113">Parameters</span></span>

 <span data-ttu-id="61567-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="61567-114">_pmsess_</span></span>
  
> <span data-ttu-id="61567-115">in Der angemeldete **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="61567-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="61567-116">Er darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="61567-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="61567-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="61567-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="61567-118">in Ein Zeiger auf ein **emsmdbUID** , das den Exchange-Dienst identifiziert, der den Exchange-Adressbuchanbieter enthält, den diese Funktion verwenden sollte, um Details zur Eintrags-ID anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="61567-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="61567-119">Wenn die ID des eingehenden Eintrags kein Exchange-Adressbuchanbieter ist, wird dieser Parameter ignoriert, und der Funktionsaufruf verhält sich wie [IAddrBook::D ails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="61567-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="61567-120">Wenn dieser Parameter NULL oder eine NULL-MAPIUID ist, verhält sich diese Funktion wie [IAddrBook::D ails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="61567-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="61567-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="61567-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="61567-122">in Das zum Öffnen des Eintrags Bezeichners verwendete Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="61567-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="61567-123">Er darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="61567-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="61567-124">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="61567-124">_cbEntryID_</span></span>
  
> <span data-ttu-id="61567-125">in Die Bytezahl der vom _lpEntryID_ -Parameter angegebenen Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="61567-125">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="61567-126">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="61567-126">_lpEntryID_</span></span>
  
>  <span data-ttu-id="61567-127">in Ein Zeiger auf die Eintrags-ID, die den zu öffnenden Adressbucheintrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="61567-127">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="61567-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="61567-128">_ulFlags_</span></span>
  
> <span data-ttu-id="61567-129">in Eine Bitmaske von Flags, die steuert, wie der Eintrag geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="61567-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="61567-130">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="61567-130">The following flags can be set:</span></span>
    
<span data-ttu-id="61567-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="61567-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="61567-132">Fordert, dass der Eintrag mit den maximal zulässigen Netzwerk-und Clientberechtigungen geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="61567-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="61567-133">Wenn der Client beispielsweise über Lese-und Schreibberechtigungen verfügt, versucht der Adressbuchanbieter, den Eintrag mit Lese-und Schreibberechtigung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="61567-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="61567-134">Der Client kann die Zugriffsebene abrufen, die durch Aufrufen der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des geöffneten Eintrags und Abrufen der PR_ACCESS_LEVEL (pidtagaccesslevel ()-Eigenschaft erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="61567-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="61567-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="61567-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="61567-136">Verwendet nur das Offlineadressbuch zum Durchführen der Namensauflösung.</span><span class="sxs-lookup"><span data-stu-id="61567-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="61567-137">Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung die globale Adressliste (GAL) im Exchange-Cache-Modus zu öffnen und auf einen Eintrag in diesem Adressbuch aus dem Cache zuzugreifen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="61567-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="61567-138">Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="61567-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="61567-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="61567-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="61567-140">Der Aufruf kann erfolgreich ausgeführt werden, bevor der Eintrag vollständig geöffnet und verfügbar ist, was bedeutet, dass nachfolgende Aufrufe des Eintrags möglicherweise einen Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="61567-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="61567-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="61567-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="61567-142">Verwendet nur die GAL zur Namensauflösung.</span><span class="sxs-lookup"><span data-stu-id="61567-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="61567-143">Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="61567-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="61567-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="61567-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="61567-145">Fordert, dass der Eintrag mit Lese-und Schreibberechtigung geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="61567-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="61567-146">Da Einträge standardmäßig mit schreibgeschütztem Zugriff geöffnet werden, sollten Clients nicht davon ausgehen, dass Lese-und Schreibberechtigungen erteilt wurden, unabhängig davon, ob MAPI_MODIFY festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="61567-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="61567-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="61567-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="61567-148">Das Offlineadressbuch wird nicht zum Durchführen der Namensauflösung verwendet.</span><span class="sxs-lookup"><span data-stu-id="61567-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="61567-149">Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="61567-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    

