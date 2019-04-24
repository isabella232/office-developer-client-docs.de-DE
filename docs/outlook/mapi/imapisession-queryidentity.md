---
title: IMAPISessionQueryIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.QueryIdentity
api_type:
- COM
ms.assetid: a2cdda90-5457-49a7-b98c-7273ffe5cbbc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 396320c6b39553da09aa1f45d0c755f40a939382
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335693"
---
# <a name="imapisessionqueryidentity"></a><span data-ttu-id="b7ed5-103">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="b7ed5-103">IMAPISession::QueryIdentity</span></span>

  
  
<span data-ttu-id="b7ed5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7ed5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7ed5-105">Gibt den Eintragsbezeichner des Objekts zurück, das die primäre Identität für die Sitzung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-105">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="b7ed5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7ed5-106">Parameters</span></span>

 <span data-ttu-id="b7ed5-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b7ed5-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="b7ed5-108">Out Ein Zeiger auf die Bytezahl in der Eintrags-ID, auf die durch den _lppEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b7ed5-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="b7ed5-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="b7ed5-110">Out Ein Zeiger auf einen Zeiger auf die Eintrags-ID des Objekts, das die primäre Identität bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-110">[out] A pointer to a pointer to the entry identifier of the object that provides the primary identity.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b7ed5-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7ed5-111">Return value</span></span>

<span data-ttu-id="b7ed5-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="b7ed5-112">S_OK</span></span> 
  
> <span data-ttu-id="b7ed5-113">Die primäre Identität wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-113">The primary identity was successfully returned.</span></span>
    
<span data-ttu-id="b7ed5-114">MAPI_W_NO_SERVICE</span><span class="sxs-lookup"><span data-stu-id="b7ed5-114">MAPI_W_NO_SERVICE</span></span> 
  
> <span data-ttu-id="b7ed5-115">Der Aufruf war erfolgreich, aber es gibt keine primäre Identität für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-115">The call succeeded, but there is no primary identity for the session.</span></span> <span data-ttu-id="b7ed5-116">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="b7ed5-117">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="b7ed5-118">Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="b7ed5-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b7ed5-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7ed5-119">Remarks</span></span>

<span data-ttu-id="b7ed5-120">Die **IMAPISession:: QueryIdentity** -Methode ruft die primäre Identität für die aktuelle Sitzung ab und gibt den Wert über den _lppEntryID_ -Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-120">The **IMAPISession::QueryIdentity** method retrieves the primary identity for the current session and returns the value through the  _lppEntryID_ parameter.</span></span> <span data-ttu-id="b7ed5-121">Die primäre Identität ist ein Objekt, in der Regel ein Messagingbenutzer, der den Benutzer einer Sitzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-121">The primary identity is an object, typically a messaging user, that represents the user of a session.</span></span>  <span data-ttu-id="b7ed5-122">_lppEntryID_ gibt die primäre Identität für ein [IMailUser](imailuserimapiprop.md) -Objekt zurück, das auch als [PidTagEntryID](pidtagentryid-canonical-property.md) -Eigenschaft gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-122">_lppEntryID_ returns the primary identity for an [IMailUser](imailuserimapiprop.md) object, which is also stored as the [PidTagEntryID](pidtagentryid-canonical-property.md) property.</span></span> <span data-ttu-id="b7ed5-123">Sie können den in _lppEntryID_ zurückgegebenen Wert verwenden, um ein **IMailUser** -Objekt mit [IMAPISession:: OpenEntry](imapisession-openentry.md)zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-123">You can use the value returned in  _lppEntryID_ to open an **IMailUser** object using [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span>
  
<span data-ttu-id="b7ed5-124">Obwohl viele Dienstanbieter in mehreren Nachrichtendiensten die primäre Identität für eine Sitzung bereitstellen können, benennt MAPI einen einzelnen Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-124">Although many service providers in multiple message services can provide the primary identity for a session, MAPI designates a single service provider.</span></span> <span data-ttu-id="b7ed5-125">Der Dienstanbieter, der die primäre Identität bereitstellt, legt die folgenden Elemente fest:</span><span class="sxs-lookup"><span data-stu-id="b7ed5-125">The service provider that supplies the primary identity sets the following items:</span></span>
  
- <span data-ttu-id="b7ed5-126">Das STATUS_PRIMARY_IDENTITY-Flag in der **PR_RESOURCE_FLAGS** ([pidtagresourceflags (](pidtagresourceflags-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-126">The STATUS_PRIMARY_IDENTITY flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="b7ed5-127">Die **PR_IDENTITY_DISPLAY** ([pidtagidentitydisplay (](pidtagidentitydisplay-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-127">The **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="b7ed5-128">Die **PR_IDENTITY_ENTRYID** ([pidtagidentityentryid (](pidtagidentityentryid-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-128">The **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="b7ed5-129">Die **PR_IDENTITY_SEARCH_KEY** ([pidtagidentitysearchkey (](pidtagidentitysearchkey-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-129">The **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="b7ed5-130">Wenn der Dienstanbieter, der die primäre Identität bereitstellt, zu einem Nachrichtendienst gehört, legen die anderen Dienstanbieter im Nachrichtendienst auch die PR_IDENTITY-Eigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-130">If the service provider that supplies the primary identity belongs to a message service, the other service providers in the message service also set the PR_IDENTITY properties.</span></span> <span data-ttu-id="b7ed5-131">Diese Eigenschaften werden in der Statustabelle der Sitzung veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-131">These properties are published in the session's status table.</span></span> 
  
<span data-ttu-id="b7ed5-132">Wenn möglich, gibt **QueryIdentity** den Wert für die **PR_IDENTITY_ENTRYID** -Eigenschaft aus der Zeile Status mit STATUS_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-132">If possible, **QueryIdentity** returns the value for the **PR_IDENTITY_ENTRYID** property from the status row tagged with STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="b7ed5-133">Wenn die **PR_IDENTITY_ENTRYID** -Eigenschaft in der primären Identitätszeile fehlt, gibt **QueryIdentity** einen einmaligen Eintragsbezeichner zurück, der mit anderen Informationen aus dieser Zeile erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-133">If the **PR_IDENTITY_ENTRYID** property is missing from the primary identity row, **QueryIdentity** returns a one-off entry identifier built with other information from that row.</span></span> 
  
<span data-ttu-id="b7ed5-134">Wenn das STATUS_PRIMARY_IDENTITY-Flag in allen **PR_RESOURCE_FLAG** -Spalten in der Status-Tabelle fehlt, gibt **QueryIdentity** den ersten gefundenen Eintragsbezeichner zurück.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-134">If the STATUS_PRIMARY_IDENTITY flag is missing from all of the **PR_RESOURCE_FLAG** columns in the status table, **QueryIdentity** returns the first entry identifier that it finds.</span></span> <span data-ttu-id="b7ed5-135">Wenn kein entsprechender Eingabe Bezeichner vorhanden ist, wird **QueryIdentity** mit der Warnung MAPI_W_NO_SERVICE und _lppEntryID_ auf eine hart codierte Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-135">When there is no appropriate entry identifier to return, **QueryIdentity** succeeds with the warning MAPI_W_NO_SERVICE and points  _lppEntryID_ to a hard-coded entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b7ed5-136">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="b7ed5-136">Notes to callers</span></span>

<span data-ttu-id="b7ed5-137">Sie können die [IMsgServiceAdmin:: SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) -Methode aufrufen, um einem Nachrichtendienst die Aufgabe zuzuweisen, die primäre Identität der Sitzung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-137">You can call the [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) method to assign a message service the task of supplying the session's primary identity.</span></span> 
  
<span data-ttu-id="b7ed5-138">Eine weitere Möglichkeit zum Abrufen der primären Identität besteht darin, die Statustabelle für die Zeile zu durchsuchen, wobei die **PR_RESOURCE_FLAGS** -Spalten auf STATUS_PRIMARY_IDENTITY festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-138">Another way to retrieve the primary identity is by searching the status table for the row with the **PR_RESOURCE_FLAGS** columns set to STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="b7ed5-139">Weitere Informationen zu diesem alternativen Verfahren zum Abrufen von Identitätsinformationen finden Sie unter [Status Table-und Status-Objekte](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="b7ed5-139">For more information about this alternate way of retrieving identity information, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  
<span data-ttu-id="b7ed5-140">Wenn Sie die Eintrags-ID für die primäre von **QueryIdentity**zurückgegebene Identität nicht mehr verwenden möchten, müssen Sie den Speicher freigeben, indem Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-140">When you are finished using the entry identifier for the primary identity returned by **QueryIdentity**, free its memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="b7ed5-141">Weitere Informationen zur Identität im Allgemeinen finden Sie unter [MAPI Primary Identity](mapi-primary-identity.md).</span><span class="sxs-lookup"><span data-stu-id="b7ed5-141">For more information about identity in general, see [MAPI Primary Identity](mapi-primary-identity.md).</span></span> 
  
<span data-ttu-id="b7ed5-142">Weitere Informationen zum Abrufen der MAPI-Sitzungs Identität finden Sie unter [Abrufen der primären und Anbieter Identität](retrieving-primary-and-provider-identity.md).</span><span class="sxs-lookup"><span data-stu-id="b7ed5-142">For more information about retrieving MAPI session identity, see [Retrieving Primary and Provider Identity](retrieving-primary-and-provider-identity.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b7ed5-143">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="b7ed5-143">MFCMAPI reference</span></span>

<span data-ttu-id="b7ed5-144">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b7ed5-145">**Datei**</span><span class="sxs-lookup"><span data-stu-id="b7ed5-145">**File**</span></span>|<span data-ttu-id="b7ed5-146">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="b7ed5-146">**Function**</span></span>|<span data-ttu-id="b7ed5-147">**Comment**</span><span class="sxs-lookup"><span data-stu-id="b7ed5-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b7ed5-148">MainDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="b7ed5-148">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="b7ed5-149">CMainDlg:: OnQueryIdentity</span><span class="sxs-lookup"><span data-stu-id="b7ed5-149">CMainDlg::OnQueryIdentity</span></span>  <br/> |<span data-ttu-id="b7ed5-150">MFCMAPI verwendet die **IMAPISession:: QueryIdentity** -Methode, um den Adressbucheintrag für die primäre Identität der Sitzung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b7ed5-150">MFCMAPI uses the **IMAPISession::QueryIdentity** method to open the address book entry for the primary identity of the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b7ed5-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7ed5-151">See also</span></span>



[<span data-ttu-id="b7ed5-152">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="b7ed5-152">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
  
[<span data-ttu-id="b7ed5-153">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="b7ed5-153">IMsgServiceAdmin::SetPrimaryIdentity</span></span>](imsgserviceadmin-setprimaryidentity.md)
  
[<span data-ttu-id="b7ed5-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b7ed5-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b7ed5-155">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b7ed5-155">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="b7ed5-156">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="b7ed5-156">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="b7ed5-157">Primäre MAPI-Identität</span><span class="sxs-lookup"><span data-stu-id="b7ed5-157">MAPI Primary Identity</span></span>](mapi-primary-identity.md)
  
[<span data-ttu-id="b7ed5-158">Abrufen der primären und Anbieter Identität</span><span class="sxs-lookup"><span data-stu-id="b7ed5-158">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
[<span data-ttu-id="b7ed5-159">Verwenden von Makros zur Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="b7ed5-159">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)
  
[<span data-ttu-id="b7ed5-160">Statustabelle und Statusobjekte</span><span class="sxs-lookup"><span data-stu-id="b7ed5-160">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)

