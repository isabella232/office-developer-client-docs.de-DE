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
ms.openlocfilehash: 794674df38266743cac8c947ec93dc1fcfff438b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430574"
---
# <a name="imsproviderspoolerlogon"></a><span data-ttu-id="4fb4a-103">IMSProvider::SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="4fb4a-103">IMSProvider::SpoolerLogon</span></span>

  
  
<span data-ttu-id="4fb4a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fb4a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fb4a-105">Protokolliert den MAPI-Spooler bei einem Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-105">Logs the MAPI spooler on to a message store.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="4fb4a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4fb4a-106">Parameters</span></span>

 <span data-ttu-id="4fb4a-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="4fb4a-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="4fb4a-108">[in] Ein Zeiger auf das MAPI-Unterstützungsobjekt für den Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-108">[in] A pointer to the MAPI support object for the message store.</span></span>
    
 <span data-ttu-id="4fb4a-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="4fb4a-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="4fb4a-110">[in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-110">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> 
    
 <span data-ttu-id="4fb4a-111">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="4fb4a-111">_lpszProfileName_</span></span>
  
> <span data-ttu-id="4fb4a-112">[in] Ein Zeiger auf eine Zeichenfolge, die den Namen des Profils enthält, das für die ANMELDUNG des MAPI-Spoolers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-112">[in] A pointer to a string that contains the name of the profile being used for the MAPI spooler logon.</span></span> <span data-ttu-id="4fb4a-113">Diese Zeichenfolge kann in Dialogfelder angezeigt, in eine Protokolldatei geschrieben oder einfach ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-113">This string can be displayed in dialog boxes, written out to a log file, or simply ignored.</span></span> <span data-ttu-id="4fb4a-114">Sie muss im Unicode-Format vorliegen, wenn MAPI_UNICODE im  _ulFlags-Parameter festgelegt_ ist.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-114">It must be in Unicode format if the MAPI_UNICODE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="4fb4a-115">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="4fb4a-115">_cbEntryID_</span></span>
  
> <span data-ttu-id="4fb4a-116">[in] Die Größe des Eintragsbezeichners in Bytes, auf den der  _lpEntryID-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-116">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="4fb4a-117">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="4fb4a-117">_lpEntryID_</span></span>
  
> <span data-ttu-id="4fb4a-118">[in] Ein Zeiger auf die Eintrags-ID für den Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-118">[in] A pointer to the entry identifier for the message store.</span></span> <span data-ttu-id="4fb4a-119">Das Übergeben von NULL im  _lpEntryID-Parameter_ gibt an, dass ein Nachrichtenspeicher noch nicht ausgewählt wurde und dass Dialogfelder angezeigt werden können, in denen der Benutzer einen Nachrichtenspeicher auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-119">Passing NULL in the  _lpEntryID_ parameter indicates that a message store has not yet been selected and that dialog boxes that enable the user to select a message store can be presented.</span></span> 
    
 <span data-ttu-id="4fb4a-120">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4fb4a-120">_ulFlags_</span></span>
  
> <span data-ttu-id="4fb4a-121">[in] Eine Bitmaske mit Flags, die steuert, wie die Anmeldung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-121">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="4fb4a-122">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="4fb4a-122">The following flags can be set:</span></span>
    
<span data-ttu-id="4fb4a-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="4fb4a-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="4fb4a-124">Der Aufruf kann auch dann erfolgreich sein, wenn das zugrunde liegende Objekt für die aufrufende Implementierung nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-124">The call is allowed to succeed even if the underlying object is not available to the calling implementation.</span></span> <span data-ttu-id="4fb4a-125">Wenn das Objekt nicht verfügbar ist, kann ein nachfolgender Aufruf des Objekts einen Fehler zur Folge haben.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-125">If the object is not available, a subsequent call to the object might raise an error.</span></span>
    
<span data-ttu-id="4fb4a-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4fb4a-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="4fb4a-127">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-127">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="4fb4a-128">Wenn MAPI_UNICODE nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-128">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="4fb4a-129">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="4fb4a-129">MDB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="4fb4a-130">Verhindert die Anzeige von Anmeldedialogfeldern.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-130">Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="4fb4a-131">Wenn dieses Flag festgelegt ist, wird der Fehlerwert MAPI_E_LOGON_FAILED zurückgegeben, wenn die Anmeldung nicht erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-131">If this flag is set, the error value MAPI_E_LOGON_FAILED is returned if the logon is unsuccessful.</span></span> <span data-ttu-id="4fb4a-132">Wenn dieses Kennzeichen nicht festgelegt ist, kann der Nachrichtenspeicheranbieter den Benutzer zur Korrektur eines Namens oder Kennworts, zum Einfügen eines Datenträgers oder zum Ausführen anderer aktionen aufgefordert, die zum Herstellen einer Verbindung mit dem Speicher erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-132">If this flag is not set, the message store provider can prompt the user to correct a name or password, to insert a disk, or to perform other actions necessary to establish connection to the store.</span></span>
    
<span data-ttu-id="4fb4a-133">MDB_WRITE</span><span class="sxs-lookup"><span data-stu-id="4fb4a-133">MDB_WRITE</span></span> 
  
> <span data-ttu-id="4fb4a-134">Fordert Lese-/Schreibberechtigungen an.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-134">Requests read/write permission.</span></span>
    
 <span data-ttu-id="4fb4a-135">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="4fb4a-135">_lpInterface_</span></span>
  
> <span data-ttu-id="4fb4a-136">[in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), bei der sich der Nachrichtenspeicher anmelden soll.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-136">[in] A pointer to the interface identifier (IID) for the message store to log on to.</span></span> <span data-ttu-id="4fb4a-137">Das Übergeben von NULL gibt an, dass die MAPI-Schnittstelle für den Nachrichtenspeicher ([IMsgStore](imsgstoreimapiprop.md)) zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-137">Passing NULL indicates the MAPI interface for the message store ([IMsgStore](imsgstoreimapiprop.md)) is returned.</span></span> <span data-ttu-id="4fb4a-138">Der  _lpInterface-Parameter_ kann auch auf einen Bezeichner für eine geeignete Schnittstelle für den Nachrichtenspeicher festgelegt werden (z. B. IID_IUnknown oder IID_IMAPIProp).</span><span class="sxs-lookup"><span data-stu-id="4fb4a-138">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the message store (for example IID_IUnknown or IID_IMAPIProp).</span></span> 
    
 <span data-ttu-id="4fb4a-139">_cbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="4fb4a-139">_cbSpoolSecurity_</span></span>
  
> <span data-ttu-id="4fb4a-140">[in] Ein Zeiger auf die Größe der Überprüfungsdaten im  _lppbSpoolSecurity-Parameter_ in Bytes.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-140">[in] A pointer to the size, in bytes, of validation data in the  _lppbSpoolSecurity_ parameter.</span></span> 
    
 <span data-ttu-id="4fb4a-141">_lpbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="4fb4a-141">_lpbSpoolSecurity_</span></span>
  
> <span data-ttu-id="4fb4a-142">[in] Ein Zeiger auf einen Zeiger auf Validierungsdaten.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-142">[in] A pointer to a pointer to validation data.</span></span> <span data-ttu-id="4fb4a-143">Die **SpoolerLogon-Methode** verwendet diese Daten, um den MAPI-Spooler im selben Speicher wie der zuvor angemeldete Nachrichtenspeicheranbieter mit der [IMSProvider::Logon-Methode](imsprovider-logon.md) zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-143">The **SpoolerLogon** method uses this data to log the MAPI spooler on to the same store as the message store provider previously logged on to by using the [IMSProvider::Logon](imsprovider-logon.md) method.</span></span> 
    
 <span data-ttu-id="4fb4a-144">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="4fb4a-144">_lppMAPIError_</span></span>
  
> <span data-ttu-id="4fb4a-145">[out] Ein Zeiger auf einen Zeiger auf die zurückgegebene [MAPIERROR-Struktur,](mapierror.md) die Versions-, Komponenten- und Kontextinformationen für einen Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-145">[out] A pointer to a pointer to the returned [MAPIERROR](mapierror.md) structure, if any, that contains version, component, and context information for an error.</span></span> <span data-ttu-id="4fb4a-146">Der  _Parameter lppMAPIError_ kann auf NULL festgelegt werden, wenn keine **MAPIERROR-Struktur** zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-146">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="4fb4a-147">_lppMSLogon_</span><span class="sxs-lookup"><span data-stu-id="4fb4a-147">_lppMSLogon_</span></span>
  
> <span data-ttu-id="4fb4a-148">[out] Ein Zeiger auf den Zeiger auf das Anmeldeobjekt des Nachrichtenspeichers, bei dem sich MAPI anmelden soll.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-148">[out] A pointer to the pointer to the message store logon object for MAPI to log on to.</span></span>
    
 <span data-ttu-id="4fb4a-149">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="4fb4a-149">_lppMDB_</span></span>
  
> <span data-ttu-id="4fb4a-150">[out] Ein Zeiger auf den Zeiger auf das Nachrichtenspeicherobjekt, an dem sich der MAPI-Spooler und die Clientanwendungen anmelden können.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-150">[out] A pointer to the pointer to the message store object for the MAPI spooler and client applications to log on to.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4fb4a-151">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4fb4a-151">Return value</span></span>

<span data-ttu-id="4fb4a-152">S_OK</span><span class="sxs-lookup"><span data-stu-id="4fb4a-152">S_OK</span></span> 
  
> <span data-ttu-id="4fb4a-153">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-153">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="4fb4a-154">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="4fb4a-154">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="4fb4a-155">Das Profil enthält nicht genügend Informationen, damit die Anmeldung abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-155">The profile does not contain enough information for the logon to complete.</span></span> <span data-ttu-id="4fb4a-156">Wenn dieser Wert zurückgegeben wird, ruft MAPI die Einstiegspunktfunktion des Nachrichtenspeicheranbieters auf.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-156">When this value is returned, MAPI calls the message store provider's message service entry point function.</span></span>
    
<span data-ttu-id="4fb4a-157">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="4fb4a-157">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="4fb4a-158">Der Aufruf ist erfolgreich, der Nachrichtenspeicheranbieter verfügt jedoch über Fehlerinformationen.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-158">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="4fb4a-159">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="4fb4a-160">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="4fb4a-161">Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="4fb4a-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> <span data-ttu-id="4fb4a-162">Rufen Sie die [IMAPISession::GetLastError-Methode](imapisession-getlasterror.md) auf, um die Fehlerinformationen vom Anbieter zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-162">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4fb4a-163">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4fb4a-163">Remarks</span></span>

<span data-ttu-id="4fb4a-164">Der MAPI-Spooler ruft die **IMSProvider::SpoolerLogon-Methode** auf, um sich bei einem Nachrichtenspeicher zu anmelden.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-164">The MAPI spooler calls the **IMSProvider::SpoolerLogon** method to log on to a message store.</span></span> <span data-ttu-id="4fb4a-165">Der MAPI-Spooler sollte das Nachrichtenspeicherobjekt verwenden, das vom Nachrichtenspeicheranbieter im  _lppMDB-Parameter_ während und nach der Anmeldung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-165">The MAPI spooler should use the message store object returned by the message store provider in the  _lppMDB_ parameter during and after logon.</span></span> 
  
<span data-ttu-id="4fb4a-166">Zur Konsistenz mit der [IMSProvider::Logon-Methode](imsprovider-logon.md) gibt der Anbieter auch ein Anmeldeobjekt des Nachrichtenspeichers im  _lppMSLogon-Parameter_ zurück.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-166">For consistency with the [IMSProvider::Logon](imsprovider-logon.md) method, the provider also returns a message store logon object in the  _lppMSLogon_ parameter.</span></span> <span data-ttu-id="4fb4a-167">Die Verwendung des Store-Objekts und des Anmeldeobjekts ist für die übliche Storeanmeldung identisch. Es sollte eine 1:1-Entsprechung zwischen dem Anmeldeobjekt und dem Storeobjekt sein, damit die Objekte so tun, als wären sie ein Objekt, das zwei Schnittstellen verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-167">The use of the store object and the logon object are identical for usual store logon; there should be a one-to-one correspondence between the logon object and the store object such that the objects act as if they are one object that exposes two interfaces.</span></span> <span data-ttu-id="4fb4a-168">Die beiden Objekte werden zusammen erstellt und gemeinsam frei.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-168">The two objects are created together and freed together.</span></span> 
  
<span data-ttu-id="4fb4a-169">Der Speicheranbieter sollte das zurückgegebene Nachrichtenspeicherobjekt intern markieren, um anzugeben, dass der Speicher vom MAPI-Spooler verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-169">The store provider should internally mark the returned message store object to indicate that the store is being used by the MAPI spooler.</span></span> <span data-ttu-id="4fb4a-170">Einige Methoden für dieses Speicherobjekt verhalten sich anders als für das Nachrichtenspeicherobjekt, das Clientanwendungen zur Verfügung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-170">Some of the methods for this store object behave differently than for the message store object provided to client applications.</span></span> <span data-ttu-id="4fb4a-171">Das Behalten dieser internen Markierung ist die häufigste Methode, um das für den MAPI-Spooler spezifische Verhalten auszulösen.</span><span class="sxs-lookup"><span data-stu-id="4fb4a-171">Keeping this internal mark is the most common way of triggering the behavior specific to the MAPI spooler.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4fb4a-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fb4a-172">See also</span></span>



[<span data-ttu-id="4fb4a-173">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="4fb4a-173">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="4fb4a-174">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="4fb4a-174">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="4fb4a-175">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4fb4a-175">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

