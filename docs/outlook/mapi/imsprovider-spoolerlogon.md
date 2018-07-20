---
title: IMSProviderSpoolerLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.SpoolerLogon
api_type:
- COM
ms.assetid: 79d5af23-efad-4013-a330-56babfb2bb0f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: eaf84e1b2a747b313f1534eb66b190d86cf89df9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792689"
---
# <a name="imsproviderspoolerlogon"></a><span data-ttu-id="eec2b-103">IMSProvider::SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="eec2b-103">IMSProvider::SpoolerLogon</span></span>

  
  
<span data-ttu-id="eec2b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eec2b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eec2b-105">Die MAPI-Warteschlange an einen Nachrichtenspeicher protokolliert.</span><span class="sxs-lookup"><span data-stu-id="eec2b-105">Logs the MAPI spooler on to a message store.</span></span>
  
```cpp
HRESULT SpoolerLogon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  LPCIID lpInterface,
  ULONG cbSpoolSecurity,
  LPBYTE lpbSpoolSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPMSLOGON FAR * lppMSLogon,
  LPMDB FAR * lppMDB     
);
```

## <a name="parameters"></a><span data-ttu-id="eec2b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eec2b-106">Parameters</span></span>

 <span data-ttu-id="eec2b-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="eec2b-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="eec2b-108">[in] Ein Zeiger auf die MAPI unterstützt Objekt für den Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="eec2b-108">[in] A pointer to the MAPI support object for the message store.</span></span>
    
 <span data-ttu-id="eec2b-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="eec2b-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="eec2b-110">[in] Ein Handle für das übergeordnete Fenster des alle Dialogfelder oder Fenster zeigt diese Methode an.</span><span class="sxs-lookup"><span data-stu-id="eec2b-110">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> 
    
 <span data-ttu-id="eec2b-111">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="eec2b-111">_lpszProfileName_</span></span>
  
> <span data-ttu-id="eec2b-112">[in] Ein Zeiger auf eine Zeichenfolge mit dem Namen des Profils, das für die Anmeldung des MAPI-Warteschlange verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eec2b-112">[in] A pointer to a string that contains the name of the profile being used for the MAPI spooler logon.</span></span> <span data-ttu-id="eec2b-113">Diese Zeichenfolge kann in Dialogfeldern angezeigt, in eine Protokolldatei geschrieben oder einfach ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="eec2b-113">This string can be displayed in dialog boxes, written out to a log file, or simply ignored.</span></span> <span data-ttu-id="eec2b-114">Es muss im Unicode-Format sein, wenn die Option MAPI_UNICODE im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="eec2b-114">It must be in Unicode format if the MAPI_UNICODE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="eec2b-115">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="eec2b-115">_cbEntryID_</span></span>
  
> <span data-ttu-id="eec2b-116">[in] Die Größe des Eintrags-ID, die auf das durch den Parameter _LpEntryID_ in Bytes.</span><span class="sxs-lookup"><span data-stu-id="eec2b-116">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="eec2b-117">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="eec2b-117">_lpEntryID_</span></span>
  
> <span data-ttu-id="eec2b-118">[in] Ein Zeiger auf die Eintrags-ID für den Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="eec2b-118">[in] A pointer to the entry identifier for the message store.</span></span> <span data-ttu-id="eec2b-119">NULL in der _LpEntryID_ -Parameter übergeben gibt an, dass ein Nachrichtenspeicher noch nicht ausgewählt wurden und Dialogfelder, mit denen den Benutzer die Auswahl ein Nachrichtenspeichers präsentiert werden können.</span><span class="sxs-lookup"><span data-stu-id="eec2b-119">Passing NULL in the  _lpEntryID_ parameter indicates that a message store has not yet been selected and that dialog boxes that enable the user to select a message store can be presented.</span></span> 
    
 <span data-ttu-id="eec2b-120">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="eec2b-120">_ulFlags_</span></span>
  
> <span data-ttu-id="eec2b-121">[in] Eine Bitmaske aus Flags, die steuert, wie die Anmeldung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eec2b-121">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="eec2b-122">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="eec2b-122">The following flags can be set:</span></span>
    
<span data-ttu-id="eec2b-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="eec2b-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="eec2b-124">Der Aufruf ist zulässig, erfolgreich ausgeführt werden kann, auch wenn das zugrunde liegende Objekt nicht an die Implementierung der aufrufenden verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="eec2b-124">The call is allowed to succeed even if the underlying object is not available to the calling implementation.</span></span> <span data-ttu-id="eec2b-125">Wenn das Objekt nicht verfügbar ist, kann ein nachfolgender Aufruf für das Objekt ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="eec2b-125">If the object is not available, a subsequent call to the object might raise an error.</span></span>
    
<span data-ttu-id="eec2b-126">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="eec2b-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="eec2b-127">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="eec2b-127">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="eec2b-128">Wenn der Parameter MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="eec2b-128">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="eec2b-129">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="eec2b-129">MDB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="eec2b-130">Verhindert die Anzeige von Dialogfeldern für die Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="eec2b-130">Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="eec2b-131">Wenn dieses Flag festgelegt ist, wird der Fehlerwert MAPI_E_LOGON_FAILED zurückgegeben, wenn die Anmeldung nicht erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="eec2b-131">If this flag is set, the error value MAPI_E_LOGON_FAILED is returned if the logon is unsuccessful.</span></span> <span data-ttu-id="eec2b-132">Wenn dieses Flag nicht festgelegt ist, kann die Nachricht Speicher-Anbieter den Benutzer an den richtigen einen Namen oder ein Kennwort, zum Einfügen von eines Datenträgers oder zum Ausführen anderer Aktionen erforderlich sind, um die Verbindung zu den Speicher auffordern.</span><span class="sxs-lookup"><span data-stu-id="eec2b-132">If this flag is not set, the message store provider can prompt the user to correct a name or password, to insert a disk, or to perform other actions necessary to establish connection to the store.</span></span>
    
<span data-ttu-id="eec2b-133">MDB_WRITE</span><span class="sxs-lookup"><span data-stu-id="eec2b-133">MDB_WRITE</span></span> 
  
> <span data-ttu-id="eec2b-134">Anfragen Lese-/Schreibberechtigung.</span><span class="sxs-lookup"><span data-stu-id="eec2b-134">Requests read/write permission.</span></span>
    
 <span data-ttu-id="eec2b-135">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="eec2b-135">_lpInterface_</span></span>
  
> <span data-ttu-id="eec2b-136">[in] Ein Zeiger auf der Benutzeroberfläche IID (Identifier) für den Nachrichtenspeicher anmelden.</span><span class="sxs-lookup"><span data-stu-id="eec2b-136">[in] A pointer to the interface identifier (IID) for the message store to log on to.</span></span> <span data-ttu-id="eec2b-137">Übergeben von NULL gibt an, dass die MAPI-Schnittstelle für den Nachrichtenspeicher ([IMsgStore](imsgstoreimapiprop.md)) zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="eec2b-137">Passing NULL indicates the MAPI interface for the message store ([IMsgStore](imsgstoreimapiprop.md)) is returned.</span></span> <span data-ttu-id="eec2b-138">Der Parameter _LpInterface_ kann auch auf einen Bezeichner für eine entsprechende Schnittstelle für den Nachrichtenspeicher (beispielsweise IID_IUnknown oder IID_IMAPIProp) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="eec2b-138">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the message store (for example IID_IUnknown or IID_IMAPIProp).</span></span> 
    
 <span data-ttu-id="eec2b-139">_cbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="eec2b-139">_cbSpoolSecurity_</span></span>
  
> <span data-ttu-id="eec2b-140">[in] Ein Zeiger auf die Größe des im Parameter _LppbSpoolSecurity_ Überprüfungsdaten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="eec2b-140">[in] A pointer to the size, in bytes, of validation data in the  _lppbSpoolSecurity_ parameter.</span></span> 
    
 <span data-ttu-id="eec2b-141">_lpbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="eec2b-141">_lpbSpoolSecurity_</span></span>
  
> <span data-ttu-id="eec2b-142">[in] Ein Zeiger auf einen Zeiger auf Überprüfungsdaten.</span><span class="sxs-lookup"><span data-stu-id="eec2b-142">[in] A pointer to a pointer to validation data.</span></span> <span data-ttu-id="eec2b-143">Die **SpoolerLogon** -Methode verwendet diese Daten zur Anmeldung bei der MAPI-Warteschlange an den gleichen Speicher als dem Anbieter für anmelden zuvor für die Anmeldung mithilfe der [IMSProvider::Logon](imsprovider-logon.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="eec2b-143">The **SpoolerLogon** method uses this data to log the MAPI spooler on to the same store as the message store provider previously logged on to by using the [IMSProvider::Logon](imsprovider-logon.md) method.</span></span> 
    
 <span data-ttu-id="eec2b-144">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="eec2b-144">_lppMAPIError_</span></span>
  
> <span data-ttu-id="eec2b-145">[out] Ein Zeiger auf einen Zeiger auf das zurückgegebene [MAPIERROR](mapierror.md) Struktur, falls vorhanden, die Angaben zu Version, Komponente und Kontext für einen Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="eec2b-145">[out] A pointer to a pointer to the returned [MAPIERROR](mapierror.md) structure, if any, that contains version, component, and context information for an error.</span></span> <span data-ttu-id="eec2b-146">Der Parameter _LppMAPIError_ kann auf NULL festgelegt werden, wenn es keine **MAPIERROR** -Struktur ist zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eec2b-146">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="eec2b-147">_lppMSLogon_</span><span class="sxs-lookup"><span data-stu-id="eec2b-147">_lppMSLogon_</span></span>
  
> <span data-ttu-id="eec2b-148">[out] Ein Zeiger auf den Zeiger auf die Nachricht speichern Objekt für die MAPI anmelden anmelden.</span><span class="sxs-lookup"><span data-stu-id="eec2b-148">[out] A pointer to the pointer to the message store logon object for MAPI to log on to.</span></span>
    
 <span data-ttu-id="eec2b-149">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="eec2b-149">_lppMDB_</span></span>
  
> <span data-ttu-id="eec2b-150">[out] Ein Zeiger auf den Zeiger auf die Nachricht speichern-Objekt für die MAPI-Warteschlange und Clientanwendungen anmelden.</span><span class="sxs-lookup"><span data-stu-id="eec2b-150">[out] A pointer to the pointer to the message store object for the MAPI spooler and client applications to log on to.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="eec2b-151">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eec2b-151">Return value</span></span>

<span data-ttu-id="eec2b-152">S_OK</span><span class="sxs-lookup"><span data-stu-id="eec2b-152">S_OK</span></span> 
  
> <span data-ttu-id="eec2b-153">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="eec2b-153">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="eec2b-154">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="eec2b-154">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="eec2b-155">Das Profil enthält nicht ausreichend Informationen für die Anmeldung für die Durchführung.</span><span class="sxs-lookup"><span data-stu-id="eec2b-155">The profile does not contain enough information for the logon to complete.</span></span> <span data-ttu-id="eec2b-156">Wenn dieser Wert zurückgegeben wird, ruft MAPI der Nachricht Informationsdienst Nachricht Service Entry Point-Funktion.</span><span class="sxs-lookup"><span data-stu-id="eec2b-156">When this value is returned, MAPI calls the message store provider's message service entry point function.</span></span>
    
<span data-ttu-id="eec2b-157">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="eec2b-157">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="eec2b-158">Der Aufruf war erfolgreich, aber der Nachricht Speicheranbieter hat Fehlerinformationen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="eec2b-158">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="eec2b-159">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="eec2b-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="eec2b-160">Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen.</span><span class="sxs-lookup"><span data-stu-id="eec2b-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="eec2b-161">Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="eec2b-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> <span data-ttu-id="eec2b-162">Wenn Sie die Fehlerinformationen vom Anbieter erhalten möchten, rufen Sie die [IMAPISession::GetLastError](imapisession-getlasterror.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="eec2b-162">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="eec2b-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eec2b-163">Remarks</span></span>

<span data-ttu-id="eec2b-164">Die MAPI-Warteschlange Ruft die **IMSProvider::SpoolerLogon** -Methode zur Anmeldung bei einem Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="eec2b-164">The MAPI spooler calls the **IMSProvider::SpoolerLogon** method to log on to a message store.</span></span> <span data-ttu-id="eec2b-165">Die MAPI-Warteschlange sollten das Nachricht Store-Objekt von der Nachricht Informationsdienst im _LppMDB_ -Parameter zurückgegeben werden, während und nach der Anmeldung verwenden.</span><span class="sxs-lookup"><span data-stu-id="eec2b-165">The MAPI spooler should use the message store object returned by the message store provider in the  _lppMDB_ parameter during and after logon.</span></span> 
  
<span data-ttu-id="eec2b-166">Aus Gründen der Konsistenz mit der [IMSProvider::Logon](imsprovider-logon.md) -Methode gibt der Anbieter auch ein Message Store Anmeldung-Objekt im Parameter _LppMSLogon_ zurück.</span><span class="sxs-lookup"><span data-stu-id="eec2b-166">For consistency with the [IMSProvider::Logon](imsprovider-logon.md) method, the provider also returns a message store logon object in the  _lppMSLogon_ parameter.</span></span> <span data-ttu-id="eec2b-167">Die Verwendung von das Store-Objekt und das Anmeldeobjekt sind für die Anmeldung üblichen Store identisch. So, dass die Objekte fungieren, als wären sie ein Objekt, das zwei Schnittstellen verfügbar macht sollte eine 1: 1-Beziehung zwischen der Anmeldung-Objekt und das Store-Objekt sein.</span><span class="sxs-lookup"><span data-stu-id="eec2b-167">The use of the store object and the logon object are identical for usual store logon; there should be a one-to-one correspondence between the logon object and the store object such that the objects act as if they are one object that exposes two interfaces.</span></span> <span data-ttu-id="eec2b-168">Die zwei Objekte werden zusammen und freigegebenen zusammen erstellt.</span><span class="sxs-lookup"><span data-stu-id="eec2b-168">The two objects are created together and freed together.</span></span> 
  
<span data-ttu-id="eec2b-169">Speicheranbieter sollten intern kennzeichnen zurückgegebene Message Store-Objekts, um anzugeben, dass der Speicher von den MAPI-Warteschlange verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eec2b-169">The store provider should internally mark the returned message store object to indicate that the store is being used by the MAPI spooler.</span></span> <span data-ttu-id="eec2b-170">Einige der Methoden für dieses Objekt Store Verhalten sich anders als für die Nachricht Clientanwendungen bereitgestellte Objekt speichern.</span><span class="sxs-lookup"><span data-stu-id="eec2b-170">Some of the methods for this store object behave differently than for the message store object provided to client applications.</span></span> <span data-ttu-id="eec2b-171">Nachhaltiger Schutz von dieser internen Mark ist am häufigsten das Verhalten, das speziell für die MAPI-Warteschlange auslösen.</span><span class="sxs-lookup"><span data-stu-id="eec2b-171">Keeping this internal mark is the most common way of triggering the behavior specific to the MAPI spooler.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eec2b-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eec2b-172">See also</span></span>



[<span data-ttu-id="eec2b-173">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="eec2b-173">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="eec2b-174">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="eec2b-174">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="eec2b-175">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eec2b-175">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

