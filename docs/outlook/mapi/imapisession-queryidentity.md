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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6b64653aa87ff7ac983409978a69f59148251d7d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583414"
---
# <a name="imapisessionqueryidentity"></a><span data-ttu-id="dea62-103">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="dea62-103">IMAPISession::QueryIdentity</span></span>

  
  
<span data-ttu-id="dea62-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dea62-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dea62-105">Gibt die Eintrags-ID des Objekts, das die primäre Identität für die Sitzung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="dea62-105">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="dea62-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dea62-106">Parameters</span></span>

 <span data-ttu-id="dea62-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="dea62-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="dea62-108">[out] Ein Zeiger auf die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LppEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="dea62-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="dea62-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="dea62-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="dea62-110">[out] Ein Zeiger auf einen Zeiger auf die Eintrags-ID des Objekts, das die primäre Identität bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="dea62-110">[out] A pointer to a pointer to the entry identifier of the object that provides the primary identity.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dea62-111">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="dea62-111">Return value</span></span>

<span data-ttu-id="dea62-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="dea62-112">S_OK</span></span> 
  
> <span data-ttu-id="dea62-113">Die primäre Identität wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dea62-113">The primary identity was successfully returned.</span></span>
    
<span data-ttu-id="dea62-114">MAPI_W_NO_SERVICE</span><span class="sxs-lookup"><span data-stu-id="dea62-114">MAPI_W_NO_SERVICE</span></span> 
  
> <span data-ttu-id="dea62-115">Der Aufruf war erfolgreich, es gibt aber keine primäre Identität für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="dea62-115">The call succeeded, but there is no primary identity for the session.</span></span> <span data-ttu-id="dea62-116">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="dea62-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="dea62-117">Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen.</span><span class="sxs-lookup"><span data-stu-id="dea62-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="dea62-118">Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="dea62-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dea62-119">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="dea62-119">Remarks</span></span>

<span data-ttu-id="dea62-120">Die **IMAPISession::QueryIdentity** -Methode die primäre Identität für die aktuelle Sitzung abgerufen und gibt den Wert über den Parameter _LppEntryID_ zurück.</span><span class="sxs-lookup"><span data-stu-id="dea62-120">The **IMAPISession::QueryIdentity** method retrieves the primary identity for the current session and returns the value through the  _lppEntryID_ parameter.</span></span> <span data-ttu-id="dea62-121">Die primäre Identität ist ein Objekt, in der Regel ein messaging-Benutzer, die den Benutzer einer Sitzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="dea62-121">The primary identity is an object, typically a messaging user, that represents the user of a session.</span></span>  <span data-ttu-id="dea62-122">_LppEntryID_ gibt die primäre Identität bei einem [IMailUser](imailuserimapiprop.md) -Objekt, das auch als-Eigenschaft [PidTagEntryID](pidtagentryid-canonical-property.md) gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="dea62-122">_lppEntryID_ returns the primary identity for an [IMailUser](imailuserimapiprop.md) object, which is also stored as the [PidTagEntryID](pidtagentryid-canonical-property.md) property.</span></span> <span data-ttu-id="dea62-123">Den Rückgabewert in _LppEntryID_ können Sie um ein **IMailUser** -Objekt mit [IMAPISession::OpenEntry](imapisession-openentry.md)zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dea62-123">You can use the value returned in  _lppEntryID_ to open an **IMailUser** object using [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span>
  
<span data-ttu-id="dea62-124">Obwohl viele Dienstanbieter in mehrere Nachrichtendienste für die die primäre Identität für eine Sitzung bereitstellen können, kennzeichnet MAPI einen einzelnen-Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="dea62-124">Although many service providers in multiple message services can provide the primary identity for a session, MAPI designates a single service provider.</span></span> <span data-ttu-id="dea62-125">Der Dienstanbieter, der die primäre Identität liefert setzt die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="dea62-125">The service provider that supplies the primary identity sets the following items:</span></span>
  
- <span data-ttu-id="dea62-126">Das Flag STATUS_PRIMARY_IDENTITY in der Eigenschaft **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dea62-126">The STATUS_PRIMARY_IDENTITY flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="dea62-127">Die Eigenschaft **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dea62-127">The **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="dea62-128">Die Eigenschaft **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dea62-128">The **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="dea62-129">Die Eigenschaft **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dea62-129">The **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="dea62-130">Zugehörigkeit der Dienstanbieter, der die primäre Identität liefert eine Message Service, legen Sie die anderen Dienstanbieter den Dienst auch die PR_IDENTITY-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dea62-130">If the service provider that supplies the primary identity belongs to a message service, the other service providers in the message service also set the PR_IDENTITY properties.</span></span> <span data-ttu-id="dea62-131">Diese Eigenschaften werden in der Sitzung Statustabelle veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="dea62-131">These properties are published in the session's status table.</span></span> 
  
<span data-ttu-id="dea62-132">Wenn möglich, gibt **QueryIdentity** den Wert für die **PR_IDENTITY_ENTRYID** -Eigenschaft aus der Statuszeile, die mit STATUS_PRIMARY_IDENTITY markiert.</span><span class="sxs-lookup"><span data-stu-id="dea62-132">If possible, **QueryIdentity** returns the value for the **PR_IDENTITY_ENTRYID** property from the status row tagged with STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="dea62-133">Wenn die **PR_IDENTITY_ENTRYID** -Eigenschaft der primäre Identitätszeile nicht vorhanden ist, gibt **QueryIdentity** eine einmaligen Eintrags-ID, die mit anderen Informationen aus dieser Zeile erstellte zurück.</span><span class="sxs-lookup"><span data-stu-id="dea62-133">If the **PR_IDENTITY_ENTRYID** property is missing from the primary identity row, **QueryIdentity** returns a one-off entry identifier built with other information from that row.</span></span> 
  
<span data-ttu-id="dea62-134">Wenn das Flag STATUS_PRIMARY_IDENTITY aller **PR_RESOURCE_FLAG** Spalten in der Tabelle "Status" nicht vorhanden ist, gibt **QueryIdentity** die erste Eintrags-ID, die es findet zurück.</span><span class="sxs-lookup"><span data-stu-id="dea62-134">If the STATUS_PRIMARY_IDENTITY flag is missing from all of the **PR_RESOURCE_FLAG** columns in the status table, **QueryIdentity** returns the first entry identifier that it finds.</span></span> <span data-ttu-id="dea62-135">Wird keine entsprechenden Eintrags-ID zurückgegeben, **QueryIdentity** erfolgreich ausgeführt wird, mit der Warnung MAPI_W_NO_SERVICE und enthält Verweise _LppEntryID_ auf einen Eintrag hartcodierte-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="dea62-135">When there is no appropriate entry identifier to return, **QueryIdentity** succeeds with the warning MAPI_W_NO_SERVICE and points  _lppEntryID_ to a hard-coded entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dea62-136">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="dea62-136">Notes to callers</span></span>

<span data-ttu-id="dea62-137">Sie können die [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) -Methode, um einer Message Service weisen Sie die Aufgabe angeben primären Identität der Sitzung aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dea62-137">You can call the [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) method to assign a message service the task of supplying the session's primary identity.</span></span> 
  
<span data-ttu-id="dea62-138">Eine andere Möglichkeit, die primäre Identität abrufen, ist suchen die Tabelle "Status" für die Zeile mit den **PR_RESOURCE_FLAGS** Spalten auf STATUS_PRIMARY_IDENTITY festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dea62-138">Another way to retrieve the primary identity is by searching the status table for the row with the **PR_RESOURCE_FLAGS** columns set to STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="dea62-139">Weitere Informationen zu dieser alternative Möglichkeit zum Abrufen von Identitätsinformationen finden Sie unter [Statustabelle und Status-Objekte](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="dea62-139">For more information about this alternate way of retrieving identity information, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  
<span data-ttu-id="dea62-140">Wenn Sie mit dem Eintrag Bezeichner für die primäre von **QueryIdentity**zurückgegebene Identität fertig sind, freigeben Sie seine Speicher durch Aufrufen der Funktion [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="dea62-140">When you are finished using the entry identifier for the primary identity returned by **QueryIdentity**, free its memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="dea62-141">Weitere Informationen zu Identität im Allgemeinen finden Sie unter [Primäre MAPI-Identität](mapi-primary-identity.md).</span><span class="sxs-lookup"><span data-stu-id="dea62-141">For more information about identity in general, see [MAPI Primary Identity](mapi-primary-identity.md).</span></span> 
  
<span data-ttu-id="dea62-142">Weitere Informationen zum Abrufen von MAPI-Sitzung Identität finden Sie unter [Abrufen von primären und Identity Provider](retrieving-primary-and-provider-identity.md).</span><span class="sxs-lookup"><span data-stu-id="dea62-142">For more information about retrieving MAPI session identity, see [Retrieving Primary and Provider Identity](retrieving-primary-and-provider-identity.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="dea62-143">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="dea62-143">MFCMAPI reference</span></span>

<span data-ttu-id="dea62-144">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="dea62-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dea62-145">**Datei**</span><span class="sxs-lookup"><span data-stu-id="dea62-145">**File**</span></span>|<span data-ttu-id="dea62-146">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="dea62-146">**Function**</span></span>|<span data-ttu-id="dea62-147">**Comment**</span><span class="sxs-lookup"><span data-stu-id="dea62-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dea62-148">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="dea62-148">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="dea62-149">CMainDlg::OnQueryIdentity</span><span class="sxs-lookup"><span data-stu-id="dea62-149">CMainDlg::OnQueryIdentity</span></span>  <br/> |<span data-ttu-id="dea62-150">MFCMAPI (engl.) verwendet die **IMAPISession::QueryIdentity** -Methode, um den Adressbuch-Adresseintrag für die primäre Identität der Sitzung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dea62-150">MFCMAPI uses the **IMAPISession::QueryIdentity** method to open the address book entry for the primary identity of the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dea62-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dea62-151">See also</span></span>



[<span data-ttu-id="dea62-152">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="dea62-152">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
  
[<span data-ttu-id="dea62-153">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="dea62-153">IMsgServiceAdmin::SetPrimaryIdentity</span></span>](imsgserviceadmin-setprimaryidentity.md)
  
[<span data-ttu-id="dea62-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="dea62-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="dea62-155">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="dea62-155">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="dea62-156">MFCMAPI als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="dea62-156">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="dea62-157">Primäre MAPI-Identität</span><span class="sxs-lookup"><span data-stu-id="dea62-157">MAPI Primary Identity</span></span>](mapi-primary-identity.md)
  
[<span data-ttu-id="dea62-158">Abrufen der primären und Anbieteridentität</span><span class="sxs-lookup"><span data-stu-id="dea62-158">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
[<span data-ttu-id="dea62-159">Verwenden von Makros zur Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="dea62-159">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)
  
[<span data-ttu-id="dea62-160">Statustabelle und Statusobjekte</span><span class="sxs-lookup"><span data-stu-id="dea62-160">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)

