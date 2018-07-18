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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d22c24088960debcd18ccd818dad23656f6a01f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793136"
---
# <a name="mapiinitialize"></a><span data-ttu-id="e0b78-103">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="e0b78-103">MAPIInitialize</span></span>

  
  
<span data-ttu-id="e0b78-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e0b78-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e0b78-105">Inkrementiert den Referenzzähler des MAPI-Subsystems und globale-Daten für die MAPI-DLL initialisiert.</span><span class="sxs-lookup"><span data-stu-id="e0b78-105">Increments the MAPI subsystem reference count and initializes global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e0b78-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e0b78-106">Header file:</span></span>  <br/> |<span data-ttu-id="e0b78-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="e0b78-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="e0b78-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="e0b78-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e0b78-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e0b78-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e0b78-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="e0b78-110">Called by:</span></span>  <br/> |<span data-ttu-id="e0b78-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="e0b78-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a><span data-ttu-id="e0b78-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0b78-112">Parameters</span></span>

 <span data-ttu-id="e0b78-113">_lpMapiInit_</span><span class="sxs-lookup"><span data-stu-id="e0b78-113">_lpMapiInit_</span></span>
  
> <span data-ttu-id="e0b78-114">[in] Zeiger auf eine [MAPIINIT_0](mapiinit_0.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e0b78-114">[in] Pointer to a [MAPIINIT_0](mapiinit_0.md) structure.</span></span> <span data-ttu-id="e0b78-115">Der Parameter _LpMapiInit_ kann auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e0b78-115">The  _lpMapiInit_ parameter can be set to NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e0b78-116">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="e0b78-116">Return value</span></span>

<span data-ttu-id="e0b78-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="e0b78-117">S_OK</span></span> 
  
> <span data-ttu-id="e0b78-118">MAPI-Subsystems wurde erfolgreich initialisiert.</span><span class="sxs-lookup"><span data-stu-id="e0b78-118">The MAPI subsystem was initialized successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e0b78-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0b78-119">Remarks</span></span>

<span data-ttu-id="e0b78-120">Die MAPI-Referenz für das MAPI-Subsystem und die [MAPIUninitialize](mapiuninitialize.md) Funktion dekrementiert zählen **"MAPIInitialize"** Funktion Schritten für die interne verweiszählung.</span><span class="sxs-lookup"><span data-stu-id="e0b78-120">The **MAPIInitialize** function increments the MAPI reference count for the MAPI subsystem, and the [MAPIUninitialize](mapiuninitialize.md) function decrements the internal reference count.</span></span> <span data-ttu-id="e0b78-121">Die Anzahl der Anrufe an eine Funktion muss daher die Anzahl der Aufrufe der anderen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e0b78-121">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> <span data-ttu-id="e0b78-122">**"MAPIInitialize"** gibt S_OK zurück, wenn MAPI zuvor nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e0b78-122">**MAPIInitialize** returns S_OK if MAPI has not been previously initialized.</span></span> 
  
<span data-ttu-id="e0b78-123">Ein Client oder Dienstanbieter muss **"MAPIInitialize"** aufrufen, bevor eine beliebige andere MAPI-Aufruf.</span><span class="sxs-lookup"><span data-stu-id="e0b78-123">A client or service provider must call **MAPIInitialize** before making any other MAPI call.</span></span> <span data-ttu-id="e0b78-124">Dazu wird Client oder Dienst Anbieter Aufrufe den MAPI_E_NOT_INITIALIZED Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e0b78-124">Failure to do so causes client or service provider calls to return the MAPI_E_NOT_INITIALIZED value.</span></span> 
  
<span data-ttu-id="e0b78-125">Beim Aufruf von **"MAPIInitialize"** aus einer Multithread-Anwendung, legen Sie den Parameter _LpMapiInit_ auf eine [MAPIINIT_0](mapiinit_0.md) -Struktur, die wie folgt deklariert wird:</span><span class="sxs-lookup"><span data-stu-id="e0b78-125">When calling **MAPIInitialize** from a multithreaded application, set the  _lpMapiInit_ parameter to a [MAPIINIT_0](mapiinit_0.md) structure that is declared as follows:</span></span> 
  
 <span data-ttu-id="e0b78-126">**MAPIINIT_0** MAPIINIT = {0, MAPI_MULTITHREAD_NOTIFICATIONS}</span><span class="sxs-lookup"><span data-stu-id="e0b78-126">**MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS}</span></span> 
  
<span data-ttu-id="e0b78-127">und rufen Sie:</span><span class="sxs-lookup"><span data-stu-id="e0b78-127">and call:</span></span> 
  
 <span data-ttu-id="e0b78-128">**"MAPIInitialize"** (&amp;MAPIINIT);</span><span class="sxs-lookup"><span data-stu-id="e0b78-128">**MAPIInitialize** (&amp;MAPIINIT);</span></span> 
  
<span data-ttu-id="e0b78-129">Wenn diese Struktur deklariert wird, erstellt MAPI einen getrennten Thread, um das Benachrichtigungsfenster verarbeitet werden, wird fortgesetzt, bis der Initialize-Referenzzähler auf 0 (null) fällt aus.</span><span class="sxs-lookup"><span data-stu-id="e0b78-129">When this structure is declared, MAPI creates a separate thread to handle the notification window, which continues until the initialize reference count falls to zero.</span></span> <span data-ttu-id="e0b78-130">Ein Windows-Dienst muss das **Ulflags** Mitglied der **MAPIINIT_0** -Struktur, die auf den _LpMapiInit_ zu MAPI_NT_SERVICE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e0b78-130">A Windows service must set the **ulflags** member of the **MAPIINIT_0** structure pointed to by  _lpMapiInit_ to MAPI_NT_SERVICE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e0b78-131">**"MAPIInitialize"** oder **MAPIUninitialize** aus kann nicht innerhalb einer Win32 **DllMain** -Funktion oder eine andere Funktion, die erstellt oder Threads beendet aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e0b78-131">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="e0b78-132">Weitere Informationen finden Sie unter [Verwenden von threadsicheren Objekten](using-thread-safe-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e0b78-132">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  
 <span data-ttu-id="e0b78-133">**"MAPIInitialize"** gibt keine erweiterten Fehlerinformationen zurück.</span><span class="sxs-lookup"><span data-stu-id="e0b78-133">**MAPIInitialize** does not return any extended error information.</span></span> <span data-ttu-id="e0b78-134">Im Gegensatz zu den meisten anderen MAPI-Aufrufe sind die Bedeutung der seine Rückgabewerte streng, um mit dem bestimmten Schritt der Initialisierung entsprechen, die nicht definiert:</span><span class="sxs-lookup"><span data-stu-id="e0b78-134">Unlike most other MAPI calls, the meanings of its return values are strictly defined to correspond to the particular step of the initialization that failed:</span></span> 
  
1. <span data-ttu-id="e0b78-135">Überprüft, Parameter und Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="e0b78-135">Checks parameters and flags.</span></span>
    
    <span data-ttu-id="e0b78-136">MAPI_E_INVALID_PARAMETER oder MAPI_E_UNKNOWN_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="e0b78-136">MAPI_E_INVALID_PARAMETER or MAPI_E_UNKNOWN_FLAGS.</span></span> <span data-ttu-id="e0b78-137">Ungültiger Parameter oder Flag Aufrufer übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="e0b78-137">Caller passed invalid parameter or flag.</span></span>
    
2. <span data-ttu-id="e0b78-138">Initialisiert MAPI erforderliche Registrierungsschlüssel, und die Art des Betriebssystems bestätigt.</span><span class="sxs-lookup"><span data-stu-id="e0b78-138">Initializes registry keys required by MAPI and confirms the type of operating system.</span></span> <span data-ttu-id="e0b78-139">Dieser Schritt tritt nur auf, wenn der Clientprozess als Dienst unter Windows ausgeführt wird und das Flag MAPI_NT-Dienst in der Struktur **MAPIINIT_0** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e0b78-139">This step only happens if the client process is running as a service under Windows and sets the MAPI_NT SERVICE flag in the **MAPIINIT_0** structure.</span></span> 
    
    <span data-ttu-id="e0b78-140">MAPI_E_TOO_COMPLEX.</span><span class="sxs-lookup"><span data-stu-id="e0b78-140">MAPI_E_TOO_COMPLEX.</span></span> <span data-ttu-id="e0b78-141">Der aufrufende Prozess ist ein Windows-Dienst und MAPI erforderliche Registrierungsschlüssel konnte nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e0b78-141">The calling process is a Windows service and registry keys required by MAPI could not be initialized.</span></span> 
    
    <span data-ttu-id="e0b78-142">Zusätzliche Informationen möglicherweise im Anwendungsereignisprotokoll zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="e0b78-142">Additional information may be available in the application event log.</span></span>
    
3. <span data-ttu-id="e0b78-143">Überprüfen Sie die Kompatibilität von MAPI mit OLE und anschließend werden Sie OLE initialisiert.</span><span class="sxs-lookup"><span data-stu-id="e0b78-143">Check for the compatibility of MAPI with OLE, then initialize OLE.</span></span>
    
1. <span data-ttu-id="e0b78-144">Überprüft die Kompatibilität zwischen den aktuellen Versionen von OLE und MAPI.</span><span class="sxs-lookup"><span data-stu-id="e0b78-144">Checks for compatibility between the current versions of OLE and MAPI.</span></span> 
    
    <span data-ttu-id="e0b78-145">MAPI_E_VERSION.</span><span class="sxs-lookup"><span data-stu-id="e0b78-145">MAPI_E_VERSION.</span></span> <span data-ttu-id="e0b78-146">Auf der Arbeitsstation installierte OLE-Version ist nicht kompatibel mit dieser Version von MAPI.</span><span class="sxs-lookup"><span data-stu-id="e0b78-146">The version of OLE installed on the workstation is not compatible with this version of MAPI.</span></span>
    
2. <span data-ttu-id="e0b78-147">OLE initialisiert.</span><span class="sxs-lookup"><span data-stu-id="e0b78-147">Initializes OLE.</span></span> 
    
    <span data-ttu-id="e0b78-148">In diesem Schritt nur kann diese Funktion nicht aufgelisteten Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="e0b78-148">During this step only, this function can return an error code not listed here.</span></span> <span data-ttu-id="e0b78-149">Etwaige Fehler _nicht_ aufgeführt Hier sollte angenommen werden, dass der OLE-Funktion **CoInitialize**stammen.</span><span class="sxs-lookup"><span data-stu-id="e0b78-149">Any error  _not_ listed here should be assumed to come from the OLE function **CoInitialize**.</span></span>
    
4. <span data-ttu-id="e0b78-150">Initialisiert pro Prozess globale Variablen.</span><span class="sxs-lookup"><span data-stu-id="e0b78-150">Initializes per-process global variables.</span></span>
    
    <span data-ttu-id="e0b78-151">MAPI_E_SESSION_LIMIT.</span><span class="sxs-lookup"><span data-stu-id="e0b78-151">MAPI_E_SESSION_LIMIT.</span></span> <span data-ttu-id="e0b78-152">MAPI richtet Kontext speziell für den aktuellen Prozess.</span><span class="sxs-lookup"><span data-stu-id="e0b78-152">MAPI sets up context specific to the current process.</span></span> <span data-ttu-id="e0b78-153">Fehler können auftreten, Win16 übersteigt die Anzahl der Prozesse eine bestimmte Anzahl oder auf einem System verfügbaren Arbeitsspeicher ausgeschöpft ist.</span><span class="sxs-lookup"><span data-stu-id="e0b78-153">Failures may occur on Win16 if the number of processes exceeds a certain number, or on any system if available memory is exhausted.</span></span>
    
5. <span data-ttu-id="e0b78-154">Initialisiert gemeinsam genutzte globale Variablen von allen Prozessen.</span><span class="sxs-lookup"><span data-stu-id="e0b78-154">Initializes shared global variables of all processes.</span></span>
    
    <span data-ttu-id="e0b78-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span><span class="sxs-lookup"><span data-stu-id="e0b78-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span></span> <span data-ttu-id="e0b78-156">Nicht genügend Systemressourcen waren zum Abschließen des Vorgangs verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e0b78-156">Not enough system resources were available to complete the operation.</span></span>
    
6. <span data-ttu-id="e0b78-157">Initialisiert das Modul Benachrichtigung, die zugehörigen Fenster und einem Thread erstellt, wenn durch das Flag MAPI_MULTITHREAD_NOTIFICATIONS angefordert.</span><span class="sxs-lookup"><span data-stu-id="e0b78-157">Initializes the notification engine, creates its window and its thread if requested by the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
    
    <span data-ttu-id="e0b78-158">MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="e0b78-158">MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="e0b78-159">Kann fehlschlagen Systemressourcen aufgebraucht sind.</span><span class="sxs-lookup"><span data-stu-id="e0b78-159">May fail if system resources are exhausted.</span></span> 
    
7. <span data-ttu-id="e0b78-160">Lädt und initialisiert den Benutzerprofildienst-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="e0b78-160">Loads and initializes the profile provider.</span></span> <span data-ttu-id="e0b78-161">Stellt sicher, dass **"MAPIInitialize"** den Registrierungsschlüssel zugreifen können, auf dem Profildaten gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="e0b78-161">Verifies that **MAPIInitialize** can access the registry key where profile data are stored.</span></span> 
    
    <span data-ttu-id="e0b78-162">MAPI_E_NOT_INITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="e0b78-162">MAPI_E_NOT_INITIALIZED.</span></span> <span data-ttu-id="e0b78-163">Der Benutzerprofildienst-Anbieter ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="e0b78-163">The profile provider has encountered an error.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="e0b78-164">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="e0b78-164">MFCMAPI reference</span></span>

<span data-ttu-id="e0b78-165">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e0b78-165">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e0b78-166">**Datei**</span><span class="sxs-lookup"><span data-stu-id="e0b78-166">**File**</span></span>|<span data-ttu-id="e0b78-167">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="e0b78-167">**Function**</span></span>|<span data-ttu-id="e0b78-168">**Comment**</span><span class="sxs-lookup"><span data-stu-id="e0b78-168">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e0b78-169">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="e0b78-169">ContentsTableListCtrl.cpp</span></span>  <br/> ||<span data-ttu-id="e0b78-170">MFCMAPI (engl.) verwendet die Methode **"MAPIInitialize"** MAPI in einem Hintergrundthread die einige Tabelle Verarbeitung nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e0b78-170">MFCMAPI uses the **MAPIInitialize** method to initialize MAPI on a background thread to do some table processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e0b78-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0b78-171">See also</span></span>



[<span data-ttu-id="e0b78-172">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="e0b78-172">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

