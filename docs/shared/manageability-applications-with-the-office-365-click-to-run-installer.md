---
title: Integrieren von Verwaltbarkeit-Anwendungen mit Office 365 Klick-und-Los-Installationsprogramm
manager: lindalu
ms.date: 12/03/2019
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Hier erfahren Sie, wie Sie das Office 365 Klick-und-Los-Installationsprogramm mit einer Software Verwaltungslösung integrieren.
ms.openlocfilehash: 62bfef0063c414fcecd0948e49dfa098b5c82bbb
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819273"
---
# <a name="integrating-manageability-applications-with-office-365-click-to-run-installer"></a><span data-ttu-id="f27e3-103">Integrieren von Verwaltbarkeit-Anwendungen mit Office 365 Klick-und-Los-Installationsprogramm</span><span class="sxs-lookup"><span data-stu-id="f27e3-103">Integrating manageability applications with Office 365 click-to-run installer</span></span>

<span data-ttu-id="f27e3-104">Hier erfahren Sie, wie Sie das Office 365 Klick-und-Los-Installationsprogramm mit einer Software Verwaltungslösung integrieren.</span><span class="sxs-lookup"><span data-stu-id="f27e3-104">Learn how to integrate the Office 365 Click-to-Run installer with a software management solution.</span></span>
  
<span data-ttu-id="f27e3-105">Das Office 365 Klick-und-Los-Installationsprogramm stellt eine COM-Schnittstelle bereit, die IT-Spezialisten und Software Verwaltungslösungen die programmgesteuerte Steuerung der Updateverwaltung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="f27e3-105">The Office 365 Click-to-Run installer provides a COM interface that allows IT Professionals and software management solutions programmatic control over update management.</span></span> <span data-ttu-id="f27e3-106">Diese Schnittstelle stellt zusätzliche Verwaltungsfunktionen bereit, die über das Office-Bereitstellungs Tool hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="f27e3-106">This interface provides additional management capabilities beyond what is provided by the Office Deployment Tool.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f27e3-107">Dieser Artikel bezieht sich auf Office 2016 und höher, Office 365.</span><span class="sxs-lookup"><span data-stu-id="f27e3-107">This article applies to Office 2016 and later, Office 365.</span></span> 
  
## <a name="integrating-with-the-click-to-run"></a><span data-ttu-id="f27e3-108">Integrieren in das Klick-und-Los</span><span class="sxs-lookup"><span data-stu-id="f27e3-108">Integrating with the Click-to-Run</span></span>

<span data-ttu-id="f27e3-109">Um diese Schnittstelle zu verwenden, ruft eine verwaltbare Anwendung die COM-Schnittstelle auf und ruft freigegebene APIs auf, die direkt mit dem Klick-und-Los-Installationsdienst kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="f27e3-109">To use this interface, a manageability application invokes the COM interface and calls exposed APIs that communicate directly with the Click-to-Run installation service.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f27e3-110">Das Office-Klick-und-Los-Installationsprogramm kann über die Befehlszeile mit Parametern ausgeführt werden, die das Verhalten steuern können, wie im [Office-Bereitstellungs Tool für Klick-und-Los](https://www.microsoft.com/download/details.aspx?id=49117)dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="f27e3-110">The Office Click-to-Run installer can be run from the command-line with parameters that can control the behavior, as documented in [Office Deployment Tool for Click-to-Run](https://www.microsoft.com/download/details.aspx?id=49117).</span></span> 
  
<span data-ttu-id="f27e3-111">**Es folgt ein konzeptionelles Diagramm der COM-Schnittstelle.**</span><span class="sxs-lookup"><span data-stu-id="f27e3-111">**Following is a conceptual diagram of the COM interface**</span></span>

<span data-ttu-id="f27e3-112">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Ein Diagramm zur Verwendung der COM-Schnittstelle im Office-Klick-und-Los-Installationsprogramm")</span><span class="sxs-lookup"><span data-stu-id="f27e3-112">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on  the Office Click-To-Run installer")</span></span>
  
<span data-ttu-id="f27e3-113">Das Office 365 Klick-und-Los-Installationsprogramm implementiert eine COM-basierte Schnittstelle, die für CLSID- **CLSID_UpdateNotifyObject**registriert **IUpdateNotify** .</span><span class="sxs-lookup"><span data-stu-id="f27e3-113">The Office 365 Click-to-Run installer implements a COM-based interface, **IUpdateNotify** registered to CLSID **CLSID_UpdateNotifyObject**.</span></span>
  
<span data-ttu-id="f27e3-114">Diese Schnittstelle kann wie folgt aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="f27e3-114">This interface can be invoked as follows:</span></span>
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

<span data-ttu-id="f27e3-115">Der Anruf ist nur erfolgreich, wenn der Anrufer unter erhöhten Rechten ausgeführt wird, da das Installationsprogramm für die Klick-und-Los-Installation mit erhöhten Rechten ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="f27e3-115">The call will only succeed if the caller is running under elevated privileges, as the Click-to-Run installation program must be run with elevated privileges.</span></span>
  
<span data-ttu-id="f27e3-116">Die **IUpdateNotify** -com-Schnittstelle stellt drei asynchrone Funktionen zur Verfügung, die für die Überprüfung der Befehle und Parameter und die Planung der Ausführung mit dem Klick-und-Los-Installationsdienst verantwortlich sind.</span><span class="sxs-lookup"><span data-stu-id="f27e3-116">The **IUpdateNotify** COM interface exposes three asynchronous functions responsible for validating the commands and parameters and scheduling execution with the Click-to-Run installation service.</span></span> 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

<span data-ttu-id="f27e3-117">Eine Forth-Methode, **Status**, kann verwendet werden, um Informationen über den Status des zuletzt ausgeführten Befehls oder den Status des derzeit ausgeführten Befehls abzurufen (also Erfolg, Fehler, detaillierte Fehlercodes).</span><span class="sxs-lookup"><span data-stu-id="f27e3-117">A forth method, **Status**, can be used to get information about the status of the last executed command or the status of the currently executing command (i.e. success, failure, detailed error codes).</span></span>
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

<span data-ttu-id="f27e3-118">Es gibt vier Zustände, in denen der Klick-und-Los-Installationsdienst während seines Lebenszyklus möglicherweise vorliegt, während dessen **IUpdateNotify** -Methoden aufgerufen werden können. Neustarten, Leerlauf, herunterladen und anwenden.</span><span class="sxs-lookup"><span data-stu-id="f27e3-118">There are four states that the Click-to-Run installation service may be in during its lifecycle, during which **IUpdateNotify** methods may be called; Rebooting, Idle, Downloading and Applying.</span></span> 
  
<span data-ttu-id="f27e3-119">**Im folgenden finden Sie das Diagramm "Statuscomputer" der COM-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f27e3-119">**Following is the COM Interface State Machine diagram**</span></span>

<span data-ttu-id="f27e3-120">![A state diagram for the COM interface.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Ein Statusdiagramm für die COM-Schnittstelle")</span><span class="sxs-lookup"><span data-stu-id="f27e3-120">![A state diagram for the COM interface.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "A state diagram for the COM interface")</span></span>
  
> [!NOTE]
> <span data-ttu-id="f27e3-121">**Neustart: beim**Booten des Computers gibt es einen Zeitraum, in dem der Klick-und-Los-Installationsdienst nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f27e3-121">**Rebooting**: When the machine is booting there is a period of time when the Click-to-Run installer service is not available.</span></span> <span data-ttu-id="f27e3-122">Ein erfolgreicher Aufruf der Status-Methode nach einem Neustart wird eUPDATE_UNKNOWN zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f27e3-122">A successful call to the Status method after a reboot will return eUPDATE_UNKNOWN.</span></span> 
  
<span data-ttu-id="f27e3-123">**Leerlauf:** Wenn sich das Klick-und-Los-Installationsprogramm im Leerlauf befindet, können Sie Folgendes aufrufen:</span><span class="sxs-lookup"><span data-stu-id="f27e3-123">**Idle:** When the Click-to-Run installer is in the idle state, you can call:</span></span> 
  
- <span data-ttu-id="f27e3-124">**Apply**: Installieren Sie zuvor heruntergeladenen Inhalt.</span><span class="sxs-lookup"><span data-stu-id="f27e3-124">**Apply**: Install previously downloaded content.</span></span>
    
- <span data-ttu-id="f27e3-125">**Cancel**: gibt `0x800000e`zurück, "eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen."</span><span class="sxs-lookup"><span data-stu-id="f27e3-125">**Cancel**: Returns  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="f27e3-126">**Download**: lädt neue Inhalte zur späteren Installation auf den Client herunter.</span><span class="sxs-lookup"><span data-stu-id="f27e3-126">**Download**: Downloads new content to the client for later installation.</span></span>
    
- <span data-ttu-id="f27e3-127">**Status**: gibt das Ergebnis der letzten abgeschlossenen Aktion oder eine Fehlermeldung zurück, wenn die Aktion mit einem Fehler beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f27e3-127">**Status**: Returns the result of the last completed action, or an error message if the action ended in failure.</span></span> <span data-ttu-id="f27e3-128">Wenn keine vorherige Aktion vorliegt, \*\*\*\* wird der `eUPDATE_UNKNOWN`Status zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f27e3-128">If there is no previous action, **Status** returns  `eUPDATE_UNKNOWN`.</span></span>
    
<span data-ttu-id="f27e3-129">**Herunterladen:** Wenn sich das Klick-und-Los-Installationsprogramm im Download Zustand befindet, können Sie Folgendes aufrufen:</span><span class="sxs-lookup"><span data-stu-id="f27e3-129">**Downloading:** When the Click-to-Run installer is in the downloading state, you can call:</span></span> 
  
- <span data-ttu-id="f27e3-130">**Apply**: gibt ein **HRESULT** mit dem Wert `0x800000e`"eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen." zurück.</span><span class="sxs-lookup"><span data-stu-id="f27e3-130">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="f27e3-131">**Abbrechen**: beendet den Download und entfernt die teilweise heruntergeladenen Inhalte.</span><span class="sxs-lookup"><span data-stu-id="f27e3-131">**Cancel**: Stops the download and removes the partially downloaded content.</span></span>
    
- <span data-ttu-id="f27e3-132">**Download**: gibt ein **HRESULT** mit dem Wert `0x800000e`"eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen." zurück.</span><span class="sxs-lookup"><span data-stu-id="f27e3-132">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="f27e3-133">**Status**: gibt **DOWNLOAD_WIP** zurück, um anzugeben, dass die Download Arbeit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f27e3-133">**Status**: Returns **DOWNLOAD_WIP** to indicate that download work is in progress.</span></span> 
    
<span data-ttu-id="f27e3-134">**Anwendung:** Wenn das Klick-und-Los-Installationsprogramm den Download Inhalt bereits installiert hat:</span><span class="sxs-lookup"><span data-stu-id="f27e3-134">**Applying:** When the Click-to-Run installer is in the process of installing previously download content:</span></span> 
  
- <span data-ttu-id="f27e3-135">**Apply**: gibt ein **HRESULT** mit dem Wert `0x800000e`"eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen." zurück.</span><span class="sxs-lookup"><span data-stu-id="f27e3-135">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="f27e3-136">**Cancel**: gibt `0x800000e`zurück, die Apply-Aktion kann nicht abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="f27e3-136">**Cancel**: Returns  `0x800000e`, the Apply action cannot be canceled.</span></span>
    
- <span data-ttu-id="f27e3-137">**Download**: gibt ein **HRESULT** mit dem Wert `0x800000e`"eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen." zurück.</span><span class="sxs-lookup"><span data-stu-id="f27e3-137">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="f27e3-138">**Status**: gibt **APPLY_WIP** zurück, um anzugeben, dass die Anwendung "Arbeit" ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f27e3-138">**Status**: Returns **APPLY_WIP** to indicate that apply work is in progress.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="f27e3-139">Da OfficeC2RCOM ein com+-Dienst ist und dynamisch geladen wird, müssen Sie **CoCreateInstance** jedes Mal aufrufen, wenn Sie eine Methode für diese Klasse aufrufen, um sicherzustellen, dass Sie das erwartete Ergebnis erhalten.</span><span class="sxs-lookup"><span data-stu-id="f27e3-139">Since OfficeC2RCOM is a COM+ service and is dynamically loaded, you need to call **CoCreateInstance** every time you call a method on this class to ensure that you get the expected result.</span></span> <span data-ttu-id="f27e3-140">Der com+-Dienst behandelt das Erstellen einer neuen Instanz, wenn dies erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f27e3-140">The COM+ service will handle creating a new instance if necessary.</span></span> <span data-ttu-id="f27e3-141">Wenn eine der Methoden zum ersten Mal aufgerufen wird, lädt com+ das **IUpdateNotify** -Objekt und führt es in einer der dllhost. exe-Instanzen aus.</span><span class="sxs-lookup"><span data-stu-id="f27e3-141">When one of the methods is called for the first time, COM+ will load the **IUpdateNotify** object and run it within one of the dllhost.exe instances.</span></span> <span data-ttu-id="f27e3-142">Das neue Objekt bleibt im Leerlauf etwa 3 Minuten aktiv.</span><span class="sxs-lookup"><span data-stu-id="f27e3-142">The new object will stay active for about 3 minutes in idle.</span></span> <span data-ttu-id="f27e3-143">Wenn ein anschließender Aufruf innerhalb von drei Minuten nach dem letzten Aufruf erfolgt, bleibt das **IUpdateNotify** -Objekt geladen, und es wird keine neue Instanz erstellt.</span><span class="sxs-lookup"><span data-stu-id="f27e3-143">If a subsequent call is made within three minutes of the last call, the **IUpdateNotify** object will remain loaded and a new instance is not created.</span></span> <span data-ttu-id="f27e3-144">Wenn innerhalb von drei Minuten kein Aufruf erfolgt, wird das IUpdateNotify-Objekt entladen, und ein neues **IUpdateNotify** -Objekt wird erstellt, wenn der nächste Aufruf erfolgt.</span><span class="sxs-lookup"><span data-stu-id="f27e3-144">If no call is made within three minutes, the IUpdateNotify object will be unloaded and a new **IUpdateNotify** object will be created when the next call is made.</span></span> 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a><span data-ttu-id="f27e3-145">Leitfaden zur com-API-Referenz für Klick-und-Los-Installer</span><span class="sxs-lookup"><span data-stu-id="f27e3-145">Click-to-Run installer COM API reference guide</span></span>

<span data-ttu-id="f27e3-146">In der folgenden API-Referenzdokumentation:</span><span class="sxs-lookup"><span data-stu-id="f27e3-146">In the following API reference documentation:</span></span>
  
- <span data-ttu-id="f27e3-147">Parameter befinden sich in einem Schlüssel-Wert-Paar Format, das durch ein Leerzeichengetrennt ist.</span><span class="sxs-lookup"><span data-stu-id="f27e3-147">Parameters are in a key/value pair format separated by a space.</span></span>
    
- <span data-ttu-id="f27e3-148">Bei den Parametern wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="f27e3-148">The parameters are not case-sensitive.</span></span>
    
- <span data-ttu-id="f27e3-149">Es gibt eine [Liste von Parametern](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) mit verfügbarer Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="f27e3-149">There is a [list of parameters](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) with documentation available.</span></span> 
    
- <span data-ttu-id="f27e3-150">Zusammenfassung der IUpdateNotify2-Schnittstelle ist jetzt enthalten.</span><span class="sxs-lookup"><span data-stu-id="f27e3-150">Summary of IUpdateNotify2 interface is now included.</span></span>
    
### <a name="apply"></a><span data-ttu-id="f27e3-151">Anwenden</span><span class="sxs-lookup"><span data-stu-id="f27e3-151">Apply</span></span>

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a><span data-ttu-id="f27e3-152">Parameter</span><span class="sxs-lookup"><span data-stu-id="f27e3-152">Parameters</span></span>

-  <span data-ttu-id="f27e3-153">_Display Level_: **true** , um den Installationsstatus, einschließlich Fehlern, während des Updateprozesses anzuzeigen; **false** , um den Installationsstatus, einschließlich Fehlern, während des Aktualisierungsvorgangs auszublenden.</span><span class="sxs-lookup"><span data-stu-id="f27e3-153">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="f27e3-154">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="f27e3-154">The default is **false**.</span></span>
    
-  <span data-ttu-id="f27e3-155">_forceappshutdown_: **true** , um zu erzwingen, dass Office-Anwendungen sofort heruntergefahren werden, wenn die **Apply** -Aktion ausgelöst wird; **false** , wenn ein Fehler auftritt, wenn Office-Anwendungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f27e3-155">_forceappshutdown_: **true** to force Office applications to shut down immediately when the **Apply** action is triggered; **false** to fail if any Office applications are running.</span></span> <span data-ttu-id="f27e3-156">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="f27e3-156">The default is **false**.</span></span> <span data-ttu-id="f27e3-157">Weitere Informationen finden Sie unter [Hinweise](#bk_ApplyRemark) .</span><span class="sxs-lookup"><span data-stu-id="f27e3-157">See [Remarks](#bk_ApplyRemark) for more information.</span></span> 
    
  <span data-ttu-id="f27e3-158">Wenn eine Office-Anwendung ausgeführt wird, wenn die **Apply** -Aktion ausgelöst wird, tritt in der Regel die **Apply** -Aktion nicht mehr auf.</span><span class="sxs-lookup"><span data-stu-id="f27e3-158">If any Office application is running when the **Apply** action is triggered, the **Apply** action will usually fail.</span></span> <span data-ttu-id="f27e3-159">Die `forceappshutdown=true` Übergabe an die **Apply** -Methode führt dazu, dass der **OfficeClickToRun** -Dienst die Anwendungen sofort herunterfährt und das Update anwendet.</span><span class="sxs-lookup"><span data-stu-id="f27e3-159">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down the applications and apply the update.</span></span> <span data-ttu-id="f27e3-160">Der Benutzer kann in diesem Fall Datenverlust auftreten.</span><span class="sxs-lookup"><span data-stu-id="f27e3-160">The user may experience data loss in this case.</span></span> 
    
#### <a name="return-results"></a><span data-ttu-id="f27e3-161">Ergebnisse zurückgeben</span><span class="sxs-lookup"><span data-stu-id="f27e3-161">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f27e3-162">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="f27e3-162">**S_OK**</span></span> <br/> |<span data-ttu-id="f27e3-163">Aktion wurde erfolgreich an den Klick-und-Los-Dienst zur Ausführung übermittelt.</span><span class="sxs-lookup"><span data-stu-id="f27e3-163">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="f27e3-164">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="f27e3-164">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="f27e3-165">Der Aufrufer wird nicht mit erhöhten Rechten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f27e3-165">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="f27e3-166">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="f27e3-166">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="f27e3-167">Ungültige Parameter wurden übergeben.</span><span class="sxs-lookup"><span data-stu-id="f27e3-167">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="f27e3-168">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="f27e3-168">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="f27e3-169">Die Aktion ist zu diesem Zeitpunkt nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="f27e3-169">Action is not allowed at this time.</span></span> <span data-ttu-id="f27e3-170">Weitere Informationen finden Sie unter [Hinweise](#bk_ApplyRemark) .</span><span class="sxs-lookup"><span data-stu-id="f27e3-170">See [Remarks](#bk_ApplyRemark) for more information.</span></span>  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="f27e3-171">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f27e3-171">Remarks</span></span>

- <span data-ttu-id="f27e3-172">Wenn eine Office-Anwendung ausgeführt wird, wenn die **Apply** -Aktion ausgelöst wird, tritt bei der **Apply** -Aktion ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="f27e3-172">If any Office application is running when the **Apply** action is triggered, the **Apply** action will fail.</span></span> <span data-ttu-id="f27e3-173">Die `forceappshutdown=true` Übergabe an die **Apply** -Methode führt dazu, dass der **OfficeClickToRun** -Dienst sofort alle Office-Anwendungen herunterfährt, die ausgeführt werden und das Update anwenden.</span><span class="sxs-lookup"><span data-stu-id="f27e3-173">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down any Office applications that are running and apply the update.</span></span> <span data-ttu-id="f27e3-174">Dem Benutzer treten möglicherweise Daten auf, da Sie nicht zum Speichern von Änderungen an geöffneten Dokumenten aufgefordert werden..</span><span class="sxs-lookup"><span data-stu-id="f27e3-174">The user may experience data as they are not prompted to save changes to open documents..</span></span> 
    
- <span data-ttu-id="f27e3-175">Diese Aktion kann nur ausgelöst werden, wenn der com-Status einer der folgenden ist:</span><span class="sxs-lookup"><span data-stu-id="f27e3-175">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="f27e3-176">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="f27e3-176">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="f27e3-177">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="f27e3-177">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="f27e3-178">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="f27e3-178">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="f27e3-179">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="f27e3-179">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="f27e3-180">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="f27e3-180">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="f27e3-181">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="f27e3-181">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="f27e3-182">Wenn Sie die **Apply** -Methode aufrufen, ohne Inhalt zuvor herunterzuladen, wird die **Apply** -Methode den Bericht **erfolgreich ausgeführt** , da Sie festgestellt hat, dass nichts angewendet und der **Apply** -Prozess erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="f27e3-182">If you call the **Apply** method without previously downloading content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
### <a name="cancel"></a><span data-ttu-id="f27e3-183">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="f27e3-183">Cancel</span></span>

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a><span data-ttu-id="f27e3-184">Ergebnisse zurückgeben</span><span class="sxs-lookup"><span data-stu-id="f27e3-184">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f27e3-185">S_OK</span><span class="sxs-lookup"><span data-stu-id="f27e3-185">S_OK</span></span>  <br/> |<span data-ttu-id="f27e3-186">Aktion wurde erfolgreich an den Klick-und-Los-Dienst zur Ausführung übermittelt.</span><span class="sxs-lookup"><span data-stu-id="f27e3-186">Action was successfully submitted to the Click-to-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="f27e3-187">E_ILLEGAL_METHOD_CALL</span><span class="sxs-lookup"><span data-stu-id="f27e3-187">E_ILLEGAL_METHOD_CALL</span></span>  <br/> |<span data-ttu-id="f27e3-188">Die Aktion ist zu diesem Zeitpunkt nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="f27e3-188">Action is not allowed at this time.</span></span> <span data-ttu-id="f27e3-189">Weitere Informationen finden Sie im Abschnitt " [Hinweise](#bk_CancelRemarks) ".</span><span class="sxs-lookup"><span data-stu-id="f27e3-189">See the [Remarks](#bk_CancelRemarks) section for more information</span></span>  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a><span data-ttu-id="f27e3-190">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f27e3-190">Remarks</span></span>

- <span data-ttu-id="f27e3-191">Diese Methode kann nur ausgelöst werden, wenn die com-Status-ID **eDOWNLOAD_WIP**.</span><span class="sxs-lookup"><span data-stu-id="f27e3-191">This method can only be triggered when the COM status id **eDOWNLOAD_WIP**.</span></span> <span data-ttu-id="f27e3-192">Es wird versucht, die aktuelle Download Aktion abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="f27e3-192">It will attempt to cancel the current download action.</span></span> <span data-ttu-id="f27e3-193">Der com-Status wechselt in **eDOWNLOAD_CANCELLING** und ändert sich schließlich in **eDOWNLOAD_CANCELED**.</span><span class="sxs-lookup"><span data-stu-id="f27e3-193">The COM status will change to **eDOWNLOAD_CANCELLING** and eventually change to **eDOWNLOAD_CANCELED**.</span></span> <span data-ttu-id="f27e3-194">Der com-Status gibt **E_ILLEGAL_METHOD_CALL** zurück, wenn Sie zu einem anderen Zeitpunkt ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="f27e3-194">The COM status will return **E_ILLEGAL_METHOD_CALL** if triggered at any other time.</span></span> 
    
### <a name="download"></a><span data-ttu-id="f27e3-195">Herunterladen</span><span class="sxs-lookup"><span data-stu-id="f27e3-195">Download</span></span>

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a><span data-ttu-id="f27e3-196">Parameter</span><span class="sxs-lookup"><span data-stu-id="f27e3-196">Parameters</span></span>

-  <span data-ttu-id="f27e3-197">_Display Level_: **true** , um den Installationsstatus, einschließlich Fehlern, während des Updateprozesses anzuzeigen; **false** , um den Installationsstatus, einschließlich Fehlern, während des Aktualisierungsvorgangs auszublenden.</span><span class="sxs-lookup"><span data-stu-id="f27e3-197">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="f27e3-198">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="f27e3-198">The default is **false**.</span></span>
    
-  <span data-ttu-id="f27e3-199">_updatebaseurl_: URL zur alternativen Download Quelle.</span><span class="sxs-lookup"><span data-stu-id="f27e3-199">_updatebaseurl_: URL to the alternate download source.</span></span>
    
-  <span data-ttu-id="f27e3-200">_updatetoversion_: die Version, auf der Office aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f27e3-200">_updatetoversion_: The version to update Office to.</span></span> <span data-ttu-id="f27e3-201">Definieren Sie diesen Parameter, wenn Sie eine ältere Version als die aktuell installierte Version aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f27e3-201">Define this parameter if you want to update to an older version than the version that is currently installed.</span></span>
    
-  <span data-ttu-id="f27e3-202">_downloadsource_: CLSID der angepassten **IBackgroundCopyManager** -Implementierung (Bits-Manager).</span><span class="sxs-lookup"><span data-stu-id="f27e3-202">_downloadsource_: CLSID of the customized **IBackgroundCopyManager** implementation (BITS manager).</span></span> 
    
-  <span data-ttu-id="f27e3-203">_Content_-Kennung: gibt den Inhalt an, der vom Inhaltsserver über den angepassten Bits-Manager heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f27e3-203">_contentid_: Identifies the content to download from the content server through the customized BITS manager.</span></span> <span data-ttu-id="f27e3-204">Dieser Wert wird über die Bits-Schnittstelle zur Interpretation übergeben.</span><span class="sxs-lookup"><span data-stu-id="f27e3-204">This value is passed through the BITS interface for interpretation.</span></span>
    
#### <a name="return-results"></a><span data-ttu-id="f27e3-205">Ergebnisse zurückgeben</span><span class="sxs-lookup"><span data-stu-id="f27e3-205">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f27e3-206">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="f27e3-206">**S_OK**</span></span> <br/> |<span data-ttu-id="f27e3-207">Aktion wurde erfolgreich an den Klick-und-Los-Dienst zur Ausführung übermittelt.</span><span class="sxs-lookup"><span data-stu-id="f27e3-207">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="f27e3-208">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="f27e3-208">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="f27e3-209">Der Aufrufer wird nicht mit erhöhten Rechten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f27e3-209">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="f27e3-210">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="f27e3-210">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="f27e3-211">Ungültige Parameter wurden übergeben.</span><span class="sxs-lookup"><span data-stu-id="f27e3-211">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="f27e3-212">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="f27e3-212">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="f27e3-213">Die Aktion ist zu diesem Zeitpunkt nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="f27e3-213">Action is not allowed at this time.</span></span> <span data-ttu-id="f27e3-214">Weitere Informationen finden Sie unter [Hinweise](#bk_DownloadRemark) .</span><span class="sxs-lookup"><span data-stu-id="f27e3-214">See [Remarks](#bk_DownloadRemark) for more information.</span></span>  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="f27e3-215">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f27e3-215">Remarks</span></span>

- <span data-ttu-id="f27e3-216">Sie müssen _downloadsource_ und _Content_ -Nr als Paar angeben.</span><span class="sxs-lookup"><span data-stu-id="f27e3-216">You must specify  _downloadsource_ and  _contentid_ as a pair.</span></span> <span data-ttu-id="f27e3-217">Wenn dies nicht der Fall ist, gibt die **Download** -Methode einen **E_INVALIDARG** Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="f27e3-217">If not, the **Download** method will return an **E_INVALIDARG** error.</span></span> 
    
- <span data-ttu-id="f27e3-218">Wenn _downloadsource_, _Content_-und _updatebaseurl_ bereitgestellt werden, wird _updatebaseurl_ ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f27e3-218">If  _downloadsource_,  _contentid_, and  _updatebaseurl_ are provided,  _updatebaseurl_ will be ignored.</span></span> 
    
- <span data-ttu-id="f27e3-219">Diese Aktion kann nur ausgelöst werden, wenn der com-Status einer der folgenden ist:</span><span class="sxs-lookup"><span data-stu-id="f27e3-219">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="f27e3-220">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="f27e3-220">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="f27e3-221">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="f27e3-221">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="f27e3-222">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="f27e3-222">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="f27e3-223">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="f27e3-223">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="f27e3-224">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="f27e3-224">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="f27e3-225">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="f27e3-225">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="f27e3-226">Wenn Sie die **Apply** -Methode ohne zuvor heruntergeladenen Inhalt aufrufen, wird die **Apply** -Methode den Bericht **erfolgreich ausgeführt** , da Sie festgestellt hat, dass nichts angewendet und der **Apply** -Prozess erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="f27e3-226">If you call the **Apply** method without previously downloaded content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
#### <a name="examples"></a><span data-ttu-id="f27e3-227">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f27e3-227">Examples</span></span>

- <span data-ttu-id="f27e3-228">So laden Sie den Inhalt aus dem angepassten Bits-Manager herunter: Rufen Sie die **Download ()** -Funktion auf, indem Sie die folgenden Parameter übergeben:</span><span class="sxs-lookup"><span data-stu-id="f27e3-228">To download the content from the customized BITS manager: Call the **download()** function passing the following parameters:</span></span> 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- <span data-ttu-id="f27e3-229">Zum Herunterladen des Inhalts aus dem Microsoft CDN: Rufen Sie die **Download ()** -Funktion ohne Angabe der Parameter _downloadsource_, _contentbar_oder _updatebaseurl_ .</span><span class="sxs-lookup"><span data-stu-id="f27e3-229">To download the content from the Microsoft CDN: Call the **download()** function without specifying the  _downloadsource_,  _contentid_, or  _updatebaseurl_ parameters.</span></span> 
    
- <span data-ttu-id="f27e3-230">So laden Sie die Inhalte von einem benutzerdefinierten Speicherort herunter: Rufen Sie die **Download ()-** Funktion auf, indem Sie den folgenden Parameter übergeben:</span><span class="sxs-lookup"><span data-stu-id="f27e3-230">To download the content from a customized location: Call the **download()** function passing the following parameter:</span></span> 
    
  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a><span data-ttu-id="f27e3-231">Status</span><span class="sxs-lookup"><span data-stu-id="f27e3-231">Status</span></span>

```cpp
typdef struct _UPDATE_STATUS_REPORT
{
    UPDATE_STATUS status;
    UINT error;
    LPCWSTR contentid;
}UPDATE_STATUS_REPORT;
HRESULT status([out] _UPDATE_STATUS_REPORT& pUpdateStatusReport) // Get status of current action
```

#### <a name="parameters"></a><span data-ttu-id="f27e3-232">Parameter</span><span class="sxs-lookup"><span data-stu-id="f27e3-232">Parameters</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="f27e3-233">_pUpdateStatusReport_</span><span class="sxs-lookup"><span data-stu-id="f27e3-233">_pUpdateStatusReport_</span></span> <br/> |<span data-ttu-id="f27e3-234">Zeiger auf eine UPDATE_STATUS_REPORT Struktur.</span><span class="sxs-lookup"><span data-stu-id="f27e3-234">Pointer to an UPDATE_STATUS_REPORT structure.</span></span>  <br/> |
   
#### <a name="return-results"></a><span data-ttu-id="f27e3-235">Ergebnisse zurückgeben</span><span class="sxs-lookup"><span data-stu-id="f27e3-235">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f27e3-236">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="f27e3-236">**S_OK**</span></span> <br/> |<span data-ttu-id="f27e3-237">Die **Status** -Methode gibt immer dieses Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="f27e3-237">The **Status** method always returns this result.</span></span> <span data-ttu-id="f27e3-238">Überprüfen `UPDATE_STATUS_RESULT` Sie die Struktur auf den Status der aktuellen Aktion.</span><span class="sxs-lookup"><span data-stu-id="f27e3-238">Inspect the  `UPDATE_STATUS_RESULT` structure for the status of the current action.</span></span>  <br/> |
   
#### <a name="remarks"></a><span data-ttu-id="f27e3-239">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f27e3-239">Remarks</span></span>

- <span data-ttu-id="f27e3-240">Das Feld Status des `UPDATE_STATUS_REPORT` enthält den Status der aktuellen Aktion.</span><span class="sxs-lookup"><span data-stu-id="f27e3-240">The status field of the  `UPDATE_STATUS_REPORT` contains the status of the current action.</span></span> <span data-ttu-id="f27e3-241">Einer der folgenden Statuswerte wird zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="f27e3-241">One of the following status values is returned:</span></span> 
    
  ```cpp
  typedef enum _UPDATE_STATUS
  {
  eUPDATE_UNKNOWN = 0,
  eDOWNLOAD_PENDING,
  eDOWNLOAD_WIP,
  eDOWNLOAD_CANCELLING,
  eDOWNLOAD_CANCELLED,
  eDOWNLOAD_FAILED,
  eDOWNLOAD_SUCCEEDED,
  eAPPLY_PENDING,
  eAPPLY_WIP,
  eAPPLY_SUCCEEDED,
  eAPPLY_FAILED,
  } UPDATE_STATUS;
  
  ```

- <span data-ttu-id="f27e3-242">Wenn der letzte Befehl zu einem Fehler geführt hat, `UPDATE_STATUS_REPORT` enthält das Feld Error des-Fehlers detaillierte Informationen zu dem Fehler.</span><span class="sxs-lookup"><span data-stu-id="f27e3-242">If the last command resulted in an error, the error field of the  `UPDATE_STATUS_REPORT` contains detailed information about the error.</span></span> <span data-ttu-id="f27e3-243">Zwei Arten von Fehlercodes werden von der **Status** -Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f27e3-243">Two types of error codes are returned from the **Status** method.</span></span> 
    
- <span data-ttu-id="f27e3-244">Wenn der Fehler kleiner als `UPDATE_ERROR_CODE::eUNKNOWN`ist, ist der Fehler einer der folgenden vordefinierten Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="f27e3-244">If the error less than  `UPDATE_ERROR_CODE::eUNKNOWN`, the error is one of the following pre-defined error codes:</span></span>
    
  ```cpp
  typedef enum _UPDATE_ERROR_CODE
  {
  eOK = 0,
  eFAILED_UNEXPECTED,
  eTRIGGER_DISABLED,
  ePIPELINE_IN_USE,
  eFAILED_STOP_C2RSERVICE,
  eFAILED_GET_CLIENTUPDATEFOLDER,
  eFAILED_LOCK_PACKAGE_TO_UPDATE,
  eFAILED_CREATE_STREAM_SESSION,
  eFAILED_PUBLISH_WORKING_CONFIGURATION,
  eFAILED_DOWNLOAD_UPGRADE_PACKAGE,
  eFAILED_APPLY_UPGRADE_PACKAGE,
  eFAILED_INITIALIZE_RSOD,
  eFAILED_PUBLISH_RSOD,
  // Keep this one as the last
  eUNKNOWN
  } UPDATE_ERROR_CODE;
  
  ```

  <span data-ttu-id="f27e3-245">Wenn der Rückgabefehlercode größer als `UPDATE_ERROR_CODE::eUNKNOWN` der **HRESULT** -Wert eines fehlgeschlagenen Funktionsaufrufs ist.</span><span class="sxs-lookup"><span data-stu-id="f27e3-245">If the return error code is larger than  `UPDATE_ERROR_CODE::eUNKNOWN` it is the **HRESULT** of a failed function call.</span></span> <span data-ttu-id="f27e3-246">So extrahieren Sie das HRESULT `UPDATE_ERROR_CODE::eUNKNOWN` subtrahieren aus dem Wert, der im Feld Error `UPDATE_STATUS_REPORT`von zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f27e3-246">To extract the HRESULT subtract  `UPDATE_ERROR_CODE::eUNKNOWN` from the value returned in the error field of the  `UPDATE_STATUS_REPORT`.</span></span>
    
  <span data-ttu-id="f27e3-247">Die vollständige Liste der Status-und Fehlerwerte kann angezeigt werden, indem die in OfficeC2RCom. dll eingebettete **IUpdateNotify** -Typbibliothek überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="f27e3-247">The complete list of status and error values can be viewed by inspecting the **IUpdateNotify** type library embedded in OfficeC2RCom.dll.</span></span> 
    
- <span data-ttu-id="f27e3-248">Das Feld "Content-Nr" wird für Aufrufe von **Status** verwendet, nachdem der **Download** initiiert wurde, und gibt die Inhalts-Nr zurück, die an den **Download** Aufruf übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f27e3-248">The contentid field is used for calls to **Status** after **Download** has initiated and returns the contentid that was passed in to the **Download** call.</span></span> <span data-ttu-id="f27e3-249">Es wird empfohlen, dieses Feld vor dem Aufrufen der **Status** -Methode auf **null** zu initialisieren und anschließend den Wert nach dem Zurückgeben des **Status** zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f27e3-249">It is a best practice to initialize this field to **null** before you call the **Status** method and then check the value after **Status** has been returned.</span></span> <span data-ttu-id="f27e3-250">Wenn der Wert immer noch **null**ist, bedeutet dies, dass keine Inhalts-Nr vorhanden ist, die zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="f27e3-250">If the value is still **null**, that means there is no contentid to return.</span></span> <span data-ttu-id="f27e3-251">Wenn der Wert nicht **null**ist, müssen Sie ihn mit einem Aufruf von **sysfree String ()** freigeben.</span><span class="sxs-lookup"><span data-stu-id="f27e3-251">If the value is not **null**, you need to free it with a call to **SysFreeString()**.</span></span> <span data-ttu-id="f27e3-252">Im folgenden finden Sie einen Codeausschnitt zum Aufrufen des **Status** nach dem **Download**.</span><span class="sxs-lookup"><span data-stu-id="f27e3-252">Here is a code snippet of how to call **Status** after **Download**.</span></span>
    
  ```cpp
  std::wstring contentID;
  UPDATE_STATUS_REPORT statusReport;
  statusReport.status = eUPDATE_UNKNOWN;
  statusReport.error = eOK;
  statusReport.contentid = NULL;
  hr = p->Status(&statusReport);
  if (statusReport.contentid != NULL)
  {
  contentID = statusReport.contentid;
  SysFreeString(statusReport.contentid);
  }
  wprintf(L"ContentID: %s, Status: %d, LastError: %d", contentID.c_str(), statusReport.status, statusReport.error);
  
  ```

### <a name="summary-of-iupdatenotify2-interface"></a><span data-ttu-id="f27e3-253">Zusammenfassung der IUpdateNotify2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f27e3-253">Summary of IUpdateNotify2 interface</span></span>

> [!NOTE]
> <span data-ttu-id="f27e3-254">Diese Zusammenfassung wird als Kompliment zur [Integration von Verwaltbarkeit-Anwendungen mit dem Office 365 Klick-und-Los-Installationsprogramm](https://docs.microsoft.com/office/client-developer/shared/manageability-applications-with-the-office-365-click-to-run-installer)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="f27e3-254">This summary is provided as a compliment info to [Integrating manageability applications with the Office 365 click-to-run installer](https://docs.microsoft.com/office/client-developer/shared/manageability-applications-with-the-office-365-click-to-run-installer).</span></span> <span data-ttu-id="f27e3-255">Sobald das öffentliche Dokument aktualisiert wurde, kann dieses Dokument als veraltet betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="f27e3-255">Once the public doc is updated, this doc can be considered as obsolete.</span></span> 
  
<span data-ttu-id="f27e3-256">Von C2RTenant [16.0.8208.6352](https://oloop/BuildGroup/Details/tenantc2rclient#3519/1255278) (erstes öffentlich verfügbares Build sollte June Fork Build--8326. \*) Wir haben eine neue **IUpdateNotify2** -Schnittstelle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f27e3-256">From C2RTenant [16.0.8208.6352](https://oloop/BuildGroup/Details/tenantc2rclient#3519/1255278) (First publicly available build should be June fork build -- 8326.\*) we have added a new **IUpdateNotify2** interface.</span></span> <span data-ttu-id="f27e3-257">Hier finden Sie einige grundlegende Informationen zu dieser Schnittstelle:</span><span class="sxs-lookup"><span data-stu-id="f27e3-257">Here is some basic info about this interface:</span></span> 
  
- <span data-ttu-id="f27e3-258">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span><span class="sxs-lookup"><span data-stu-id="f27e3-258">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span></span>
    
- <span data-ttu-id="f27e3-259">Diese Schnittstelle hat auch die ursprüngliche IUpdateNotify-Schnittstelle gehostet, um Abwärtskompatibilität zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="f27e3-259">This interface also hosted the original IUpdateNotify interface to provide backward compatibility.</span></span> <span data-ttu-id="f27e3-260">Das heißt, wenn Sie diese Schnittstelle verwenden, haben Sie Zugriff auf alle Methoden, die in der **UpdateNotifyObject** -Schnittstelle bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f27e3-260">Which means if you use this interface, you have access to all the methods provided in **UpdateNotifyObject** interface.</span></span> 
    
- <span data-ttu-id="f27e3-261">Neue Methoden zu IUpdateNotify2 hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="f27e3-261">New methods added to IUpdateNotify2:</span></span>
    
  - <span data-ttu-id="f27e3-262">**HRESULT** GetBlockingApps (BSTR \* -appsliste).</span><span class="sxs-lookup"><span data-stu-id="f27e3-262">**HRESULT** GetBlockingApps([out] BSTR \* AppsList).</span></span> <span data-ttu-id="f27e3-263">Updates blockieren apps-Liste abrufen.</span><span class="sxs-lookup"><span data-stu-id="f27e3-263">Get updates blocking apps list.</span></span> <span data-ttu-id="f27e3-264">Bei diesem Aufruf werden ausgeführte Office-Apps zurückgegeben, wodurch der Aktualisierungsprozess blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="f27e3-264">This call will return running Office apps which will block the update process from proceeding.</span></span> 
    
  - <span data-ttu-id="f27e3-265">**HRESULT** GetOfficeDeploymentData ([in] int DataType, [in] **ein LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span><span class="sxs-lookup"><span data-stu-id="f27e3-265">**HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span></span> <span data-ttu-id="f27e3-266">Abrufen von Office-Bereitstellungsdaten</span><span class="sxs-lookup"><span data-stu-id="f27e3-266">Get Office deployment Data.</span></span> 
    
- <span data-ttu-id="f27e3-267">Wenn Sie die neuen Methoden verwenden möchten, müssen Sie Folgendes sicherstellen:</span><span class="sxs-lookup"><span data-stu-id="f27e3-267">If you want to use the new methods, you need to make sure:</span></span>
    
  - <span data-ttu-id="f27e3-268">Ihre C2R-Version ist neuer als der obige Build\>(= June Fork Build).</span><span class="sxs-lookup"><span data-stu-id="f27e3-268">Your C2R version is newer than the above build (\>= June fork build).</span></span>
    
  - <span data-ttu-id="f27e3-269">Verwenden Sie UpdateNotifyObject2 anstelle von **UpdateNotifyObject** , um **CoCreateInstance**aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="f27e3-269">Use UpdateNotifyObject2, instead of **UpdateNotifyObject** to call **CoCreateInstance**.</span></span>
    
<span data-ttu-id="f27e3-270">Wenn Sie keine der neuen Methoden verwenden, müssen Sie nichts ändern.</span><span class="sxs-lookup"><span data-stu-id="f27e3-270">If you don't use any of the new methods, you don't need to change anything.</span></span> <span data-ttu-id="f27e3-271">Alle vorhandenen Methoden funktionieren genauso genau wie zuvor.</span><span class="sxs-lookup"><span data-stu-id="f27e3-271">All the existing methods will work as exact the same way as before.</span></span>
  
## <a name="implementing-the-bits-interface"></a><span data-ttu-id="f27e3-272">Implementieren der Bits-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f27e3-272">Implementing the BITS interface</span></span>

<span data-ttu-id="f27e3-273">Der [intelligente Hintergrundübertragungsdienst (Background Intelligent Transfer Service](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) , Bits) ist ein von Microsoft bereitgestellter Dienst zum Übertragen von Dateien zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="f27e3-273">The [Background Intelligent Transfer Service](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) (BITS) is a service provided by Microsoft to transfer files between a client and server.</span></span> <span data-ttu-id="f27e3-274">Bits ist einer der Kanäle, die von einem Office-Klick-und-Los-Installationsprogramm zum Herunterladen von Inhalten verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="f27e3-274">BITS is one of the channels that Office Click-To-Run installer can use to download content.</span></span> <span data-ttu-id="f27e3-275">Standardmäßig verwendet das Office-Klick-und-Los-Installationsprogramm die in der Implementierung von Bits integrierte Windows-Datei, um den Inhalt aus dem CDN herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="f27e3-275">By default, the Office Click-To-Run installer uses the Windows' built in implementation of BITS to download the content from the CDN.</span></span> 
  
<span data-ttu-id="f27e3-276">Durch die Bereitstellung einer angepassten Bits-Implementierung für die **Download ()** -Methode der **IUpdateNotify** -Schnittstelle kann Ihre Verwaltbarkeit-Software steuern, wo und wie der Client den Inhalt herunterlädt.</span><span class="sxs-lookup"><span data-stu-id="f27e3-276">By providing a customized BITS implementation to the **download()** method of the **IUpdateNotify** interface, your manageability software can control where and how the client downloads the content.</span></span> <span data-ttu-id="f27e3-277">Eine angepasste Bits-Schnittstelle ist nützlich, wenn ein benutzerdefinierter Inhalts Verteilungskanal als die integrierten Klick-und-Los-Kanäle bereitgestellt wird, beispielsweise die Office CDN-, IIS-Server oder Dateifreigaben.</span><span class="sxs-lookup"><span data-stu-id="f27e3-277">A customized BITS interface is useful when providing a custom content distribution channel other than the Click-to-Run built-in channels, such as the Office CDN, IIS servers, or file shares.</span></span> 
  
<span data-ttu-id="f27e3-278">Die Mindestanforderung für eine angepasste Bits-Schnittstelle für die Verwendung des Office C2R-Diensts lautet:</span><span class="sxs-lookup"><span data-stu-id="f27e3-278">The minimum requirement for a customized BITS interface to work with Office C2R service is:</span></span>
  
- <span data-ttu-id="f27e3-279">Für **IBackgroundCopyManager**:</span><span class="sxs-lookup"><span data-stu-id="f27e3-279">For **IBackgroundCopyManager**:</span></span>
    
  ```cpp
  HRESULT _stdcall CreateJob(
                      [in] LPWSTR DisplayName, 
                      [in] BG_JOB_TYPE Type, 
                      [out] GUID* pJobId, 
                      [out] IBackgroundCopyJob** ppJob)
  HRESULT _stdcall GetJob(
                      [in] GUID* jobID, 
                      [out] IBackgroundCopyJob** ppJob)
  HRESULT _stdcall EnumJobs(
                      [in] unsigned long dwFlags, 
                      [out] IEnumBackgroundCopyJobs** ppenum)
  
  ```

- <span data-ttu-id="f27e3-280">Für **IBackgroundCopyJob**:</span><span class="sxs-lookup"><span data-stu-id="f27e3-280">For **IBackgroundCopyJob**:</span></span>
    
  ```cpp
  HRESULT _stdcall AddFile(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName)
  HRESULT _stdcall Resume()
  HRESULT _stdcall Complete()
  HRESULT _stdcall Cancel();
  HRESULT _stdcall GetState([out] BG_JOB_STATE* pVal);
  HRESULT GetProgress( [out] BG_JOB_PROGRESS *pProgress);
  
  ```

- <span data-ttu-id="f27e3-281">Für **IBackgroundCopyJob3**:</span><span class="sxs-lookup"><span data-stu-id="f27e3-281">For **IBackgroundCopyJob3**:</span></span>
    
  ```cpp
  HRESULT _stdcall AddFileWithRanges(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName,
                      [in] DWORD RangeCount,
                      [in] BG_FILE_RANGE Ranges[])
  
  ```

- <span data-ttu-id="f27e3-282">Für die `Addfile` - `AddFileWithRanges` und-Funktionen hat die Remote-URL folgendes Format:</span><span class="sxs-lookup"><span data-stu-id="f27e3-282">For the  `Addfile` and  `AddFileWithRanges` functions, the remote URL is in the following format:</span></span> 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - <span data-ttu-id="f27e3-283">cmbits ist hart codiert und steht für angepasste Bits.</span><span class="sxs-lookup"><span data-stu-id="f27e3-283">cmbits is hard coded, and stands for customized BITS.</span></span>
    
  -  <span data-ttu-id="f27e3-284">Content-Wert ist der _Content_ -Parameter für die **Download ()** -Methode. _ \<\> _</span><span class="sxs-lookup"><span data-stu-id="f27e3-284">_\<contentid\>_ is the  _contentid_ parameter for the **Download()** method.</span></span> 
    
  -  <span data-ttu-id="f27e3-285">_Relative Path to target file\> enthält den Speicherort und den Dateinamen der Datei, die heruntergeladen werden soll. \<_</span><span class="sxs-lookup"><span data-stu-id="f27e3-285">_\<relative path to target file\>_ provides the location and file name of the file to download.</span></span> 
    
    <span data-ttu-id="f27e3-286">Wenn Sie beispielsweise eine _Inhalts_ `f732af58-5d86-4299-abe9-7595c35136ef` -Nr für die **Download ()** -Methode bereitgestellt haben und Office C2R die Version der CAB-Datei (beispielsweise `v32.cab` Datei) herunterladen möchte, wird **AddFile ()** mit folgendem `RemoteUrl`Aufruf aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="f27e3-286">For example, if you have provided a  _contentid_ of  `f732af58-5d86-4299-abe9-7595c35136ef` to the **Download()** method, and Office C2R wants to download the version cab file, such as  `v32.cab` file, it will call **AddFile()** with the following  `RemoteUrl`:</span></span>
    
  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- <span data-ttu-id="f27e3-287">Für **IBackgroundCopyError**:</span><span class="sxs-lookup"><span data-stu-id="f27e3-287">For **IBackgroundCopyError**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- <span data-ttu-id="f27e3-288">Für **IBackgroundCopyFile**:</span><span class="sxs-lookup"><span data-stu-id="f27e3-288">For **IBackgroundCopyFile**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetLocalName([out] LPWSTR *ppName); 
  HRESULT _stdcall GetRemoteName([out] LPWSTR *ppName);
  
  ```

<!--## Automating content staging

IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the Microsoft Content Delivery Network (CDN) or they can choose to control the deployment of updates available from the [update channels](https://docs.microsoft.com/DeployOffice/overview-of-update-channels-for-office-365-proplus) using the [Office 2016 Deployment Tool](https://www.microsoft.com/download/details.aspx?id=49117) or [System Center Configuration Manager](https://docs.microsoft.com/deployoffice/manage-office-365-proplus-updates-with-configuration-manager).
  
The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.
  
**Following is a diagram showing the overview of downloading a custom image**

![An overview of downloading Office updates from the CDN.](media/9afac230-6b22-4526-a800-0562708cc436.png "An overview of downloading Office updates from the CDN")
  
In the above diagram you see that a new Office 365 ProPlus image is available on the Office Content Distribution Network (CDN). Along with the Office 365 ProPlus image, an XML-formatted file list is also available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.
  
An enterprise configures their WSUS to sync the Office 365 Client Updates. These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available. The manageability software can then read the Client Update metadata to understand what version of Office the update applies to.
  
If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.
  
### Format of the XML file list

There are two file lists available in a cab file on the CDN. One lists the files for the 32-bit version of Office and one for the 64-bit version of Office. The URL of the location of the Office File List (OFL.CAB) file is [https://officecdn.microsoft.com/pr/wsus/ofl.cab](https://officecdn.microsoft.com/pr/wsus/ofl.cab). The two file lists are called:
  
- O365Client_32bit.xml
    
- O365Client_64bit.xml
    
Within the XML for each of the file lists is an  `UpdateFiles` node which contains a version attribute.  `UpdateFiles version="1.4"`.
  
This version is incremented if changes are made to the file lists.
  
There are two parameters that need to be combined with the XML to make a custom image: 
  
- Replace  _%version%_ with the build version of Office. This can be derived from the Client Update metadata  `MoreInfoURL` field, see below. 
    
- Define  _baseURL_ by using the URL value associated with the branch the image is being created for. This can be derived from the Client Update metadata, see below. 
    
The steps for creating an image are:
  
1. Open the XML file list.
    
2. Replace occurrences of  _%version%_ with the applicable Office build version. The build version can be acquired from releasehistory.xml as described later in this article. 
    
3. Read the URL attribute for the target branch.
    
4. Remove language nodes for any languages not required in the custom image.
    
   > [!NOTE]
   > Nodes with language='0' are language neutral and must be included in the image. 
  
5. Construct a local image of the CDN by iterating through the XML file list and copying the CDN files, while creating the folder structure as needed. 
    
   - If the  _rename_ attribute is provided, then rename the copied file to the value provided in the  _rename_ attribute. This used to create the top-level default v64.cab and v32.cab files. These are the renamed versions of the top-level build cab file and are used as the default installation version if the version is not specified. 
    
   - Use URL + relativePath + filename to construct the CDN location.
    
The following examples use the Monthly channel (as defined by the  `baseURL` node) and build version 16.0.4229.1004 from releasehistory.xml. 
  
```cpp
baseURL branch="Monthly" URL="https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60" /
```

- The following is a language neutral file needed for all languages. The name of the file is v64_16.0.4229.1004.cab and it should be copied from https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab and renamed to …/office/data/v64.cab.
    
  ```cpp
  baseURL branch="Business" URL="https://officecdn.microsoft.com/pr/7ffbc6bf-bc32-4f92-8982-f9dd17fd3114" /
  File name="v64_%version%.cab" rename="v64.cab" relativePath="/office/data/" language="0"/
  
  ```

- The following is a file to be included in the en-US image as designated by the language LCID=1033. The name of the file is s641033.cab and it should be copied from https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab and not renamed.
    
  ```cpp
  File name="s641033.cab" relativePath="/office/data/%version%/" language="1033" /
  ```

### Hash verification of data files

Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed HASH value with the supplied HASH value associated with each of the .dat files. Below is an example of a .dat file from the Monthly channel with build version 16.0.4229.1004 and language set to Bulgarian.
  
```cpp
File name="stream.x64.bg-bg.dat" hashLocation="s641026.cab/stream.x64.bg-bg.hash" hashAlgo="Sha256" relativePath="/office/data/%version%/" language="1026"
```

- The  _hashLocation_ attribute specifies the relative path location of the stream.x64.bg-bg.hash for the stream.x64.bg-bg.dat file. Construct the hash file location by concatenating URL + relativePath + hashLocation. In this example the stream.x64.bg-bg.hash location would be https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
    
- The  _hashAlgo_ attribute specifies what hashing algorithm was used. In this case the Sha256 algorithm was used. 
    
To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the hash value from the first line of text in the hash file. Compare this to the has value that you computed using the specified hashing algorithm to verify that the values match. Use the following C# code to read the hash.
  
```cs
string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
string readHash = readHashes.First();

```

### Office 365 Client Updates

Office 365 Client Updates enable manageability software to treat the Office 365 Client Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload. The Office 365 Client Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.
  
**Office 365 Client Update workflow**

![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")
  
Each Office 365 Client Update that is published includes metadata about the update. This metadata includes a parameter called  _MoreInfoUrl_ which can be used to derive the following information: 
  
-  _Ver_: Identifies the Office version associated with this update. For example 16.0.4229.1004.
    
-  _Branch_: Identifies the Update Channel for this update. Values include InsiderFast, Insiders, Monthly, Targeted, Broad. Additional values may be added in the future.
    
-  _Arch_: Identifies the processor architecture associated with this update.
    
-  _xmlVer_: Identifies the version of the XML file lists to use to construct the base image for this update.
    
-  _xmlPath_: Path to the OFL.CAB file that contains the XML file lists.
    
-  _xmlFile_: The name of the file list that should be used for this update. The value will be  `O365Client_32bit` or  `O365Client_64bit` and will match the value in  _Arch_.
    
The following is an example of the  _MoreInfoURL_ parameter which refers to the Office 365 Client Update for the 32-bit version of Office with build version of 16.0.2342.2343 on the Current channel. 
  
```http
https://officecdn.microsoft.com/pr/wsus/ofl.cab is the location of the XML file lists for this update, specifically the O365Client_32bit.xml from within the OFL.CAB.
https://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.8326.2096&Branch=Current&Arch=64&XMLVer=1.4&xmlPath=https://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml 

```
THE ABOVE SECTION APPEARS TO BE A DUPLICATE OF THE FOLLOWING SECTION; TEMPORARILY COMMENTING IT OUT.-->

## <a name="automating-content-staging"></a><span data-ttu-id="f27e3-289">Automatisieren der Inhaltsbereitstellung</span><span class="sxs-lookup"><span data-stu-id="f27e3-289">Automating content staging</span></span>

<span data-ttu-id="f27e3-290">IT-Administratoren können festlegen, dass Desktop Clients automatisch Updates erhalten, wenn Sie direkt im Microsoft Content Delivery Network (CDN) zur Verfügung stehen, oder Sie können auswählen, ob die Bereitstellung von Updates gesteuert werden soll, die im Update verfügbar sind. Kanäle mit dem Office-Bereitstellungs Tool oder System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f27e3-290">IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the Microsoft Content Delivery Network (CDN) or they can choose to control the deployment of updates available from the update channels using the Office Deployment Tool or System Center Configuration Manager.</span></span>
  
<span data-ttu-id="f27e3-291">Der Dienst unterstützt die Möglichkeit für Verwaltungstools, den Download der Inhalte zu erkennen und zu automatisieren, wenn Updates zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f27e3-291">The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.</span></span>
  
<span data-ttu-id="f27e3-292">**Die folgende Abbildung ist eine Übersicht über das Herunterladen eines benutzerdefinierten Bilds.**</span><span class="sxs-lookup"><span data-stu-id="f27e3-292">**The following image is an overview of downloading a custom image**</span></span>

<span data-ttu-id="f27e3-293">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Ein Diagramm zur Verwendung der COM-Schnittstelle im Office-Klick-und-Los-Installationsprogramm")</span><span class="sxs-lookup"><span data-stu-id="f27e3-293">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on  the Office Click-To-Run installer")</span></span>
  
### <a name="overview-of-downloading-a-custom-image"></a><span data-ttu-id="f27e3-294">Übersicht über das Herunterladen eines benutzerdefinierten Bilds</span><span class="sxs-lookup"><span data-stu-id="f27e3-294">Overview of downloading a custom image</span></span>
  
<span data-ttu-id="f27e3-295">Im vorherigen Diagramm sehen Sie, dass ein neues Office 365 ProPlus-Bild im Office-Inhalts Verteilungsnetzwerk (CDN) zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="f27e3-295">In the previous diagram, you see that a new Office 365 ProPlus image is available on the Office Content Distribution Network (CDN).</span></span> <span data-ttu-id="f27e3-296">Zusammen mit dem Office 365 ProPlus-Bild ist auch eine XML-formatierte Dateiliste verfügbar, die über die erforderlichen Informationen verfügt, um die Verwaltbarkeit von Software zu ermöglichen, um direkt angepasste Bilder zu erstellen, die die Verwendung des Office-Bereitstellungstools ersetzen.</span><span class="sxs-lookup"><span data-stu-id="f27e3-296">Along with the Office 365 ProPlus image, an XML-formatted file list is also available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.</span></span>
  
<span data-ttu-id="f27e3-297">Ein Unternehmen konfiguriert seine WSUS so, dass die Office 365 Client Updates synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f27e3-297">An enterprise configures their WSUS to sync the Office 365 Client Updates.</span></span> <span data-ttu-id="f27e3-298">Diese Updates enthalten nicht die tatsächliche Bild Nutzlast, aber die Verwaltungssoftware kann erkennen, wenn neue Inhalte verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f27e3-298">These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available.</span></span> <span data-ttu-id="f27e3-299">Die Verwaltungssoftware kann dann die Client Update Metadaten lesen, um zu verstehen, für welche Version von Office das Update gilt.</span><span class="sxs-lookup"><span data-stu-id="f27e3-299">The manageability software can then read the Client Update metadata to understand what version of Office the update applies to.</span></span>
  
<span data-ttu-id="f27e3-300">Wenn das Update anwendbar ist, kann die Verwaltbarkeit-Software den CDN-Inhalt und die Dateiliste verwenden, um das benutzerdefinierte Abbild zu erstellen und es auf dem Dateifreigabespeicherort zu speichern, der für die Verwendung konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="f27e3-300">If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.</span></span>
  
### <a name="format-of-the-xml-file-list"></a><span data-ttu-id="f27e3-301">Format der XML-Dateiliste</span><span class="sxs-lookup"><span data-stu-id="f27e3-301">Format of the XML file list</span></span>

<span data-ttu-id="f27e3-302">In einer CAB-Datei auf dem CDN stehen zwei Dateilisten zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="f27e3-302">There are two file lists available in a cab file on the CDN.</span></span> <span data-ttu-id="f27e3-303">Eine Liste enthält die Dateien für die 32-Bit-Version von Office und eine für die 64-Bit-Version von Office.</span><span class="sxs-lookup"><span data-stu-id="f27e3-303">One lists the files for the 32-bit version of Office and one for the 64-bit version of Office.</span></span> <span data-ttu-id="f27e3-304">Die URL des Speicherorts der Office-Dateiliste (ofl. CAB)-Datei [https://officecdn.microsoft.com/pr/wsus/ofl.cab](https://officecdn.microsoft.com/pr/wsus/ofl.cab)ist.</span><span class="sxs-lookup"><span data-stu-id="f27e3-304">The URL of the location of the Office File List (OFL.CAB) file is [https://officecdn.microsoft.com/pr/wsus/ofl.cab](https://officecdn.microsoft.com/pr/wsus/ofl.cab).</span></span> <span data-ttu-id="f27e3-305">Die beiden Dateilisten werden aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="f27e3-305">The two file lists are called:</span></span>
  
- <span data-ttu-id="f27e3-306">O365Client_32bit. XML</span><span class="sxs-lookup"><span data-stu-id="f27e3-306">O365Client_32bit.xml</span></span>
    
- <span data-ttu-id="f27e3-307">O365Client_64bit. XML</span><span class="sxs-lookup"><span data-stu-id="f27e3-307">O365Client_64bit.xml</span></span>
    
<span data-ttu-id="f27e3-308">Innerhalb des XML-Code für jede der Dateilisten ist <UpdateFiles> ein Knoten, der ein Version-Attribut enthält.</span><span class="sxs-lookup"><span data-stu-id="f27e3-308">Within the XML for each of the file lists is an <UpdateFiles> node which contains a version attribute.</span></span>  <span data-ttu-id="f27e3-309">`<UpdateFiles version="1.4">`.</span><span class="sxs-lookup"><span data-stu-id="f27e3-309"></span></span> <span data-ttu-id="f27e3-310">Diese Version wird inkrementiert, wenn Änderungen an den Dateilisten vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="f27e3-310">This version is incremented if changes are made to the file lists.</span></span>
  
<span data-ttu-id="f27e3-311">Es gibt zwei Parameter, die mit dem XML-Code kombiniert werden müssen, um ein benutzerdefiniertes Bild zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="f27e3-311">There are two parameters that need to be combined with the XML to make a custom image:</span></span> 
  
- <span data-ttu-id="f27e3-312">Ersetzen Sie *% Version%* durch die Buildversion von Office.</span><span class="sxs-lookup"><span data-stu-id="f27e3-312">Replace  *%version%*  with the build version of Office.</span></span> <span data-ttu-id="f27e3-313">Dies kann von den Client Update-Metadaten abgeleitet werden (siehe nächster Abschnitt).</span><span class="sxs-lookup"><span data-stu-id="f27e3-313">This can be derived from the Client Update metadata (explained in the next section).</span></span> 
    
- <span data-ttu-id="f27e3-314">Definieren Sie *baseURL* mit dem URL-Wert, der der Verzweigung zugeordnet ist, für die das Bild erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f27e3-314">Define  *baseURL*  by using the URL value associated with the branch the image is being created for.</span></span> <span data-ttu-id="f27e3-315">Dies wird von den Client Update-Metadaten abgeleitet, die im folgenden Abschnitt erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="f27e3-315">This is derived from the Client Update metadata, explained in the following section.</span></span> 
    
<span data-ttu-id="f27e3-316">Die Schritte zum Erstellen eines Bilds lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f27e3-316">The steps for creating an image are:</span></span>
  
1. <span data-ttu-id="f27e3-317">Öffnen Sie die Liste XML-Datei.</span><span class="sxs-lookup"><span data-stu-id="f27e3-317">Open the XML file list.</span></span>
    
2. <span data-ttu-id="f27e3-318">Ersetzen Sie Vorkommen von *% Version%* durch die entsprechende Office Build-Version.</span><span class="sxs-lookup"><span data-stu-id="f27e3-318">Replace occurrences of  *%version%*  with the applicable Office build version.</span></span> <span data-ttu-id="f27e3-319">Die Buildversion kann aus releasehistory. XML abgerufen werden, wie weiter unten in diesem Artikel beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f27e3-319">The build version can be acquired from releasehistory.xml as described later in this article.</span></span> 
    
3. <span data-ttu-id="f27e3-320">Lesen Sie das URL-Attribut für die Zielverzweigung.</span><span class="sxs-lookup"><span data-stu-id="f27e3-320">Read the URL attribute for the target branch.</span></span>
    
4. <span data-ttu-id="f27e3-321">Entfernen Sie Sprachknoten für alle Sprachen, die im benutzerdefinierten Bild nicht erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f27e3-321">Remove language nodes for any languages not required in the custom image.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="f27e3-322">Knoten mit Sprache = ' 0 ' sind sprachneutral und müssen in das Bild aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="f27e3-322">Nodes with language='0' are language neutral and must be included in the image.</span></span> 
  
5. <span data-ttu-id="f27e3-323">Erstellen Sie ein lokales Image des CDN, indem Sie die XML-Dateiliste durchlaufen und die CDN-Dateien kopieren, während Sie die Ordnerstruktur nach Bedarf erstellen.</span><span class="sxs-lookup"><span data-stu-id="f27e3-323">Construct a local image of the CDN by iterating through the XML file list and copying the CDN files, while creating the folder structure as needed.</span></span> 
    
   - <span data-ttu-id="f27e3-324">Wenn das Attribut *Rename* angegeben wird, *benennen* Sie die kopierte Datei in den im Attribut Rename angegebenen Wert um.</span><span class="sxs-lookup"><span data-stu-id="f27e3-324">If the  *rename*  attribute is provided, then  *rename*  the copied file to the value provided in the rename attribute.</span></span> <span data-ttu-id="f27e3-325">Dies wird verwendet, um die standardmäßigen V64. cab-und V32. CAB-Dateien auf oberster Ebene zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f27e3-325">This is used to create the top-level default v64.cab and v32.cab files.</span></span> <span data-ttu-id="f27e3-326">Hierbei handelt es sich um die umbenannten Versionen der Build-CAB-Datei auf oberster Ebene, die als Standard Installationsversion verwendet werden, wenn die Version nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="f27e3-326">These are the renamed versions of the top-level build cab file and are used as the default installation version if the version is not specified.</span></span> 
    
   - <span data-ttu-id="f27e3-327">Verwenden Sie URL + relativePath + filename, um den CDN-Speicherort zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f27e3-327">Use URL + relativePath + filename to construct the CDN location.</span></span>
    
<span data-ttu-id="f27e3-328">Im folgenden sind Beispiele aufgeführt, die den monatlichen Kanal (wie vom `<baseURL>` Knoten definiert) und die Buildversion 16.0.4229.1004 aus releasehistory. XML verwenden.</span><span class="sxs-lookup"><span data-stu-id="f27e3-328">The following are examples that use the Monthly channel (as defined by the  `<baseURL>` node) and build version 16.0.4229.1004 from releasehistory.xml.</span></span> 
  
```xml
<baseURL branch="Monthly" URL="https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60" />
```

- <span data-ttu-id="f27e3-329">Im folgenden finden Sie eine sprachneutrale Datei, die für alle Sprachen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f27e3-329">The following is a language neutral file needed for all languages.</span></span> <span data-ttu-id="f27e3-330">Der Name der Datei lautet v64_16.0.4229.1004. cab und sollte aus `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab` kopiert und in `…/office/data/v64.cab`umbenannt werden.</span><span class="sxs-lookup"><span data-stu-id="f27e3-330">The name of the file is v64_16.0.4229.1004.cab and it should be copied from `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab` and renamed to `…/office/data/v64.cab`.</span></span> 
    
  ```xml
  <File name="v64_%version%.cab" rename="v64.cab" relativePath="/office/data/" language="0"/>
  
  ```

- <span data-ttu-id="f27e3-331">Im folgenden finden Sie eine Datei, die in das en-US-Bild aufgenommen werden soll, wie von der Sprache LCID = 1033 angegeben.</span><span class="sxs-lookup"><span data-stu-id="f27e3-331">The following is a file to be included in the en-US image as designated by the language LCID=1033.</span></span> <span data-ttu-id="f27e3-332">Der Name der Datei lautet s641033. cab und sollte aus `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab` kopiert und nicht umbenannt werden.</span><span class="sxs-lookup"><span data-stu-id="f27e3-332">The name of the file is s641033.cab and it should be copied from `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab` and not renamed.</span></span>
    
  ```xml
  <File name="s641033.cab" relativePath="/office/data/%version%/" language="1033" />
  ```

### <a name="hash-verification-of-dat-files"></a><span data-ttu-id="f27e3-333">Hash Überprüfung von DAT-Dateien</span><span class="sxs-lookup"><span data-stu-id="f27e3-333">Hash verification of .dat files</span></span>

<span data-ttu-id="f27e3-334">Bilder Erstellungstools können die Integrität der heruntergeladenen DAT-Dateien überprüfen, indem Sie einen berechneten Hashwert mit dem bereitgestellten Hashwert vergleichen, der den einzelnen DAT-Dateien zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f27e3-334">Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed HASH value with the supplied HASH value associated with each of the .dat files.</span></span> <span data-ttu-id="f27e3-335">Im folgenden finden Sie ein Beispiel für eine DAT-Datei aus dem monatlichen Kanal mit 16.0.4229.1004 der Buildversion und der auf Bulgarisch festgelegten Sprache:</span><span class="sxs-lookup"><span data-stu-id="f27e3-335">Following is an example of a .dat file from the Monthly channel with build version 16.0.4229.1004 and language set to Bulgarian:</span></span>
  
```xml
<File name="stream.x64.bg-bg.dat" hashLocation="s641026.cab/stream.x64.bg-bg.hash" hashAlgo="Sha256" relativePath="/office/data/%version%/" language="1026"/>
```

- <span data-ttu-id="f27e3-336">Das **hashLocation** -Attribut gibt den relativen Pfadspeicherort des Stream.x64.bg-bg. Hash für die Datei Stream.x64.bg-bg. dat an.</span><span class="sxs-lookup"><span data-stu-id="f27e3-336">The **hashLocation** attribute specifies the relative path location of the stream.x64.bg-bg.hash for the stream.x64.bg-bg.dat file.</span></span> <span data-ttu-id="f27e3-337">Erstellen Sie den Speicherort der Hash Datei, indem Sie URL + relativePath + hashLocation verketten.</span><span class="sxs-lookup"><span data-stu-id="f27e3-337">Construct the hash file location by concatenating URL + relativePath + hashLocation.</span></span> <span data-ttu-id="f27e3-338">Im folgenden Beispiel wäre der Speicherort Stream.x64.bg-bg. Hash wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f27e3-338">In the following example, the stream.x64.bg-bg.hash location would be:</span></span> 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- <span data-ttu-id="f27e3-339">Das **hashAlgo** -Attribut gibt an, welcher Hashalgorithmus verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f27e3-339">The **hashAlgo** attribute specifies what hashing algorithm was used.</span></span> <span data-ttu-id="f27e3-340">In diesem Fall wurde SHA256 verwendet.</span><span class="sxs-lookup"><span data-stu-id="f27e3-340">In this case Sha256 was used.</span></span> 
    
  <span data-ttu-id="f27e3-341">Um die Integrität der Datei Stream.x64.bg-bg. dat zu überprüfen, öffnen Sie den Stream.x64.bg-bg. Hash und lesen Sie den Hashwert, der die erste Textzeile in der Hash Datei ist.</span><span class="sxs-lookup"><span data-stu-id="f27e3-341">To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the HASH value which is the first line of text in the hash file.</span></span> <span data-ttu-id="f27e3-342">Vergleichen Sie diesen Wert mit dem berechneten Hashwert (mithilfe des angegebenen Hashalgorithmus), um die Integrität der heruntergeladenen DAT-Datei zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f27e3-342">Compare this to the computed hash value (using the specified hashing algorithm) to verify the integrity of the downloaded .dat file.</span></span>
    
  <span data-ttu-id="f27e3-343">Im folgenden Beispiel wird der C#-Code zum Lesen des Hashs gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f27e3-343">The following example shows the C# code to read the hash.</span></span>
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="office-365-client-updates"></a><span data-ttu-id="f27e3-344">Office 365 von Client Updates</span><span class="sxs-lookup"><span data-stu-id="f27e3-344">Office 365 Client Updates</span></span>

<span data-ttu-id="f27e3-345">Alle Office 365 Client Updates werden im [Microsoft Update-Katalog](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client)veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="f27e3-345">All Office 365 Client Updates are published to the [Microsoft Update Catalog](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span></span>
  
<span data-ttu-id="f27e3-346">Mit Office 365 Clientupdates kann die Verwaltbarkeit von Software für die Office 365-Clientupdates auf eine Art und Weise behandelt werden, die mit einer Ausnahme ähnlich wie bei anderen Wu-Updates aussieht. die Clientupdates enthalten keine tatsächliche Nutzlast.</span><span class="sxs-lookup"><span data-stu-id="f27e3-346">Office 365 Client Updates enable manageability software to treat the Office 365 Client Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload.</span></span> <span data-ttu-id="f27e3-347">Die Office 365 Client Updates sollten nicht auf allen Clients installiert werden, sondern verwendet werden, um die Workflows mit der Verwaltungssoftware auszulösen, die den Installationsbefehl durch den oben gezeigten com-basierten Installationsmechanismus ersetzt.</span><span class="sxs-lookup"><span data-stu-id="f27e3-347">The Office 365 Client Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.</span></span> 
  
<span data-ttu-id="f27e3-348">**In der folgenden Abbildung ist ein Diagramm des Office 365-Client Update Workflows dargestellt.**</span><span class="sxs-lookup"><span data-stu-id="f27e3-348">**The following figure shows a diagram of the Office 365 Client Update workflow.**</span></span>

<span data-ttu-id="f27e3-349">![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow Diagramm für O365PP-Clientupdates")</span><span class="sxs-lookup"><span data-stu-id="f27e3-349">![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")</span></span>
  
<span data-ttu-id="f27e3-350">Jedes Office 365-Client Update, das veröffentlicht wird, enthält Metadaten zum Update.</span><span class="sxs-lookup"><span data-stu-id="f27e3-350">Each Office 365 Client Update that is published includes metadata about the update.</span></span> <span data-ttu-id="f27e3-351">Diese Metadaten enthalten einen Parameter namens *MoreInfoUrl* , der verwendet werden kann, um die folgenden Informationen abzuleiten:</span><span class="sxs-lookup"><span data-stu-id="f27e3-351">This metadata includes a parameter called  *MoreInfoUrl*  which can be used to derive the following information:</span></span> 
  
-  <span data-ttu-id="f27e3-352">*Ver*: gibt die Office-Version an, die diesem Update zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f27e3-352">*Ver*: Identifies the Office version associated with this update.</span></span> 
    
-  <span data-ttu-id="f27e3-353">*Branch*: identifiziert den Update Kanal für dieses Update.</span><span class="sxs-lookup"><span data-stu-id="f27e3-353">*Branch*: Identifies the Update Channel for this update.</span></span> <span data-ttu-id="f27e3-354">Zu den Werten zählen InsiderFast, Insider, Monthly, Targeted, Broad.</span><span class="sxs-lookup"><span data-stu-id="f27e3-354">Values include InsiderFast, Insiders, Monthly, Targeted, Broad.</span></span> <span data-ttu-id="f27e3-355">Weitere Werte können in der Zukunft hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f27e3-355">Additional values may be added in the future.</span></span> 
    
-  <span data-ttu-id="f27e3-356">*Arch*: identifiziert die Prozessorarchitektur, die diesem Update zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f27e3-356">*Arch*: Identifies the processor architecture associated with this update.</span></span> 
    
-  <span data-ttu-id="f27e3-357">*xmlVer*: die Version der XML-Dateilisten, die zum Erstellen des Basis Bilds für dieses Update verwendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="f27e3-357">*xmlVer*: The version of the XML file lists that should be used to construct the base image for this update.</span></span> 
    
-  <span data-ttu-id="f27e3-358">*xmlpath*: Pfad zum ofl. CAB-Datei, die die XML-Dateilisten enthält.</span><span class="sxs-lookup"><span data-stu-id="f27e3-358">*xmlPath*: Path to the OFL.CAB file which contains the XML file lists.</span></span> 
    
-  <span data-ttu-id="f27e3-359">*mlFile*: der Name der Dateiliste, die für dieses Update verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f27e3-359">*mlFile*: The name of the file list that should be used for this update.</span></span> <span data-ttu-id="f27e3-360">Der Wert ist O365Client_32bit oder O365Client_64bit und wird mit dem Bogen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="f27e3-360">The value will be O365Client_32bit or O365Client_64bit and will match the Arch.</span></span> 
    
<span data-ttu-id="f27e3-361">Die folgende URL ist ein Beispiel für den *MoreInfoUrl* -Parameter, der auf die Office 365 Client Updateversionen für die 32-Bit-Version von Office mit der Buildversion von 16.0.2342.2343 im aktuellen Kanal verweist.</span><span class="sxs-lookup"><span data-stu-id="f27e3-361">The following URL is an example of the  *MoreInfoURL*  parameter which refers to the Office 365 client update releases for the 32-bit version of Office with build version of 16.0.2342.2343 on the Current channel.</span></span> 
  
<span data-ttu-id="f27e3-362">https://officecdn.microsoft.com/pr/wsus/ofl.cabist der Speicherort der XML-Dateilisten für dieses Update, insbesondere die O365Client_32bit. XML in der ofl. CAB.</span><span class="sxs-lookup"><span data-stu-id="f27e3-362">https://officecdn.microsoft.com/pr/wsus/ofl.cab is the location of the XML file lists for this update, specifically the O365Client_32bit.xml from within the OFL.CAB.</span></span>
  
[<span data-ttu-id="f27e3-363">Office 365-Clientupdate-Kanalversionen</span><span class="sxs-lookup"><span data-stu-id="f27e3-363">Office 365 client update channel releases</span></span>](https://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.8326.2096&Branch=Current&Arch=64&XMLVer=1.4&xmlPath=https://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml)
  
### <a name="additional-metadata-for-automating-content-staging"></a><span data-ttu-id="f27e3-364">Zusätzliche Metadaten zum Automatisieren der Inhaltsbereitstellung</span><span class="sxs-lookup"><span data-stu-id="f27e3-364">Additional metadata for automating content staging</span></span>

<span data-ttu-id="f27e3-365">Zusätzlich zu den veröffentlichten Metadaten, die definieren, gibt es auch zusätzliche XML-Dateien, die im CDN veröffentlicht werden und zusätzliche Informationen zu den Office 365 Clients bereitstellen können, die im Office CDN zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="f27e3-365">In addition to the metadata that is published which defines there are also additional XML files published to the CDN that can help provide additional information about the Office 365 clients that are available from the Office CDN.</span></span>
  
<span data-ttu-id="f27e3-366">**SKUs. XML**</span><span class="sxs-lookup"><span data-stu-id="f27e3-366">**SKUS.XML**</span></span>
  
<span data-ttu-id="f27e3-367">Diese XML-Datei ist in einem signierten CAB-Code enthalten und wird im Office CDN unter der [https://officecdn.microsoft.com/pr/wsus/skus.cab](https://officecdn.microsoft.com/pr/wsus/skus.cab)folgenden URL veröffentlicht:.</span><span class="sxs-lookup"><span data-stu-id="f27e3-367">This XML file is contained within a signed CAB and published to the Office CDN at the following URL: [https://officecdn.microsoft.com/pr/wsus/skus.cab](https://officecdn.microsoft.com/pr/wsus/skus.cab).</span></span>
  
<span data-ttu-id="f27e3-368">Die in dieser XML-Datei veröffentlichten Metadaten sind nützlich, um zu ermitteln, welche Produkte für die Bereitstellung und Wartung aus dem Office CDN zur Verfügung stehen, zusammen mit verschiedenen Optionen.</span><span class="sxs-lookup"><span data-stu-id="f27e3-368">The metadata published in this XML file is useful for determining which products are available for deployment and servicing from the Office CDN along with various options for each.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<ReleaseInfo PublishedDate="08/07/2017 16:34">
  <!-- Suite / App catalog -->
  <Suite>
    <SKU Name="Office 365 ProPlus" ProductID="O365ProPlusRetail" Default="True">
      <Apps>
        <App Name="Access" AppID="Access" />
        <App Name="Excel" AppID="Excel" />
        <App Name="OneDrive for Business (Groove)" AppID="Groove" />
        <App Name="OneDrive for Business (Next Gen Sync Client)" AppID="OneDrive" />
        <App Name="OneNote" AppID="OneNote" />
        <App Name="Outlook" AppID="Outlook" />
        <App Name="PowerPoint" AppID="PowerPoint" />
        <App Name="Publisher" AppID="Publisher" />
        <App Name="Skype for Business" AppID="Lync" />
        <App Name="Word" AppID="Word" />
      </Apps>
      <Channels>
        <Channel ID="Monthly"/>
        <Channel ID="Insiders"/>
        <Channel ID="Targeted"/>
        <Channel ID="Broad"/>
      </Channels>
    </SKU>
```

<span data-ttu-id="f27e3-369">ReleaseInfo-Stammknoten enthält das PublishedDate-Attribut, das das Datum angibt, an dem diese Datei veröffentlicht wurde. \*\* \<\> \*\*</span><span class="sxs-lookup"><span data-stu-id="f27e3-369">**\<ReleaseInfo\>** root node contains the PublishedDate attribute which identifies the date which this file was published.</span></span> 
  
<span data-ttu-id="f27e3-370">SKU-Knoten identifiziert eine einzelne SKU. \*\* \<\> \*\*</span><span class="sxs-lookup"><span data-stu-id="f27e3-370">**\<SKU\>** node identifies an individual SKU.</span></span> 
  
- <span data-ttu-id="f27e3-371">Das *ProductID* -Attribut identifiziert die ID, die als ID-Attribut in der Datei Configuration. XML übergeben wird, wenn das ODT verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f27e3-371">The  *ProductID*  attribute identifies the ID that is passed as the ID attribute in the configuration.xml if using the ODT.</span></span> <span data-ttu-id="f27e3-372">Beispiel: `<Product ID="O365ProPlusRetail">`.</span><span class="sxs-lookup"><span data-stu-id="f27e3-372">For example, `<Product ID="O365ProPlusRetail">`.</span></span> 
    
- <span data-ttu-id="f27e3-373">Das *Standard* Attribut, bei Festlegung auf "true", gibt die empfohlene SKU an.</span><span class="sxs-lookup"><span data-stu-id="f27e3-373">The  *Default*  attribute, if set to True, identifies the recommended SKU.</span></span> 
    
<span data-ttu-id="f27e3-374">App-Knoten werden verwendet, um die einzelnen Office-Apps zu definieren, die jede SKU unterstützt. \*\* \<\> \*\*</span><span class="sxs-lookup"><span data-stu-id="f27e3-374">**\<App\>** nodes are used to define the individual Office apps that each SKU supports.</span></span> 
  
- <span data-ttu-id="f27e3-375">Das *Name* -Attribut ist der angezeigte Anwendungsname.</span><span class="sxs-lookup"><span data-stu-id="f27e3-375">The  *Name*  attribute is the displayed application name.</span></span> 
    
- <span data-ttu-id="f27e3-376">Bei Verwendung des ODT-Attributs handelt es sich um das ID *-Attribut,* das in der Datei Configuration. XML für den \*\* \<ExcludeApp\> \*\* -Knoten übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f27e3-376">The  *AppID*  attribute is the ID attribute passed in the configuration.xml for the **\<ExcludeApp\>** node if using the ODT.</span></span> <span data-ttu-id="f27e3-377">Beispiel: `<ExcludeApp ID="Publisher" />`.</span><span class="sxs-lookup"><span data-stu-id="f27e3-377">For example, `<ExcludeApp ID="Publisher" />`.</span></span> 
    
<span data-ttu-id="f27e3-378">**RELEASEHISTORY. XML**</span><span class="sxs-lookup"><span data-stu-id="f27e3-378">**RELEASEHISTORY.XML**</span></span>
  
<span data-ttu-id="f27e3-379">Diese XML-Datei ist in einem signierten CAB-Code enthalten und wird im Office CDN an folgendem Speicherort veröffentlicht: [https://officecdn.microsoft.com/pr/wsus/releasehistory.cab](https://officecdn.microsoft.com/pr/wsus/releasehistory.cab).</span><span class="sxs-lookup"><span data-stu-id="f27e3-379">This XML file is contained within a signed CAB and published to the Office CDN at the following location: [https://officecdn.microsoft.com/pr/wsus/releasehistory.cab](https://officecdn.microsoft.com/pr/wsus/releasehistory.cab).</span></span> 
  
<span data-ttu-id="f27e3-380">Die in dieser XML-Datei veröffentlichten Metadaten sind nützlich, um zu ermitteln, welche Kanäle für die Wartung von Updates aus dem Office CDN unterstützt werden, zusammen mit Informationen zum Build-Verlauf für jeden der unterstützten Kanäle.</span><span class="sxs-lookup"><span data-stu-id="f27e3-380">The metadata published in this XML file is useful for determining which channels are supported for servicing updates from the Office CDN along with information about the build history for each of the supported channels.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<ReleaseHistory PublishedDate="10/22/2017 00:48">
  <UpdateChannel Name="Current" ID="Monthly" DisplayName="Monthly Channel">
    <Update Latest="True" Version="1709" LegacyVersion="16.0.8528.2139" Build="8528.2139" PubTime="2017-10-16T19:45:50.743Z" />
    <Update Latest="False" Version="1708" LegacyVersion="16.0.8431.2107" Build="8431.2107" PubTime="2017-10-11T01:52:33.793Z" />
    <Update Latest="False" Version="1708" LegacyVersion="16.0.8431.2079" Build="8431.2079" PubTime="2017-09-18T22:26:13.673Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2107" Build="8326.2107" PubTime="2017-09-12T18:56:53.657Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2096" Build="8326.2096" PubTime="2017-08-30T00:10:25.253Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2076" Build="8326.2076" PubTime="2017-08-19T00:13:01.787Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2073" Build="8326.2073" PubTime="2017-08-11T19:35:42.173Z" />
  </UpdateChannel>
```

<span data-ttu-id="f27e3-381">Der \*\* \<ReleaseHistory\> \*\* -Stammknoten enthält das PublishedDate-Attribut, das das Datum angibt, an dem diese Datei veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="f27e3-381">The **\<ReleaseHistory\>** root node contains the PublishedDate attribute which identifies the date which this file was published.</span></span> 
  
<span data-ttu-id="f27e3-382">Der \*\* \<UpdateChannel\> \*\* -Knoten definiert einen unterstützten Kanal.</span><span class="sxs-lookup"><span data-stu-id="f27e3-382">The **\<UpdateChannel\>** node defines a supported channel.</span></span> 
  
- <span data-ttu-id="f27e3-383">Das *Name* -Attribut definiert die Kanal-ID, die verwendet wird, um in der Datei Configuration. XML als Kanal Attribut an das ODT zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="f27e3-383">The  *Name*  attribute defines the channel ID which is used to pass to the ODT in the configuration.xml as the Channel attribute.</span></span> 
    
  <span data-ttu-id="f27e3-384">Beispiel: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Current">`</span><span class="sxs-lookup"><span data-stu-id="f27e3-384">Example: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Current">`</span></span> 
    
  > [!NOTE] 
  > <span data-ttu-id="f27e3-385">Dieses Attribut ist veraltet und wird nur aus Gründen der Abwärtskompatibilität verwendet.</span><span class="sxs-lookup"><span data-stu-id="f27e3-385">This attribute has been deprecated and is used for backward compatibility only.</span></span> <span data-ttu-id="f27e3-386">Verwenden Sie das ID-Attribut anstelle des Name-Attributs.</span><span class="sxs-lookup"><span data-stu-id="f27e3-386">Use the ID attribute in place of the Name attribute.</span></span> 
    
- <span data-ttu-id="f27e3-387">Das *ID-* Attribut definiert die Kanal-ID, die verwendet wird, um in der Datei Configuration. XML als Kanal Attribut an das ODT zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="f27e3-387">The  *ID*  attribute defines the channel ID which is used to pass to the ODT in the configuration.xml as the Channel attribute.</span></span> 
    
  <span data-ttu-id="f27e3-388">Beispiel: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Deferred">`</span><span class="sxs-lookup"><span data-stu-id="f27e3-388">Example: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Deferred">`</span></span> 
    
- <span data-ttu-id="f27e3-389">Das **Display** Name-Attribut wird als Anzeigename verwendet.</span><span class="sxs-lookup"><span data-stu-id="f27e3-389">The **DisplayName**  attribute is used as the display name.</span></span> 
    
<span data-ttu-id="f27e3-390">Der \*\* \<Knoten\> Update\*\* wird verwendet, um jedes Update zu definieren, das für diesen bestimmten Kanal veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="f27e3-390">The **\<Update\>** node is used to define each update that has been published for that particular channel.</span></span> 
  
- <span data-ttu-id="f27e3-391">Bei Festlegung auf "true" definiert das **neueste** Attribut die Version, die die neueste Version dieses Kanals ist.</span><span class="sxs-lookup"><span data-stu-id="f27e3-391">The **Latest**  attribute, if set to True, defines the release that is the latest release for that channel.</span></span> 
    
- <span data-ttu-id="f27e3-392">Das **Version** -Attribut definiert die Versionsnummer für diese bestimmte Aktualisierung.</span><span class="sxs-lookup"><span data-stu-id="f27e3-392">The **Version** attribute defines the version number for this particular update.</span></span> 
    
- <span data-ttu-id="f27e3-393">Das **LegacyVersion** -Attribut definiert die vollständige Versionsnummer für diese bestimmte Aktualisierung.</span><span class="sxs-lookup"><span data-stu-id="f27e3-393">The **LegacyVersion** attribute defines the full version number for this particular update.</span></span> 
    
- <span data-ttu-id="f27e3-394">Das **Build** -Attribut definiert die Buildnummer für dieses bestimmte Update.</span><span class="sxs-lookup"><span data-stu-id="f27e3-394">The **Build** attribute defines the build number for this particular update.</span></span> 
    
- <span data-ttu-id="f27e3-395">Das **PubTime** -Attribut definiert das Datum und die Uhrzeit, zu der dieses Update im Office CDN veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="f27e3-395">The **PubTime** attribute defines the date and time at which this update was published to the Office CDN.</span></span> 
    

