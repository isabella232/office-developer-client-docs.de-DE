---
title: MAPIInitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIInitialize
api_type:
- HeaderDef
ms.assetid: b9584226-79d2-4d83-8f31-dbfbc50f16c5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6464f16d9ad73b332ff20dc007ef162b9525c6d5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411176"
---
# <a name="mapiinitialize"></a><span data-ttu-id="78217-103">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="78217-103">MAPIInitialize</span></span>

  
  
<span data-ttu-id="78217-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78217-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78217-105">Erhöht die Referenzanzahl des MAPI-Subsystems und initialisiert globale Daten für die MAPI-DLL.</span><span class="sxs-lookup"><span data-stu-id="78217-105">Increments the MAPI subsystem reference count and initializes global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="78217-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="78217-106">Header file:</span></span>  <br/> |<span data-ttu-id="78217-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="78217-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="78217-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="78217-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="78217-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="78217-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="78217-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="78217-110">Called by:</span></span>  <br/> |<span data-ttu-id="78217-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="78217-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a><span data-ttu-id="78217-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="78217-112">Parameters</span></span>

 <span data-ttu-id="78217-113">_lpMapiInit_</span><span class="sxs-lookup"><span data-stu-id="78217-113">_lpMapiInit_</span></span>
  
> <span data-ttu-id="78217-114">[in] Zeiger auf [eine MAPIINIT_0](mapiinit_0.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="78217-114">[in] Pointer to a [MAPIINIT_0](mapiinit_0.md) structure.</span></span> <span data-ttu-id="78217-115">Der  _lpMapiInit-Parameter_ kann auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="78217-115">The  _lpMapiInit_ parameter can be set to NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="78217-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78217-116">Return value</span></span>

<span data-ttu-id="78217-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="78217-117">S_OK</span></span> 
  
> <span data-ttu-id="78217-118">Das MAPI-Subsystem wurde erfolgreich initialisiert.</span><span class="sxs-lookup"><span data-stu-id="78217-118">The MAPI subsystem was initialized successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="78217-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="78217-119">Remarks</span></span>

<span data-ttu-id="78217-120">Die **MAPIInitialize-Funktion** erhöht die MAPI-Referenzanzahl für das MAPI-Subsystem, und die [MAPIUninitialize-Funktion](mapiuninitialize.md) dekrementiert die interne Referenzanzahl.</span><span class="sxs-lookup"><span data-stu-id="78217-120">The **MAPIInitialize** function increments the MAPI reference count for the MAPI subsystem, and the [MAPIUninitialize](mapiuninitialize.md) function decrements the internal reference count.</span></span> <span data-ttu-id="78217-121">Daher muss die Anzahl der Aufrufe einer Funktion der Anzahl der Aufrufe an die andere entspricht.</span><span class="sxs-lookup"><span data-stu-id="78217-121">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> <span data-ttu-id="78217-122">**MAPIInitialize** gibt S_OK zurück, wenn MAPI noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="78217-122">**MAPIInitialize** returns S_OK if MAPI has not been previously initialized.</span></span> 
  
<span data-ttu-id="78217-123">Ein Client oder Dienstanbieter muss **MAPIInitialize aufrufen,** bevor ein anderer MAPI-Aufruf ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="78217-123">A client or service provider must call **MAPIInitialize** before making any other MAPI call.</span></span> <span data-ttu-id="78217-124">Anderndienst führt dazu, dass Client- oder Dienstanbieteraufrufe den wert MAPI_E_NOT_INITIALIZED zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="78217-124">Failure to do so causes client or service provider calls to return the MAPI_E_NOT_INITIALIZED value.</span></span> 
  
<span data-ttu-id="78217-125">Wenn Sie **MAPIInitialize** aus einer Multithreadanwendung aufrufen, legen Sie den  _lpMapiInit-Parameter_ auf eine MAPIINIT_0 [fest,](mapiinit_0.md) die wie folgt deklariert wird:</span><span class="sxs-lookup"><span data-stu-id="78217-125">When calling **MAPIInitialize** from a multithreaded application, set the  _lpMapiInit_ parameter to a [MAPIINIT_0](mapiinit_0.md) structure that is declared as follows:</span></span> 
  
 <span data-ttu-id="78217-126">**MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS}</span><span class="sxs-lookup"><span data-stu-id="78217-126">**MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS}</span></span> 
  
<span data-ttu-id="78217-127">und rufen Sie an:</span><span class="sxs-lookup"><span data-stu-id="78217-127">and call:</span></span> 
  
 <span data-ttu-id="78217-128">**MAPIInitialize** ( &amp; MAPIINIT);</span><span class="sxs-lookup"><span data-stu-id="78217-128">**MAPIInitialize** (&amp;MAPIINIT);</span></span> 
  
<span data-ttu-id="78217-129">Wenn diese Struktur deklariert wird, erstellt MAPI einen separaten Thread für die Verarbeitung des Benachrichtigungsfensters, der fortgesetzt wird, bis die Initialisierungsreferenzanzahl auf Null fällt.</span><span class="sxs-lookup"><span data-stu-id="78217-129">When this structure is declared, MAPI creates a separate thread to handle the notification window, which continues until the initialize reference count falls to zero.</span></span> <span data-ttu-id="78217-130">Ein Windows-Dienst muss das **ulflags-Element** der MAPIINIT_0, auf die _von lpMapiInit_ verwiesen wird, auf MAPI_NT_SERVICE. </span><span class="sxs-lookup"><span data-stu-id="78217-130">A Windows service must set the **ulflags** member of the **MAPIINIT_0** structure pointed to by  _lpMapiInit_ to MAPI_NT_SERVICE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="78217-131">Sie können **MAPIInitialize** oder **MAPIUninitialize** nicht innerhalb einer Win32 **DllMain-Funktion** oder einer anderen Funktion aufrufen, die Threads erstellt oder beendet.</span><span class="sxs-lookup"><span data-stu-id="78217-131">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="78217-132">Weitere Informationen finden Sie unter [Using Thread-Safe Objects](using-thread-safe-objects.md).</span><span class="sxs-lookup"><span data-stu-id="78217-132">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  
 <span data-ttu-id="78217-133">**MAPIInitialize** gibt keine erweiterten Fehlerinformationen zurück.</span><span class="sxs-lookup"><span data-stu-id="78217-133">**MAPIInitialize** does not return any extended error information.</span></span> <span data-ttu-id="78217-134">Im Gegensatz zu den meisten anderen MAPI-Aufrufen sind die Bedeutungen der Rückgabewerte genau so definiert, dass sie dem jeweiligen Schritt der initialisierung entsprechen, der fehlgeschlagen ist:</span><span class="sxs-lookup"><span data-stu-id="78217-134">Unlike most other MAPI calls, the meanings of its return values are strictly defined to correspond to the particular step of the initialization that failed:</span></span> 
  
1. <span data-ttu-id="78217-135">Überprüft Parameter und Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="78217-135">Checks parameters and flags.</span></span>
    
    <span data-ttu-id="78217-136">MAPI_E_INVALID_PARAMETER oder MAPI_E_UNKNOWN_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="78217-136">MAPI_E_INVALID_PARAMETER or MAPI_E_UNKNOWN_FLAGS.</span></span> <span data-ttu-id="78217-137">Der Aufrufer hat ungültige Parameter oder Kennzeichen übergeben.</span><span class="sxs-lookup"><span data-stu-id="78217-137">Caller passed invalid parameter or flag.</span></span>
    
2. <span data-ttu-id="78217-138">Initialisiert die von MAPI erforderlichen Registrierungsschlüssel und bestätigt den Betriebssystemtyp.</span><span class="sxs-lookup"><span data-stu-id="78217-138">Initializes registry keys required by MAPI and confirms the type of operating system.</span></span> <span data-ttu-id="78217-139">Dieser Schritt erfolgt nur, wenn der Clientprozess als Dienst unter Windows ausgeführt wird und das MAPI_NT SERVICE-Flag in der MAPIINIT_0 **legt.**</span><span class="sxs-lookup"><span data-stu-id="78217-139">This step only happens if the client process is running as a service under Windows and sets the MAPI_NT SERVICE flag in the **MAPIINIT_0** structure.</span></span> 
    
    <span data-ttu-id="78217-140">MAPI_E_TOO_COMPLEX.</span><span class="sxs-lookup"><span data-stu-id="78217-140">MAPI_E_TOO_COMPLEX.</span></span> <span data-ttu-id="78217-141">Der Aufrufprozess ist ein Windows, und die von MAPI erforderlichen Registrierungsschlüssel konnten nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="78217-141">The calling process is a Windows service and registry keys required by MAPI could not be initialized.</span></span> 
    
    <span data-ttu-id="78217-142">Im Anwendungsereignisprotokoll sind möglicherweise weitere Informationen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="78217-142">Additional information may be available in the application event log.</span></span>
    
3. <span data-ttu-id="78217-143">Überprüfen Sie die Kompatibilität von MAPI mit OLE, und initialisieren Sie OLE.</span><span class="sxs-lookup"><span data-stu-id="78217-143">Check for the compatibility of MAPI with OLE, then initialize OLE.</span></span>
    
1. <span data-ttu-id="78217-144">Überprüft die Kompatibilität zwischen den aktuellen Versionen von OLE und MAPI.</span><span class="sxs-lookup"><span data-stu-id="78217-144">Checks for compatibility between the current versions of OLE and MAPI.</span></span> 
    
    <span data-ttu-id="78217-145">MAPI_E_VERSION.</span><span class="sxs-lookup"><span data-stu-id="78217-145">MAPI_E_VERSION.</span></span> <span data-ttu-id="78217-146">Die auf der Arbeitsstation installierte Version von OLE ist nicht mit dieser Version von MAPI kompatibel.</span><span class="sxs-lookup"><span data-stu-id="78217-146">The version of OLE installed on the workstation is not compatible with this version of MAPI.</span></span>
    
2. <span data-ttu-id="78217-147">Initialisiert OLE.</span><span class="sxs-lookup"><span data-stu-id="78217-147">Initializes OLE.</span></span> 
    
    <span data-ttu-id="78217-148">Nur während dieses Schritts kann diese Funktion einen Fehlercode zurückgeben, der hier nicht aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="78217-148">During this step only, this function can return an error code not listed here.</span></span> <span data-ttu-id="78217-149">Alle hier _nicht_ aufgeführten Fehler sollten von der OLE-Funktion **CoInitialize stammen.**</span><span class="sxs-lookup"><span data-stu-id="78217-149">Any error  _not_ listed here should be assumed to come from the OLE function **CoInitialize**.</span></span>
    
4. <span data-ttu-id="78217-150">Initialisiert globale Variablen pro Prozess.</span><span class="sxs-lookup"><span data-stu-id="78217-150">Initializes per-process global variables.</span></span>
    
    <span data-ttu-id="78217-151">MAPI_E_SESSION_LIMIT.</span><span class="sxs-lookup"><span data-stu-id="78217-151">MAPI_E_SESSION_LIMIT.</span></span> <span data-ttu-id="78217-152">MAPI richtet kontextspezifisch für den aktuellen Prozess ein.</span><span class="sxs-lookup"><span data-stu-id="78217-152">MAPI sets up context specific to the current process.</span></span> <span data-ttu-id="78217-153">Fehler können bei Win16 auftreten, wenn die Anzahl der Prozesse eine bestimmte Anzahl überschreitet, oder auf einem beliebigen System, wenn der verfügbare Arbeitsspeicher ausgeschöpft ist.</span><span class="sxs-lookup"><span data-stu-id="78217-153">Failures may occur on Win16 if the number of processes exceeds a certain number, or on any system if available memory is exhausted.</span></span>
    
5. <span data-ttu-id="78217-154">Initialisiert freigegebene globale Variablen aller Prozesse.</span><span class="sxs-lookup"><span data-stu-id="78217-154">Initializes shared global variables of all processes.</span></span>
    
    <span data-ttu-id="78217-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span><span class="sxs-lookup"><span data-stu-id="78217-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span></span> <span data-ttu-id="78217-156">Es waren nicht genügend Systemressourcen verfügbar, um den Vorgang abschließen zu können.</span><span class="sxs-lookup"><span data-stu-id="78217-156">Not enough system resources were available to complete the operation.</span></span>
    
6. <span data-ttu-id="78217-157">Initialisiert das Benachrichtigungsmodul, erstellt sein Fenster und seinen Thread, wenn es vom Flag MAPI_MULTITHREAD_NOTIFICATIONS wird.</span><span class="sxs-lookup"><span data-stu-id="78217-157">Initializes the notification engine, creates its window and its thread if requested by the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
    
    <span data-ttu-id="78217-158">MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="78217-158">MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="78217-159">Kann fehlschlagen, wenn die Systemressourcen ausgeschöpft sind.</span><span class="sxs-lookup"><span data-stu-id="78217-159">May fail if system resources are exhausted.</span></span> 
    
7. <span data-ttu-id="78217-160">Lädt und initialisiert den Profilanbieter.</span><span class="sxs-lookup"><span data-stu-id="78217-160">Loads and initializes the profile provider.</span></span> <span data-ttu-id="78217-161">Überprüft, ob **MAPIInitialize** auf den Registrierungsschlüssel zugreifen kann, in dem Profildaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="78217-161">Verifies that **MAPIInitialize** can access the registry key where profile data are stored.</span></span> 
    
    <span data-ttu-id="78217-162">MAPI_E_NOT_INITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="78217-162">MAPI_E_NOT_INITIALIZED.</span></span> <span data-ttu-id="78217-163">Beim Profilanbieter ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="78217-163">The profile provider has encountered an error.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="78217-164">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="78217-164">MFCMAPI reference</span></span>

<span data-ttu-id="78217-165">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="78217-165">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="78217-166">**Datei**</span><span class="sxs-lookup"><span data-stu-id="78217-166">**File**</span></span>|<span data-ttu-id="78217-167">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="78217-167">**Function**</span></span>|<span data-ttu-id="78217-168">**Comment**</span><span class="sxs-lookup"><span data-stu-id="78217-168">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="78217-169">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="78217-169">ContentsTableListCtrl.cpp</span></span>  <br/> ||<span data-ttu-id="78217-170">MFCMAPI verwendet die **MAPIInitialize-Methode,** um MAPI in einem Hintergrundthread zu initialisieren, um einige Tabellenverarbeitungen zu machen.</span><span class="sxs-lookup"><span data-stu-id="78217-170">MFCMAPI uses the **MAPIInitialize** method to initialize MAPI on a background thread to do some table processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="78217-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78217-171">See also</span></span>



[<span data-ttu-id="78217-172">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="78217-172">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

