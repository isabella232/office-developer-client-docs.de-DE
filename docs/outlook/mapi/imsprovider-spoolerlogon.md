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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309737"
---
# <a name="imsproviderspoolerlogon"></a><span data-ttu-id="bb6b0-103">IMSProvider::SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="bb6b0-103">IMSProvider::SpoolerLogon</span></span>

  
  
<span data-ttu-id="bb6b0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb6b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb6b0-105">Protokolliert den MAPI-Spooler in einem Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-105">Logs the MAPI spooler on to a message store.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="bb6b0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb6b0-106">Parameters</span></span>

 <span data-ttu-id="bb6b0-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="bb6b0-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="bb6b0-108">in Ein Zeiger auf das MAPI-Unterstützungsobjekt für den Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-108">[in] A pointer to the MAPI support object for the message store.</span></span>
    
 <span data-ttu-id="bb6b0-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="bb6b0-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="bb6b0-110">in Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-110">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> 
    
 <span data-ttu-id="bb6b0-111">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="bb6b0-111">_lpszProfileName_</span></span>
  
> <span data-ttu-id="bb6b0-112">in Ein Zeiger auf eine Zeichenfolge, die den Namen des Profils enthält, das für die MAPI-Spooler-Anmeldung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-112">[in] A pointer to a string that contains the name of the profile being used for the MAPI spooler logon.</span></span> <span data-ttu-id="bb6b0-113">Diese Zeichenfolge kann in Dialogfeldern angezeigt werden, in eine Protokolldatei geschrieben oder einfach ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-113">This string can be displayed in dialog boxes, written out to a log file, or simply ignored.</span></span> <span data-ttu-id="bb6b0-114">Sie muss im Unicode-Format vorliegen, wenn das MAPI_UNICODE-Flag im _ulFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-114">It must be in Unicode format if the MAPI_UNICODE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="bb6b0-115">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="bb6b0-115">_cbEntryID_</span></span>
  
> <span data-ttu-id="bb6b0-116">in Die Größe der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird, in Bytes.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-116">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="bb6b0-117">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="bb6b0-117">_lpEntryID_</span></span>
  
> <span data-ttu-id="bb6b0-118">in Ein Zeiger auf die Eintrags-ID für den Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-118">[in] A pointer to the entry identifier for the message store.</span></span> <span data-ttu-id="bb6b0-119">Das übergeben von NULL im Parameter _lpEntryID_ gibt an, dass noch kein Nachrichtenspeicher ausgewählt wurde und dass Dialogfelder, in denen der Benutzer einen Nachrichtenspeicher auswählen kann, angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-119">Passing NULL in the  _lpEntryID_ parameter indicates that a message store has not yet been selected and that dialog boxes that enable the user to select a message store can be presented.</span></span> 
    
 <span data-ttu-id="bb6b0-120">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bb6b0-120">_ulFlags_</span></span>
  
> <span data-ttu-id="bb6b0-121">in Eine Bitmaske von Flags, die die Ausführung der Anmeldung steuert.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-121">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="bb6b0-122">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="bb6b0-122">The following flags can be set:</span></span>
    
<span data-ttu-id="bb6b0-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="bb6b0-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="bb6b0-124">Der Aufruf kann auch dann erfolgreich ausgeführt werden, wenn das zugrunde liegende Objekt für die aufrufende Implementierung nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-124">The call is allowed to succeed even if the underlying object is not available to the calling implementation.</span></span> <span data-ttu-id="bb6b0-125">Wenn das Objekt nicht verfügbar ist, kann bei einem nachfolgenden Aufruf des Objekts ein Fehler ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-125">If the object is not available, a subsequent call to the object might raise an error.</span></span>
    
<span data-ttu-id="bb6b0-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bb6b0-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="bb6b0-127">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-127">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="bb6b0-128">Wenn MAPI_UNICODE nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-128">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="bb6b0-129">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="bb6b0-129">MDB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="bb6b0-130">Verhindert die Anzeige von Anmelde Dialogfeldern.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-130">Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="bb6b0-131">Wenn dieses Flag festgelegt ist, wird der Fehlerwert MAPI_E_LOGON_FAILED zurückgegeben, wenn die Anmeldung nicht erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-131">If this flag is set, the error value MAPI_E_LOGON_FAILED is returned if the logon is unsuccessful.</span></span> <span data-ttu-id="bb6b0-132">Wenn dieses Flag nicht festgelegt ist, kann der Nachrichtenspeicher Anbieter den Benutzer auffordern, einen Namen oder ein Kennwort zu korrigieren, einen Datenträger einzufügen oder andere erforderliche Aktionen auszuführen, um eine Verbindung mit dem Speicher herzustellen.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-132">If this flag is not set, the message store provider can prompt the user to correct a name or password, to insert a disk, or to perform other actions necessary to establish connection to the store.</span></span>
    
<span data-ttu-id="bb6b0-133">MDB_WRITE</span><span class="sxs-lookup"><span data-stu-id="bb6b0-133">MDB_WRITE</span></span> 
  
> <span data-ttu-id="bb6b0-134">Fordert Lese-/Schreibzugriff-Berechtigung an.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-134">Requests read/write permission.</span></span>
    
 <span data-ttu-id="bb6b0-135">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="bb6b0-135">_lpInterface_</span></span>
  
> <span data-ttu-id="bb6b0-136">in Ein Zeiger auf die Schnittstellen-ID (IID) für den Nachrichtenspeicher, an dem sich die Anmeldung anmeldet.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-136">[in] A pointer to the interface identifier (IID) for the message store to log on to.</span></span> <span data-ttu-id="bb6b0-137">Übergeben von NULL gibt an, dass die MAPI-Schnittstelle für den Nachrichtenspeicher ([IMsgStore](imsgstoreimapiprop.md)) zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-137">Passing NULL indicates the MAPI interface for the message store ([IMsgStore](imsgstoreimapiprop.md)) is returned.</span></span> <span data-ttu-id="bb6b0-138">Der _lpInterface_ -Parameter kann auch auf einen Bezeichner für eine entsprechende Schnittstelle für den Nachrichtenspeicher festgelegt werden (beispielsweise IID_IUnknown oder IID_IMAPIProp).</span><span class="sxs-lookup"><span data-stu-id="bb6b0-138">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the message store (for example IID_IUnknown or IID_IMAPIProp).</span></span> 
    
 <span data-ttu-id="bb6b0-139">_cbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="bb6b0-139">_cbSpoolSecurity_</span></span>
  
> <span data-ttu-id="bb6b0-140">in Ein Zeiger auf die Größe der Validierungsdaten im _lppbSpoolSecurity_ -Parameter in Byte.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-140">[in] A pointer to the size, in bytes, of validation data in the  _lppbSpoolSecurity_ parameter.</span></span> 
    
 <span data-ttu-id="bb6b0-141">_lpbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="bb6b0-141">_lpbSpoolSecurity_</span></span>
  
> <span data-ttu-id="bb6b0-142">in Ein Zeiger auf einen Zeiger auf Validierungsdaten.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-142">[in] A pointer to a pointer to validation data.</span></span> <span data-ttu-id="bb6b0-143">Die **SpoolerLogon** -Methode verwendet diese Daten, um den MAPI-Spooler in demselben Speicher wie der zuvor angemeldete Nachrichtenspeicher Anbieter mithilfe der [IMSProvider:: Login](imsprovider-logon.md) -Methode zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-143">The **SpoolerLogon** method uses this data to log the MAPI spooler on to the same store as the message store provider previously logged on to by using the [IMSProvider::Logon](imsprovider-logon.md) method.</span></span> 
    
 <span data-ttu-id="bb6b0-144">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="bb6b0-144">_lppMAPIError_</span></span>
  
> <span data-ttu-id="bb6b0-145">Out Ein Zeiger auf einen Zeiger auf die zurückgegebene [MAPIERROR](mapierror.md) -Struktur, die Versions-, Komponenten-und Kontextinformationen für einen Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-145">[out] A pointer to a pointer to the returned [MAPIERROR](mapierror.md) structure, if any, that contains version, component, and context information for an error.</span></span> <span data-ttu-id="bb6b0-146">Der _lppMAPIError_ -Parameter kann auf NULL festgelegt werden, wenn keine **MAPIERROR** -Struktur zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-146">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="bb6b0-147">_lppMSLogon_</span><span class="sxs-lookup"><span data-stu-id="bb6b0-147">_lppMSLogon_</span></span>
  
> <span data-ttu-id="bb6b0-148">Out Ein Zeiger auf den Zeiger auf das Nachrichtenspeicher-Anmeldeobjekt für die Anmeldung bei MAPI.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-148">[out] A pointer to the pointer to the message store logon object for MAPI to log on to.</span></span>
    
 <span data-ttu-id="bb6b0-149">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="bb6b0-149">_lppMDB_</span></span>
  
> <span data-ttu-id="bb6b0-150">Out Ein Zeiger auf den Zeiger auf das Nachrichtenspeicherobjekt für die MAPI-Spooler und Clientanwendungen, die sich bei anmelden.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-150">[out] A pointer to the pointer to the message store object for the MAPI spooler and client applications to log on to.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bb6b0-151">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb6b0-151">Return value</span></span>

<span data-ttu-id="bb6b0-152">S_OK</span><span class="sxs-lookup"><span data-stu-id="bb6b0-152">S_OK</span></span> 
  
> <span data-ttu-id="bb6b0-153">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-153">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="bb6b0-154">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="bb6b0-154">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="bb6b0-155">Das Profil enthält nicht genügend Informationen, damit die Anmeldung abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-155">The profile does not contain enough information for the logon to complete.</span></span> <span data-ttu-id="bb6b0-156">Wenn dieser Wert zurückgegeben wird, ruft MAPI die Nachrichtendienst-Einstiegspunktfunktion des Nachrichtenspeicher Anbieters auf.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-156">When this value is returned, MAPI calls the message store provider's message service entry point function.</span></span>
    
<span data-ttu-id="bb6b0-157">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="bb6b0-157">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="bb6b0-158">Der Aufruf war erfolgreich, aber der Nachrichtenspeicher Anbieter hat Fehlerinformationen.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-158">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="bb6b0-159">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="bb6b0-160">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="bb6b0-161">Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="bb6b0-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> <span data-ttu-id="bb6b0-162">Rufen Sie die [IMAPISession:: getlasterroraufzurufen](imapisession-getlasterror.md) -Methode auf, um die Fehlerinformationen vom Anbieter abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-162">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="bb6b0-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb6b0-163">Remarks</span></span>

<span data-ttu-id="bb6b0-164">Der MAPI-Spooler Ruft die **IMSProvider:: SpoolerLogon** -Methode auf, um sich bei einem Nachrichtenspeicher anzumelden.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-164">The MAPI spooler calls the **IMSProvider::SpoolerLogon** method to log on to a message store.</span></span> <span data-ttu-id="bb6b0-165">Der MAPI-Spooler sollte das vom Nachrichtenspeicher Anbieter zurückgegebene Nachrichtenspeicherobjekt während und nach der Anmeldung im Parameter _lppMDB_ verwenden.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-165">The MAPI spooler should use the message store object returned by the message store provider in the  _lppMDB_ parameter during and after logon.</span></span> 
  
<span data-ttu-id="bb6b0-166">Aus Gründen der Konsistenz mit der [IMSProvider:: Login](imsprovider-logon.md) -Methode gibt der Anbieter auch ein Anmeldeobjekt für den Nachrichtenspeicher im Parameter _lppMSLogon_ zurück.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-166">For consistency with the [IMSProvider::Logon](imsprovider-logon.md) method, the provider also returns a message store logon object in the  _lppMSLogon_ parameter.</span></span> <span data-ttu-id="bb6b0-167">Die Verwendung des Store-Objekts und des LOGON-Objekts sind für die übliche Speicher Anmeldung identisch. Es sollte eine 1:1-Entsprechung zwischen dem Logon-Objekt und dem Store-Objekt vorhanden sein, sodass die Objekte so handeln, als ob es sich um ein Objekt handelt, das zwei Schnittstellen verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-167">The use of the store object and the logon object are identical for usual store logon; there should be a one-to-one correspondence between the logon object and the store object such that the objects act as if they are one object that exposes two interfaces.</span></span> <span data-ttu-id="bb6b0-168">Die beiden Objekte werden zusammen erstellt und gemeinsam freigegeben.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-168">The two objects are created together and freed together.</span></span> 
  
<span data-ttu-id="bb6b0-169">Der Informationsspeicher Anbieter sollte das zurückgegebene Nachrichtenspeicherobjekt intern kennzeichnen, um anzugeben, dass der Speicher vom MAPI-Spooler verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-169">The store provider should internally mark the returned message store object to indicate that the store is being used by the MAPI spooler.</span></span> <span data-ttu-id="bb6b0-170">Einige der Methoden für dieses Store-Objekt verhalten sich anders als für das Nachrichtenspeicherobjekt, das für Clientanwendungen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-170">Some of the methods for this store object behave differently than for the message store object provided to client applications.</span></span> <span data-ttu-id="bb6b0-171">Diese interne Markierung beizubehalten, ist die häufigste Methode zum Auslösen des Verhaltens, das für den MAPI-Spooler spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="bb6b0-171">Keeping this internal mark is the most common way of triggering the behavior specific to the MAPI spooler.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bb6b0-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb6b0-172">See also</span></span>



[<span data-ttu-id="bb6b0-173">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="bb6b0-173">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="bb6b0-174">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="bb6b0-174">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="bb6b0-175">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bb6b0-175">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

