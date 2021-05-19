---
title: Integrieren von Verwaltbarkeitsanwendungen Microsoft 365 Apps Klick-und-Ausführen-Installationsprogramm
manager: lindalu
ms.date: 09/28/2020
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Erfahren Sie, wie Sie Microsoft 365 Apps Klick-und-Ausführen-Installationsprogramm in eine Softwareverwaltungslösung integrieren.
ms.openlocfilehash: eccd634f7906acf25b521ed2deb456ca914f37da
ms.sourcegitcommit: c8c51bd3f51c0a59fe44c014c8e56f1ba7c7aa03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "48297314"
---
# <a name="integrating-manageability-applications-with-microsoft-365-apps-click-to-run-installer"></a><span data-ttu-id="2afef-103">Integrieren von Verwaltbarkeitsanwendungen Microsoft 365 Apps Klick-und-Ausführen-Installationsprogramm</span><span class="sxs-lookup"><span data-stu-id="2afef-103">Integrating manageability applications with Microsoft 365 Apps Click-to-Run installer</span></span>

<span data-ttu-id="2afef-104">Erfahren Sie, wie Sie Microsoft 365 Apps Klick-und-Ausführen-Installationsprogramm in eine Softwareverwaltungslösung integrieren.</span><span class="sxs-lookup"><span data-stu-id="2afef-104">Learn how to integrate the Microsoft 365 Apps Click-to-Run installer with a software management solution.</span></span>
  
<span data-ttu-id="2afef-105">Das Microsoft 365 Apps -Klick-und-Ausführen-Installationsprogramm bietet eine COM-Schnittstelle, die IT-Experten und Softwareverwaltungslösungen programmgesteuerte Kontrolle über die Updateverwaltung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="2afef-105">The Microsoft 365 Apps Click-to-Run installer provides a COM interface that allows IT Professionals and software management solutions programmatic control over update management.</span></span> <span data-ttu-id="2afef-106">Diese Schnittstelle bietet zusätzliche Verwaltungsfunktionen, die über die vom Bereitstellungstool bereitgestellten Office hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="2afef-106">This interface provides additional management capabilities beyond what is provided by the Office Deployment Tool.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2afef-107">Dieser Artikel gilt für Office Apps, die das Click-to-Run-Installationsprogramm verwenden.</span><span class="sxs-lookup"><span data-stu-id="2afef-107">This article applies to Office apps that use the Click-to-Run installer.</span></span> 
  
## <a name="integrating-with-the-click-to-run"></a><span data-ttu-id="2afef-108">Integration in das Klick-und-Ausführen</span><span class="sxs-lookup"><span data-stu-id="2afef-108">Integrating with the Click-to-Run</span></span>

<span data-ttu-id="2afef-109">Um diese Schnittstelle zu verwenden, ruft eine Verwaltbarkeitsanwendung die COM-Schnittstelle auf und ruft verfügbar gemachte APIs auf, die direkt mit dem Click-to-Run-Installationsdienst kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="2afef-109">To use this interface, a manageability application invokes the COM interface and calls exposed APIs that communicate directly with the Click-to-Run installation service.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2afef-110">Das Office-Klick-und-Ausführen-Installationsprogramm kann über die Befehlszeile mit Parametern ausgeführt werden, die das Verhalten steuern können, wie in [Office Deployment Tool for Click-to-Run](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool)dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="2afef-110">The Office Click-to-Run installer can be run from the command-line with parameters that can control the behavior, as documented in [Office Deployment Tool for Click-to-Run](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool).</span></span> 
  
<span data-ttu-id="2afef-111">**Nachfolgend finden Sie ein konzeptionelles Diagramm der COM-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="2afef-111">**Following is a conceptual diagram of the COM interface**</span></span>

<span data-ttu-id="2afef-112">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Ein Diagramm der Verwendung der COM-Schnittstelle im Office -Klick-und-Ausführen-Installationsprogramm")</span><span class="sxs-lookup"><span data-stu-id="2afef-112">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on  the Office Click-To-Run installer")</span></span>
  
<span data-ttu-id="2afef-113">Das Microsoft 365 Apps -Klick-und-Ausführen-Installationsprogramm implementiert eine COM-basierte Schnittstelle, **IUpdateNotify** registriert bei CLSID **CLSID_UpdateNotifyObject**.</span><span class="sxs-lookup"><span data-stu-id="2afef-113">The Microsoft 365 Apps Click-to-Run installer implements a COM-based interface, **IUpdateNotify** registered to CLSID **CLSID_UpdateNotifyObject**.</span></span>
  
<span data-ttu-id="2afef-114">Diese Schnittstelle kann wie folgt aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="2afef-114">This interface can be invoked as follows:</span></span>
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

<span data-ttu-id="2afef-115">Der Aufruf ist nur erfolgreich, wenn der Anrufer mit erhöhten Rechten ausgeführt wird, da das Klick-und-Ausführen-Installationsprogramm mit erhöhten Rechten ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="2afef-115">The call will only succeed if the caller is running under elevated privileges, as the Click-to-Run installation program must be run with elevated privileges.</span></span>
  
<span data-ttu-id="2afef-116">Die **IUpdateNotify** -COM-Schnittstelle macht drei asynchrone Funktionen verfügbar, die für die Validierung der Befehle und Parameter und die Planung der Ausführung mit dem Klick-und-Ausführen-Installationsdienst verantwortlich sind.</span><span class="sxs-lookup"><span data-stu-id="2afef-116">The **IUpdateNotify** COM interface exposes three asynchronous functions responsible for validating the commands and parameters and scheduling execution with the Click-to-Run installation service.</span></span> 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

<span data-ttu-id="2afef-117">Eine vierte Methode, **Status**, kann verwendet werden, um Informationen über den Status des zuletzt ausgeführten Befehls oder den Status des aktuell ausgeführten Befehls (d. h. Erfolg, Fehler, detaillierte Fehlercodes) zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2afef-117">A forth method, **Status**, can be used to get information about the status of the last executed command or the status of the currently executing command (i.e. success, failure, detailed error codes).</span></span>
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

<span data-ttu-id="2afef-118">Es gibt vier Zustände, in denen sich der Klick-und-Ausführen-Installationsdienst während seines Lebenszyklus befinden kann, während dessen **IUpdateNotify-Methoden** aufgerufen werden können. Neustart, Leerlauf, Herunterladen und Anwenden.</span><span class="sxs-lookup"><span data-stu-id="2afef-118">There are four states that the Click-to-Run installation service may be in during its lifecycle, during which **IUpdateNotify** methods may be called; Rebooting, Idle, Downloading and Applying.</span></span> 
  
<span data-ttu-id="2afef-119">**Im Folgenden finden Sie das Diagramm com Interface State Machine**</span><span class="sxs-lookup"><span data-stu-id="2afef-119">**Following is the COM Interface State Machine diagram**</span></span>

<span data-ttu-id="2afef-120">![A state diagram for the COM interface.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Ein Zustandsdiagramm für die COM-Schnittstelle")</span><span class="sxs-lookup"><span data-stu-id="2afef-120">![A state diagram for the COM interface.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "A state diagram for the COM interface")</span></span>
  
> [!NOTE]
> <span data-ttu-id="2afef-121">**Neustart:** Wenn der Computer gestartet wird, gibt es einen Zeitraum, zu dem der Klick-und-Ausführen-Installationsprogrammdienst nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="2afef-121">**Rebooting**: When the machine is booting there is a period of time when the Click-to-Run installer service is not available.</span></span> <span data-ttu-id="2afef-122">Ein erfolgreicher Aufruf der Status-Methode nach einem Neustart gibt eUPDATE_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="2afef-122">A successful call to the Status method after a reboot will return eUPDATE_UNKNOWN.</span></span> 
  
<span data-ttu-id="2afef-123">**Leerlauf:** Wenn sich das Click-to-Run-Installationsprogramm im Leerlaufzustand befindet, können Sie dies aufrufen:</span><span class="sxs-lookup"><span data-stu-id="2afef-123">**Idle:** When the Click-to-Run installer is in the idle state, you can call:</span></span> 
  
- <span data-ttu-id="2afef-124">**Apply**: Installieren sie zuvor heruntergeladene Inhalte.</span><span class="sxs-lookup"><span data-stu-id="2afef-124">**Apply**: Install previously downloaded content.</span></span>
    
- <span data-ttu-id="2afef-125">**Cancel**: Gibt  `0x800000e` zurück , "Eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen."</span><span class="sxs-lookup"><span data-stu-id="2afef-125">**Cancel**: Returns  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="2afef-126">**Download**: Lädt neue Inhalte für die spätere Installation auf den Client herunter.</span><span class="sxs-lookup"><span data-stu-id="2afef-126">**Download**: Downloads new content to the client for later installation.</span></span>
    
- <span data-ttu-id="2afef-127">**Status**: Gibt das Ergebnis der letzten abgeschlossenen Aktion oder eine Fehlermeldung zurück, wenn die Aktion zu einem Fehler endete.</span><span class="sxs-lookup"><span data-stu-id="2afef-127">**Status**: Returns the result of the last completed action, or an error message if the action ended in failure.</span></span> <span data-ttu-id="2afef-128">Wenn keine vorherige Aktion vorkommt, **gibt Status**  `eUPDATE_UNKNOWN` zurück.</span><span class="sxs-lookup"><span data-stu-id="2afef-128">If there is no previous action, **Status** returns  `eUPDATE_UNKNOWN`.</span></span>
    
<span data-ttu-id="2afef-129">**Herunterladen:** Wenn sich das Click-to-Run-Installationsprogramm im Downloadstatus befindet, können Sie:</span><span class="sxs-lookup"><span data-stu-id="2afef-129">**Downloading:** When the Click-to-Run installer is in the downloading state, you can call:</span></span> 
  
- <span data-ttu-id="2afef-130">**Apply**: Gibt ein **HRESULT mit** dem Wert  `0x800000e` "Eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen" zurück.</span><span class="sxs-lookup"><span data-stu-id="2afef-130">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="2afef-131">**Abbrechen**: Beendet den Download und entfernt die teilweise heruntergeladenen Inhalte.</span><span class="sxs-lookup"><span data-stu-id="2afef-131">**Cancel**: Stops the download and removes the partially downloaded content.</span></span>
    
- <span data-ttu-id="2afef-132">**Download**: Gibt ein **HRESULT mit** dem Wert  `0x800000e` "Eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen" zurück.</span><span class="sxs-lookup"><span data-stu-id="2afef-132">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="2afef-133">**Status**: **Gibt** DOWNLOAD_WIP zurück, um anzugeben, dass Downloadarbeiten ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2afef-133">**Status**: Returns **DOWNLOAD_WIP** to indicate that download work is in progress.</span></span> 
    
<span data-ttu-id="2afef-134">**Anwenden:** Wenn das Click-to-Run-Installationsprogramm bereits Inhalte heruntergeladen hat:</span><span class="sxs-lookup"><span data-stu-id="2afef-134">**Applying:** When the Click-to-Run installer is in the process of installing previously download content:</span></span> 
  
- <span data-ttu-id="2afef-135">**Apply**: Gibt ein **HRESULT mit** dem Wert  `0x800000e` "Eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen" zurück.</span><span class="sxs-lookup"><span data-stu-id="2afef-135">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="2afef-136">**Cancel**: Gibt  `0x800000e` zurück, die Aktion Anwenden kann nicht abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="2afef-136">**Cancel**: Returns  `0x800000e`, the Apply action cannot be canceled.</span></span>
    
- <span data-ttu-id="2afef-137">**Download**: Gibt ein **HRESULT mit** dem Wert  `0x800000e` "Eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen" zurück.</span><span class="sxs-lookup"><span data-stu-id="2afef-137">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="2afef-138">**Status**: **Gibt** APPLY_WIP zurück, um anzugeben, dass die angewendete Arbeit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2afef-138">**Status**: Returns **APPLY_WIP** to indicate that apply work is in progress.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="2afef-139">Da OfficeC2RCOM ein COM+-Dienst ist und dynamisch geladen wird, müssen Sie **CoCreateInstance** jedes Mal aufrufen, wenn Sie eine Methode für diese Klasse aufrufen, um sicherzustellen, dass Sie das erwartete Ergebnis erhalten.</span><span class="sxs-lookup"><span data-stu-id="2afef-139">Since OfficeC2RCOM is a COM+ service and is dynamically loaded, you need to call **CoCreateInstance** every time you call a method on this class to ensure that you get the expected result.</span></span> <span data-ttu-id="2afef-140">Der COM+-Dienst übert die Erstellung einer neuen Instanz, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2afef-140">The COM+ service will handle creating a new instance if necessary.</span></span> <span data-ttu-id="2afef-141">Wenn eine der Methoden zum ersten Mal aufgerufen wird, wird das **IUpdateNotify-Objekt** von COM+ geladen und in einer der dllhost.exe ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2afef-141">When one of the methods is called for the first time, COM+ will load the **IUpdateNotify** object and run it within one of the dllhost.exe instances.</span></span> <span data-ttu-id="2afef-142">Das neue Objekt bleibt ca. 3 Minuten im Leerlauf aktiv.</span><span class="sxs-lookup"><span data-stu-id="2afef-142">The new object will stay active for about 3 minutes in idle.</span></span> <span data-ttu-id="2afef-143">Wenn innerhalb von drei Minuten nach dem letzten Aufruf ein nachfolgender Aufruf erfolgt, bleibt das **IUpdateNotify-Objekt** geladen, und eine neue Instanz wird nicht erstellt.</span><span class="sxs-lookup"><span data-stu-id="2afef-143">If a subsequent call is made within three minutes of the last call, the **IUpdateNotify** object will remain loaded and a new instance is not created.</span></span> <span data-ttu-id="2afef-144">Wenn innerhalb von drei Minuten kein Aufruf erfolgt, wird das IUpdateNotify-Objekt entladen, und beim nächsten Aufruf wird ein neues **IUpdateNotify-Objekt** erstellt.</span><span class="sxs-lookup"><span data-stu-id="2afef-144">If no call is made within three minutes, the IUpdateNotify object will be unloaded and a new **IUpdateNotify** object will be created when the next call is made.</span></span> 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a><span data-ttu-id="2afef-145">Handbuch zur Com-API-Referenz für das Installationsprogramm mit Klick-und-Ausführen</span><span class="sxs-lookup"><span data-stu-id="2afef-145">Click-to-Run installer COM API reference guide</span></span>

<span data-ttu-id="2afef-146">In der folgenden API-Referenzdokumentation:</span><span class="sxs-lookup"><span data-stu-id="2afef-146">In the following API reference documentation:</span></span>
  
- <span data-ttu-id="2afef-147">Parameter befinden sich in einem Schlüssel-Wert-Paarformat, das durch ein Leerzeichen getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="2afef-147">Parameters are in a key/value pair format separated by a space.</span></span>
    
- <span data-ttu-id="2afef-148">Bei den Parametern wird die Zwischenschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="2afef-148">The parameters are not case-sensitive.</span></span>
    
- <span data-ttu-id="2afef-149">Es ist eine [Liste der Parameter mit](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) Dokumentation verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2afef-149">There is a [list of parameters](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) with documentation available.</span></span> 
    
- <span data-ttu-id="2afef-150">Die Zusammenfassung der IUpdateNotify2-Schnittstelle ist jetzt enthalten.</span><span class="sxs-lookup"><span data-stu-id="2afef-150">Summary of IUpdateNotify2 interface is now included.</span></span>
    
### <a name="apply"></a><span data-ttu-id="2afef-151">Anwenden</span><span class="sxs-lookup"><span data-stu-id="2afef-151">Apply</span></span>

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a><span data-ttu-id="2afef-152">Parameter</span><span class="sxs-lookup"><span data-stu-id="2afef-152">Parameters</span></span>

-  <span data-ttu-id="2afef-153">_displaylevel_: **true,** um den Installationsstatus, einschließlich Fehler, während des Updateprozesses zu zeigen; **false,** um den Installationsstatus, einschließlich Fehler, während des Updatevorgangs auszublenden.</span><span class="sxs-lookup"><span data-stu-id="2afef-153">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="2afef-154">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="2afef-154">The default is **false**.</span></span>
    
-  <span data-ttu-id="2afef-155">_forceappshutdown_: **true,** um zu erzwingen, Office Anwendungen sofort heruntergefahren werden, wenn die **Apply-Aktion** ausgelöst wird; **false,** um zu fehlschlagen, wenn Office anwendungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2afef-155">_forceappshutdown_: **true** to force Office applications to shut down immediately when the **Apply** action is triggered; **false** to fail if any Office applications are running.</span></span> <span data-ttu-id="2afef-156">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="2afef-156">The default is **false**.</span></span> <span data-ttu-id="2afef-157">Weitere [Informationen finden Sie unter](#bk_ApplyRemark) Hinweise.</span><span class="sxs-lookup"><span data-stu-id="2afef-157">See [Remarks](#bk_ApplyRemark) for more information.</span></span> 
    
  <span data-ttu-id="2afef-158">Wenn eine Office ausgeführt wird, wenn die **Apply-Aktion** ausgelöst wird, tritt bei der **Apply-Aktion** in der Regel ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="2afef-158">If any Office application is running when the **Apply** action is triggered, the **Apply** action will usually fail.</span></span> <span data-ttu-id="2afef-159">Wenn  `forceappshutdown=true` sie an die **Apply-Methode** übergeben werden, wird der **OfficeClickToRun-Dienst** die Anwendungen sofort herunterfahren und das Update anwenden.</span><span class="sxs-lookup"><span data-stu-id="2afef-159">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down the applications and apply the update.</span></span> <span data-ttu-id="2afef-160">In diesem Fall kann es zu Datenverlusten für den Benutzer führen.</span><span class="sxs-lookup"><span data-stu-id="2afef-160">The user may experience data loss in this case.</span></span> 
    
#### <a name="return-results"></a><span data-ttu-id="2afef-161">Zurückgeben von Ergebnissen</span><span class="sxs-lookup"><span data-stu-id="2afef-161">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2afef-162">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="2afef-162">**S_OK**</span></span> <br/> |<span data-ttu-id="2afef-163">Die Aktion wurde erfolgreich zur Ausführung an den Click-To-Run-Dienst übermittelt.</span><span class="sxs-lookup"><span data-stu-id="2afef-163">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="2afef-164">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="2afef-164">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="2afef-165">Der Aufrufer wird nicht mit erhöhten Rechten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2afef-165">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="2afef-166">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="2afef-166">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="2afef-167">Ungültige Parameter wurden übergeben.</span><span class="sxs-lookup"><span data-stu-id="2afef-167">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="2afef-168">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="2afef-168">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="2afef-169">Aktion ist derzeit nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="2afef-169">Action is not allowed at this time.</span></span> <span data-ttu-id="2afef-170">Weitere [Informationen finden Sie unter](#bk_ApplyRemark) Hinweise.</span><span class="sxs-lookup"><span data-stu-id="2afef-170">See [Remarks](#bk_ApplyRemark) for more information.</span></span>  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="2afef-171">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2afef-171">Remarks</span></span>

- <span data-ttu-id="2afef-172">Wenn eine Office ausgeführt wird, wenn die **Apply-Aktion** ausgelöst wird, kann die **Apply-Aktion** nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2afef-172">If any Office application is running when the **Apply** action is triggered, the **Apply** action will fail.</span></span> <span data-ttu-id="2afef-173">Wenn Sie an die Apply-Methode übergeben, wird der `forceappshutdown=true` **OfficeClickToRun-Dienst** sofort alle Office heruntergefahren, die ausgeführt werden und das Update anwenden. </span><span class="sxs-lookup"><span data-stu-id="2afef-173">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down any Office applications that are running and apply the update.</span></span> <span data-ttu-id="2afef-174">Dem Benutzer werden möglicherweise Daten angezeigt, da er nicht aufgefordert wird, Änderungen an geöffneten Dokumenten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="2afef-174">The user may experience data as they are not prompted to save changes to open documents..</span></span> 
    
- <span data-ttu-id="2afef-175">Diese Aktion kann nur ausgelöst werden, wenn der COM-Status einer der folgenden Ist:</span><span class="sxs-lookup"><span data-stu-id="2afef-175">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="2afef-176">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="2afef-176">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="2afef-177">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="2afef-177">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="2afef-178">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="2afef-178">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="2afef-179">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="2afef-179">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="2afef-180">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="2afef-180">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="2afef-181">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="2afef-181">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="2afef-182">Wenn Sie die **Apply-Methode** aufrufen, ohne zuvor Inhalte herunterzuladen, wird von der **Apply-Methode** **erfolgreich** berichtet, da sie keine Anwendung erkannt hat und den **Apply-Prozess** erfolgreich abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="2afef-182">If you call the **Apply** method without previously downloading content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
### <a name="cancel"></a><span data-ttu-id="2afef-183">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="2afef-183">Cancel</span></span>

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a><span data-ttu-id="2afef-184">Zurückgeben von Ergebnissen</span><span class="sxs-lookup"><span data-stu-id="2afef-184">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2afef-185">S_OK</span><span class="sxs-lookup"><span data-stu-id="2afef-185">S_OK</span></span>  <br/> |<span data-ttu-id="2afef-186">Die Aktion wurde erfolgreich zur Ausführung an den Klick-und-Ausführen-Dienst übermittelt.</span><span class="sxs-lookup"><span data-stu-id="2afef-186">Action was successfully submitted to the Click-to-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="2afef-187">E_ILLEGAL_METHOD_CALL</span><span class="sxs-lookup"><span data-stu-id="2afef-187">E_ILLEGAL_METHOD_CALL</span></span>  <br/> |<span data-ttu-id="2afef-188">Aktion ist derzeit nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="2afef-188">Action is not allowed at this time.</span></span> <span data-ttu-id="2afef-189">Weitere Informationen [finden Sie](#bk_CancelRemarks) im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="2afef-189">See the [Remarks](#bk_CancelRemarks) section for more information</span></span>  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a><span data-ttu-id="2afef-190">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2afef-190">Remarks</span></span>

- <span data-ttu-id="2afef-191">Diese Methode kann nur ausgelöst werden, wenn die COM-Status-ID **eDOWNLOAD_WIP.**</span><span class="sxs-lookup"><span data-stu-id="2afef-191">This method can only be triggered when the COM status id **eDOWNLOAD_WIP**.</span></span> <span data-ttu-id="2afef-192">Es wird versucht, die aktuelle Downloadaktion abbricht.</span><span class="sxs-lookup"><span data-stu-id="2afef-192">It will attempt to cancel the current download action.</span></span> <span data-ttu-id="2afef-193">Der COM-Status wird in **eDOWNLOAD_CANCELLING** geändert und schließlich in **eDOWNLOAD_CANCELED**.</span><span class="sxs-lookup"><span data-stu-id="2afef-193">The COM status will change to **eDOWNLOAD_CANCELLING** and eventually change to **eDOWNLOAD_CANCELED**.</span></span> <span data-ttu-id="2afef-194">Der COM-Status **gibt** E_ILLEGAL_METHOD_CALL, wenn es zu einem anderen Zeitpunkt ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="2afef-194">The COM status will return **E_ILLEGAL_METHOD_CALL** if triggered at any other time.</span></span> 
    
### <a name="download"></a><span data-ttu-id="2afef-195">Herunterladen</span><span class="sxs-lookup"><span data-stu-id="2afef-195">Download</span></span>

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a><span data-ttu-id="2afef-196">Parameter</span><span class="sxs-lookup"><span data-stu-id="2afef-196">Parameters</span></span>

-  <span data-ttu-id="2afef-197">_displaylevel_: **true,** um den Installationsstatus, einschließlich Fehler, während des Updateprozesses zu zeigen; **false,** um den Installationsstatus, einschließlich Fehler, während des Updatevorgangs auszublenden.</span><span class="sxs-lookup"><span data-stu-id="2afef-197">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="2afef-198">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="2afef-198">The default is **false**.</span></span>
    
-  <span data-ttu-id="2afef-199">_updatebaseurl_: URL zur alternativen Downloadquelle.</span><span class="sxs-lookup"><span data-stu-id="2afef-199">_updatebaseurl_: URL to the alternate download source.</span></span>
    
-  <span data-ttu-id="2afef-200">_updatetoversion_: Die Version, auf die Office aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2afef-200">_updatetoversion_: The version to update Office to.</span></span> <span data-ttu-id="2afef-201">Definieren Sie diesen Parameter, wenn Sie auf eine ältere Version aktualisieren möchten als die derzeit installierte Version.</span><span class="sxs-lookup"><span data-stu-id="2afef-201">Define this parameter if you want to update to an older version than the version that is currently installed.</span></span>
    
-  <span data-ttu-id="2afef-202">_downloadsource_: CLSID der angepassten **IBackgroundCopyManager-Implementierung** (BITS-Manager).</span><span class="sxs-lookup"><span data-stu-id="2afef-202">_downloadsource_: CLSID of the customized **IBackgroundCopyManager** implementation (BITS manager).</span></span> 
    
-  <span data-ttu-id="2afef-203">_contentid_: Identifiziert den Inhalt, der vom Inhaltsserver über den angepassten BITS-Manager heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2afef-203">_contentid_: Identifies the content to download from the content server through the customized BITS manager.</span></span> <span data-ttu-id="2afef-204">Dieser Wert wird zur Interpretation über die BITS-Schnittstelle übergeben.</span><span class="sxs-lookup"><span data-stu-id="2afef-204">This value is passed through the BITS interface for interpretation.</span></span>
    
#### <a name="return-results"></a><span data-ttu-id="2afef-205">Zurückgeben von Ergebnissen</span><span class="sxs-lookup"><span data-stu-id="2afef-205">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2afef-206">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="2afef-206">**S_OK**</span></span> <br/> |<span data-ttu-id="2afef-207">Die Aktion wurde erfolgreich zur Ausführung an den Click-To-Run-Dienst übermittelt.</span><span class="sxs-lookup"><span data-stu-id="2afef-207">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="2afef-208">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="2afef-208">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="2afef-209">Der Aufrufer wird nicht mit erhöhten Rechten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2afef-209">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="2afef-210">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="2afef-210">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="2afef-211">Ungültige Parameter wurden übergeben.</span><span class="sxs-lookup"><span data-stu-id="2afef-211">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="2afef-212">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="2afef-212">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="2afef-213">Aktion ist derzeit nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="2afef-213">Action is not allowed at this time.</span></span> <span data-ttu-id="2afef-214">Weitere [Informationen finden Sie unter](#bk_DownloadRemark) Hinweise.</span><span class="sxs-lookup"><span data-stu-id="2afef-214">See [Remarks](#bk_DownloadRemark) for more information.</span></span>  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="2afef-215">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2afef-215">Remarks</span></span>

- <span data-ttu-id="2afef-216">Sie müssen  _downloadsource und_  _contentid als_ Paar angeben.</span><span class="sxs-lookup"><span data-stu-id="2afef-216">You must specify  _downloadsource_ and  _contentid_ as a pair.</span></span> <span data-ttu-id="2afef-217">Andern falls nicht, gibt die **Download-Methode** einen **fehler E_INVALIDARG** zurück.</span><span class="sxs-lookup"><span data-stu-id="2afef-217">If not, the **Download** method will return an **E_INVALIDARG** error.</span></span> 
    
- <span data-ttu-id="2afef-218">Wenn  _downloadsource,_  _contentid_ und  _updatebaseurl_ bereitgestellt werden,  _wird updatebaseurl_ ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2afef-218">If  _downloadsource_,  _contentid_, and  _updatebaseurl_ are provided,  _updatebaseurl_ will be ignored.</span></span> 
    
- <span data-ttu-id="2afef-219">Diese Aktion kann nur ausgelöst werden, wenn der COM-Status einer der folgenden Ist:</span><span class="sxs-lookup"><span data-stu-id="2afef-219">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="2afef-220">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="2afef-220">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="2afef-221">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="2afef-221">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="2afef-222">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="2afef-222">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="2afef-223">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="2afef-223">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="2afef-224">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="2afef-224">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="2afef-225">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="2afef-225">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="2afef-226">Wenn Sie die **Apply-Methode** ohne zuvor heruntergeladenen Inhalt aufrufen, wird von der **Apply-Methode** **Erfolgreich** berichtet, da sie keine anwendungsfingen erkannt hat und den **Apply-Prozess** erfolgreich abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="2afef-226">If you call the **Apply** method without previously downloaded content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
#### <a name="examples"></a><span data-ttu-id="2afef-227">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2afef-227">Examples</span></span>

- <span data-ttu-id="2afef-228">So laden Sie den Inhalt aus dem angepassten BITS-Manager herunter: Rufen Sie die **download()-Funktion** auf, die die folgenden Parameter übertritt:</span><span class="sxs-lookup"><span data-stu-id="2afef-228">To download the content from the customized BITS manager: Call the **download()** function passing the following parameters:</span></span> 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- <span data-ttu-id="2afef-229">So laden Sie den Inhalt aus Office Content Delivery Network (CDN): Rufen Sie die **download()-Funktion** auf, ohne die Parameter _downloadsource,_ _contentid_ oder _updatebaseurl_ anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2afef-229">To download the content from the Office Content Delivery Network (CDN): Call the **download()** function without specifying the  _downloadsource_,  _contentid_, or  _updatebaseurl_ parameters.</span></span> 
    
- <span data-ttu-id="2afef-230">So laden Sie den Inhalt von einem benutzerdefinierten Speicherort herunter: Rufen Sie die **Download()-Funktion** auf, die den folgenden Parameter übertritt:</span><span class="sxs-lookup"><span data-stu-id="2afef-230">To download the content from a customized location: Call the **download()** function passing the following parameter:</span></span> 
    
  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a><span data-ttu-id="2afef-231">Status</span><span class="sxs-lookup"><span data-stu-id="2afef-231">Status</span></span>

```cpp
typdef struct _UPDATE_STATUS_REPORT
{
    UPDATE_STATUS status;
    UINT error;
    LPCWSTR contentid;
}UPDATE_STATUS_REPORT;
HRESULT status([out] _UPDATE_STATUS_REPORT& pUpdateStatusReport) // Get status of current action
```

#### <a name="parameters"></a><span data-ttu-id="2afef-232">Parameter</span><span class="sxs-lookup"><span data-stu-id="2afef-232">Parameters</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="2afef-233">_pUpdateStatusReport_</span><span class="sxs-lookup"><span data-stu-id="2afef-233">_pUpdateStatusReport_</span></span> <br/> |<span data-ttu-id="2afef-234">Zeiger auf eine UPDATE_STATUS_REPORT Struktur.</span><span class="sxs-lookup"><span data-stu-id="2afef-234">Pointer to an UPDATE_STATUS_REPORT structure.</span></span>  <br/> |
   
#### <a name="return-results"></a><span data-ttu-id="2afef-235">Zurückgeben von Ergebnissen</span><span class="sxs-lookup"><span data-stu-id="2afef-235">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2afef-236">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="2afef-236">**S_OK**</span></span> <br/> |<span data-ttu-id="2afef-237">Die **Status-Methode** gibt immer dieses Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="2afef-237">The **Status** method always returns this result.</span></span> <span data-ttu-id="2afef-238">Überprüfen Sie die  `UPDATE_STATUS_RESULT` Struktur auf den Status der aktuellen Aktion.</span><span class="sxs-lookup"><span data-stu-id="2afef-238">Inspect the  `UPDATE_STATUS_RESULT` structure for the status of the current action.</span></span>  <br/> |
   
#### <a name="remarks"></a><span data-ttu-id="2afef-239">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2afef-239">Remarks</span></span>

- <span data-ttu-id="2afef-240">Das Statusfeld von  `UPDATE_STATUS_REPORT` enthält den Status der aktuellen Aktion.</span><span class="sxs-lookup"><span data-stu-id="2afef-240">The status field of the  `UPDATE_STATUS_REPORT` contains the status of the current action.</span></span> <span data-ttu-id="2afef-241">Einer der folgenden Statuswerte wird zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="2afef-241">One of the following status values is returned:</span></span> 
    
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

- <span data-ttu-id="2afef-242">Wenn der letzte Befehl zu einem Fehler geführt hat, enthält das Fehlerfeld detaillierte  `UPDATE_STATUS_REPORT` Informationen zum Fehler.</span><span class="sxs-lookup"><span data-stu-id="2afef-242">If the last command resulted in an error, the error field of the  `UPDATE_STATUS_REPORT` contains detailed information about the error.</span></span> <span data-ttu-id="2afef-243">Von der Status-Methode werden zwei Typen von **Fehlercodes** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2afef-243">Two types of error codes are returned from the **Status** method.</span></span> 
    
- <span data-ttu-id="2afef-244">Wenn der Fehler kleiner als ist, ist der Fehler einer der folgenden  `UPDATE_ERROR_CODE::eUNKNOWN` vordefinierten Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="2afef-244">If the error less than  `UPDATE_ERROR_CODE::eUNKNOWN`, the error is one of the following pre-defined error codes:</span></span>
    
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

  <span data-ttu-id="2afef-245">Wenn der Rückgabefehlercode größer als der  `UPDATE_ERROR_CODE::eUNKNOWN` **HRESULT eines** fehlgeschlagenen Funktionsaufrufs ist.</span><span class="sxs-lookup"><span data-stu-id="2afef-245">If the return error code is larger than  `UPDATE_ERROR_CODE::eUNKNOWN` it is the **HRESULT** of a failed function call.</span></span> <span data-ttu-id="2afef-246">So extrahieren Sie das HRESULT-Subtrahieren aus dem wert, der  `UPDATE_ERROR_CODE::eUNKNOWN` im Fehlerfeld der zurückgegeben  `UPDATE_STATUS_REPORT` wird.</span><span class="sxs-lookup"><span data-stu-id="2afef-246">To extract the HRESULT subtract  `UPDATE_ERROR_CODE::eUNKNOWN` from the value returned in the error field of the  `UPDATE_STATUS_REPORT`.</span></span>
    
  <span data-ttu-id="2afef-247">Die vollständige Liste der Status- und Fehlerwerte kann durch Überprüfen der **IUpdateNotify-Typbibliothek** angezeigt werden, die in die OfficeC2RCom.dll.</span><span class="sxs-lookup"><span data-stu-id="2afef-247">The complete list of status and error values can be viewed by inspecting the **IUpdateNotify** type library embedded in OfficeC2RCom.dll.</span></span> 
    
- <span data-ttu-id="2afef-248">Das Feld contentid wird für Aufrufe von **Status** verwendet, nachdem **Download** initiiert wurde, und gibt die contentid zurück, die an den **Downloadaufruf übergeben** wurde.</span><span class="sxs-lookup"><span data-stu-id="2afef-248">The contentid field is used for calls to **Status** after **Download** has initiated and returns the contentid that was passed in to the **Download** call.</span></span> <span data-ttu-id="2afef-249">Es ist eine bewährte Methode, dieses Feld auf **NULL zu initialisieren,** bevor Sie die **Status-Methode** aufrufen und dann den Wert überprüfen, nachdem **Status** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="2afef-249">It is a best practice to initialize this field to **null** before you call the **Status** method and then check the value after **Status** has been returned.</span></span> <span data-ttu-id="2afef-250">Wenn der Wert immer noch **null** ist, bedeutet dies, dass keine contentid zurückgegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="2afef-250">If the value is still **null**, that means there is no contentid to return.</span></span> <span data-ttu-id="2afef-251">Wenn der Wert nicht **null** ist, müssen Sie ihn mit einem Aufruf von **SysFreeString() frei machen.**</span><span class="sxs-lookup"><span data-stu-id="2afef-251">If the value is not **null**, you need to free it with a call to **SysFreeString()**.</span></span> <span data-ttu-id="2afef-252">Hier ist ein Codeausschnitt zum Aufrufen von **Status** nach **Download**.</span><span class="sxs-lookup"><span data-stu-id="2afef-252">Here is a code snippet of how to call **Status** after **Download**.</span></span>
    
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

### <a name="summary-of-iupdatenotify2-interface"></a><span data-ttu-id="2afef-253">Zusammenfassung der IUpdateNotify2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2afef-253">Summary of IUpdateNotify2 interface</span></span>

<span data-ttu-id="2afef-254">Ab Version [16.0.8208.6352] wurde eine neue **IUpdateNotify2-Schnittstelle** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2afef-254">From version [16.0.8208.6352] we have added a new **IUpdateNotify2** interface.</span></span> 
  
- <span data-ttu-id="2afef-255">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span><span class="sxs-lookup"><span data-stu-id="2afef-255">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span></span>
    
- <span data-ttu-id="2afef-256">Diese Schnittstelle hat auch die ursprüngliche IUpdateNotify-Schnittstelle gehostet, um abwärtskompatibel zu sein.</span><span class="sxs-lookup"><span data-stu-id="2afef-256">This interface also hosted the original IUpdateNotify interface to provide backward compatibility.</span></span> <span data-ttu-id="2afef-257">Das heißt, wenn Sie diese Schnittstelle verwenden, haben Sie Zugriff auf alle Methoden, die in der **UpdateNotifyObject-Schnittstelle bereitgestellt** werden.</span><span class="sxs-lookup"><span data-stu-id="2afef-257">Which means if you use this interface, you have access to all the methods provided in **UpdateNotifyObject** interface.</span></span> 
    
- <span data-ttu-id="2afef-258">Neue Methoden, die IUpdateNotify2 hinzugefügt wurden:</span><span class="sxs-lookup"><span data-stu-id="2afef-258">New methods added to IUpdateNotify2:</span></span>
    
  - <span data-ttu-id="2afef-259">**HRESULT** GetBlockingApps([out] BSTR \* AppsList).</span><span class="sxs-lookup"><span data-stu-id="2afef-259">**HRESULT** GetBlockingApps([out] BSTR \* AppsList).</span></span> <span data-ttu-id="2afef-260">Holen Sie sich updates blocking apps list.</span><span class="sxs-lookup"><span data-stu-id="2afef-260">Get updates blocking apps list.</span></span> <span data-ttu-id="2afef-261">Dieser Aufruf gibt die Ausführung Office zurück, die den Updatevorgang blockieren.</span><span class="sxs-lookup"><span data-stu-id="2afef-261">This call will return running Office apps which will block the update process from proceeding.</span></span> 
    
  - <span data-ttu-id="2afef-262">**HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span><span class="sxs-lookup"><span data-stu-id="2afef-262">**HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span></span> <span data-ttu-id="2afef-263">Get Office deployment Data.</span><span class="sxs-lookup"><span data-stu-id="2afef-263">Get Office deployment Data.</span></span> 
    
- <span data-ttu-id="2afef-264">Wenn Sie die neuen Methoden verwenden möchten, müssen Sie sicherstellen, dass:</span><span class="sxs-lookup"><span data-stu-id="2afef-264">If you want to use the new methods, you need to make sure:</span></span>
    
  - <span data-ttu-id="2afef-265">Ihre #A0 ist neuer als der obige Build ( \> = Juni-Fork-Build).</span><span class="sxs-lookup"><span data-stu-id="2afef-265">Your C2R version is newer than the above build (\>= June fork build).</span></span>
    
  - <span data-ttu-id="2afef-266">Verwenden Sie UpdateNotifyObject2 anstelle von **UpdateNotifyObject,** um **CoCreateInstance auf aufruft.**</span><span class="sxs-lookup"><span data-stu-id="2afef-266">Use UpdateNotifyObject2, instead of **UpdateNotifyObject** to call **CoCreateInstance**.</span></span>
    
<span data-ttu-id="2afef-267">Wenn Sie keine der neuen Methoden verwenden, müssen Sie nichts ändern.</span><span class="sxs-lookup"><span data-stu-id="2afef-267">If you don't use any of the new methods, you don't need to change anything.</span></span> <span data-ttu-id="2afef-268">Alle vorhandenen Methoden funktionieren genauso wie zuvor.</span><span class="sxs-lookup"><span data-stu-id="2afef-268">All the existing methods will work as exact the same way as before.</span></span>
  
## <a name="implementing-the-bits-interface"></a><span data-ttu-id="2afef-269">Implementieren der BITS-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2afef-269">Implementing the BITS interface</span></span>

<span data-ttu-id="2afef-270">Die [Background Intelligent Transfer Service](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) (BITS) ist ein Von Microsoft bereitgestellter Dienst zum Übertragen von Dateien zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="2afef-270">The [Background Intelligent Transfer Service](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) (BITS) is a service provided by Microsoft to transfer files between a client and server.</span></span> <span data-ttu-id="2afef-271">BITS ist einer der Kanäle, die Office Click-To-Run-Installationsprogramm zum Herunterladen von Inhalten verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="2afef-271">BITS is one of the channels that Office Click-To-Run installer can use to download content.</span></span> <span data-ttu-id="2afef-272">Standardmäßig verwendet das Microsoft 365 Apps-Klick-und-Ausführen-Installationsprogramm die integrierte Windows-Implementierung von BITS, um den Inhalt aus dem CDN.</span><span class="sxs-lookup"><span data-stu-id="2afef-272">By default, the Microsoft 365 Apps Click-To-Run installer uses the Windows' built in implementation of BITS to download the content from the CDN.</span></span> 
  
<span data-ttu-id="2afef-273">Durch die Bereitstellung einer angepassten BITS-Implementierung für die **Download()-Methode** der **IUpdateNotify-Schnittstelle** kann Ihre Verwaltbarkeitssoftware steuern, wo und wie der Client die Inhalte herunterlädt.</span><span class="sxs-lookup"><span data-stu-id="2afef-273">By providing a customized BITS implementation to the **download()** method of the **IUpdateNotify** interface, your manageability software can control where and how the client downloads the content.</span></span> <span data-ttu-id="2afef-274">Eine angepasste BITS-Schnittstelle ist hilfreich, wenn sie einen anderen benutzerdefinierten Inhaltsverteilungskanal als die integrierten Klick-und-Ausführen-Kanäle, z. B. die CDN-, IIS-Server- oder Dateifreigaben, zur Verfügung stellt.</span><span class="sxs-lookup"><span data-stu-id="2afef-274">A customized BITS interface is useful when providing a custom content distribution channel other than the Click-to-Run built-in channels, such as the CDN, IIS servers, or file shares.</span></span> 
  
<span data-ttu-id="2afef-275">Die Mindestanforderung für eine angepasste #A0 für die Office C2R-Dienst ist:</span><span class="sxs-lookup"><span data-stu-id="2afef-275">The minimum requirement for a customized BITS interface to work with Office C2R service is:</span></span>
  
- <span data-ttu-id="2afef-276">Für **IBackgroundCopyManager**:</span><span class="sxs-lookup"><span data-stu-id="2afef-276">For **IBackgroundCopyManager**:</span></span>
    
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

- <span data-ttu-id="2afef-277">Für **IBackgroundCopyJob**:</span><span class="sxs-lookup"><span data-stu-id="2afef-277">For **IBackgroundCopyJob**:</span></span>
    
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

- <span data-ttu-id="2afef-278">Für **IBackgroundCopyJob3**:</span><span class="sxs-lookup"><span data-stu-id="2afef-278">For **IBackgroundCopyJob3**:</span></span>
    
  ```cpp
  HRESULT _stdcall AddFileWithRanges(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName,
                      [in] DWORD RangeCount,
                      [in] BG_FILE_RANGE Ranges[])
  
  ```

- <span data-ttu-id="2afef-279">Für die  `Addfile`  `AddFileWithRanges` Und-Funktionen hat die Remote-URL das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="2afef-279">For the  `Addfile` and  `AddFileWithRanges` functions, the remote URL is in the following format:</span></span> 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - <span data-ttu-id="2afef-280">cmbits ist hart codiert und steht für angepasste BITS.</span><span class="sxs-lookup"><span data-stu-id="2afef-280">cmbits is hard coded, and stands for customized BITS.</span></span>
    
  -  <span data-ttu-id="2afef-281">_\<contentid\>_ ist der _contentid-Parameter_ für die **Download()-Methode.**</span><span class="sxs-lookup"><span data-stu-id="2afef-281">_\<contentid\>_ is the  _contentid_ parameter for the **Download()** method.</span></span> 
    
  -  <span data-ttu-id="2afef-282">_\<relative path to target file\>_ stellt den Speicherort und dateinamen der datei bereit, die heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2afef-282">_\<relative path to target file\>_ provides the location and file name of the file to download.</span></span> 
    
    <span data-ttu-id="2afef-283">Wenn Sie z. B. eine _contentid_ der Download()-Methode bereitgestellt haben und Office C2R die Versions-Cab-Datei herunterladen möchte, z. B. Datei, wird `f732af58-5d86-4299-abe9-7595c35136ef`  `v32.cab` **AddFile()** mit folgendem Aufruf `RemoteUrl` angezeigt:</span><span class="sxs-lookup"><span data-stu-id="2afef-283">For example, if you have provided a  _contentid_ of  `f732af58-5d86-4299-abe9-7595c35136ef` to the **Download()** method, and Office C2R wants to download the version cab file, such as  `v32.cab` file, it will call **AddFile()** with the following  `RemoteUrl`:</span></span>
    
  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- <span data-ttu-id="2afef-284">Für **IBackgroundCopyError**:</span><span class="sxs-lookup"><span data-stu-id="2afef-284">For **IBackgroundCopyError**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- <span data-ttu-id="2afef-285">Für **IBackgroundCopyFile**:</span><span class="sxs-lookup"><span data-stu-id="2afef-285">For **IBackgroundCopyFile**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetLocalName([out] LPWSTR *ppName); 
  HRESULT _stdcall GetRemoteName([out] LPWSTR *ppName);
  
  ```
## <a name="automating-content-staging"></a><span data-ttu-id="2afef-286">Automatisieren der Inhaltsbereitstellung</span><span class="sxs-lookup"><span data-stu-id="2afef-286">Automating content staging</span></span>

<span data-ttu-id="2afef-287">IT-Administratoren können festlegen, dass Desktopclients automatisch Updates empfangen können, wenn sie direkt über die CDN verfügbar sind, oder sie können die Bereitstellung von Updates steuern, die über die Updatekanäle mit dem Office Deployment Tool oder Microsoft Endpoint Configuration Manager verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="2afef-287">IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the CDN or they can choose to control the deployment of updates available from the update channels using the Office Deployment Tool or Microsoft Endpoint Configuration Manager.</span></span>
  
<span data-ttu-id="2afef-288">Der Dienst unterstützt die Möglichkeit für Verwaltungstools, den Download der Inhalte zu erkennen und zu automatisieren, wenn Updates verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="2afef-288">The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.</span></span>
  
<span data-ttu-id="2afef-289">**Die folgende Abbildung bietet eine Übersicht über das Herunterladen eines benutzerdefinierten Bilds**</span><span class="sxs-lookup"><span data-stu-id="2afef-289">**The following image is an overview of downloading a custom image**</span></span>

<span data-ttu-id="2afef-290">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Ein Diagramm der Verwendung der COM-Schnittstelle im Office -Klick-und-Ausführen-Installationsprogramm")</span><span class="sxs-lookup"><span data-stu-id="2afef-290">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on the Office Click-To-Run installer")</span></span>
  
### <a name="overview-of-downloading-a-custom-image"></a><span data-ttu-id="2afef-291">Übersicht über das Herunterladen eines benutzerdefinierten Bilds</span><span class="sxs-lookup"><span data-stu-id="2afef-291">Overview of downloading a custom image</span></span>
  
<span data-ttu-id="2afef-292">Im vorherigen Diagramm sehen Sie, dass ein Microsoft 365 Apps bild auf der CDN.</span><span class="sxs-lookup"><span data-stu-id="2afef-292">In the previous diagram, you see that a new Microsoft 365 Apps image is available on the CDN.</span></span> <span data-ttu-id="2afef-293">Zusammen mit dem Microsoft 365 Apps steht eine API zur Verfügung, die über die erforderlichen Informationen verfügt, um verwaltbarkeitssoftware zu ermöglichen, benutzerdefinierte Bilder direkt zu erstellen, die die Notwendigkeit der Verwendung des Office-Bereitstellungstools ersetzen.</span><span class="sxs-lookup"><span data-stu-id="2afef-293">Along with the Microsoft 365 Apps image, an API is available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.</span></span>

<span data-ttu-id="2afef-294">Ein Unternehmen konfiguriert seine WSUS so, dass die Microsoft 365 Apps werden.</span><span class="sxs-lookup"><span data-stu-id="2afef-294">An enterprise configures their WSUS to sync the Microsoft 365 Apps updates.</span></span> <span data-ttu-id="2afef-295">Diese Updates enthalten nicht die tatsächliche Bildnutzlast, lassen jedoch zu, dass die Verwaltbarkeitssoftware erkennt, wann neue Inhalte verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="2afef-295">These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available.</span></span> <span data-ttu-id="2afef-296">Die Verwaltbarkeitssoftware kann dann die Microsoft 365 Apps Updatemetadaten lesen, um zu verstehen, auf welche Version Office Update angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="2afef-296">The manageability software can then read the Microsoft 365 Apps Update metadata to understand what version of Office the update applies to.</span></span>

<span data-ttu-id="2afef-297">Wenn das Update anwendbar ist, kann die Verwaltbarkeitssoftware den CDN-Inhalt und die Dateiliste verwenden, um das benutzerdefinierte Image zu erstellen und es an dem Dateifreigabespeicherort zu speichern, für den es konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="2afef-297">If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.</span></span>
  
### <a name="using-the-microsoft-365-apps-file-list-api"></a><span data-ttu-id="2afef-298">Verwenden der Microsoft 365 Apps-Dateilisten-API</span><span class="sxs-lookup"><span data-stu-id="2afef-298">Using the Microsoft 365 Apps file list API</span></span>

<span data-ttu-id="2afef-299">Die Microsoft 365 Apps-Dateilisten-API wird verwendet, um die Namen der Dateien abzurufen, die für ein bestimmtes Update Microsoft 365 Apps werden.</span><span class="sxs-lookup"><span data-stu-id="2afef-299">The Microsoft 365 Apps file list API is used to retrieve the names of the files needed for a particular Microsoft 365 Apps update.</span></span>

<span data-ttu-id="2afef-300">HTTP-Anforderung</span><span class="sxs-lookup"><span data-stu-id="2afef-300">HTTP Request</span></span>

<span data-ttu-id="2afef-301">GET https://config.office.com/api/filelist</span><span class="sxs-lookup"><span data-stu-id="2afef-301">GET https://config.office.com/api/filelist</span></span>

<span data-ttu-id="2afef-302">Geben Sie für diese Methode keinen Anforderungstext an.</span><span class="sxs-lookup"><span data-stu-id="2afef-302">Do not supply a request body for this method.</span></span>

<span data-ttu-id="2afef-303">Zum Aufrufen dieser API sind keine Berechtigungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2afef-303">No permissions are required to call this API.</span></span>

<span data-ttu-id="2afef-304">Optionale Abfrageparameter</span><span class="sxs-lookup"><span data-stu-id="2afef-304">Optional query parameters</span></span>

|<span data-ttu-id="2afef-305">**Name**</span><span class="sxs-lookup"><span data-stu-id="2afef-305">**Name**</span></span>|<span data-ttu-id="2afef-306">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2afef-306">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2afef-307">channel</span><span class="sxs-lookup"><span data-stu-id="2afef-307">channel</span></span> <br/>| <span data-ttu-id="2afef-308">Gibt den Kanalnamen an</span><span class="sxs-lookup"><span data-stu-id="2afef-308">Specifies the channel name</span></span>  <br/> <span data-ttu-id="2afef-309">Optional – Standardeinstellung "SemiAnnual"</span><span class="sxs-lookup"><span data-stu-id="2afef-309">Optional – default to ‘SemiAnnual’</span></span> <br/> <span data-ttu-id="2afef-310">Unterstützte Werte https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element</span><span class="sxs-lookup"><span data-stu-id="2afef-310">Supported values https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element</span></span> |
| <span data-ttu-id="2afef-311">Version</span><span class="sxs-lookup"><span data-stu-id="2afef-311">version</span></span> <br/>| <span data-ttu-id="2afef-312">Gibt die Updateversion an</span><span class="sxs-lookup"><span data-stu-id="2afef-312">Specifies the update version</span></span> <br/> <span data-ttu-id="2afef-313">Optional – standardmäßig die neueste Version, die für den angegebenen Kanal verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="2afef-313">Optional – defaults to the latest version available for the specified channel</span></span> |
| <span data-ttu-id="2afef-314">arch</span><span class="sxs-lookup"><span data-stu-id="2afef-314">arch</span></span> <br/>| <span data-ttu-id="2afef-315">Gibt die Clientarchitektur an</span><span class="sxs-lookup"><span data-stu-id="2afef-315">Specifies client architecture</span></span> <br/> <span data-ttu-id="2afef-316">Optional – standardmäßig "x64"</span><span class="sxs-lookup"><span data-stu-id="2afef-316">Optional – defaults to ‘x64’</span></span> <br/> <span data-ttu-id="2afef-317">Unterstützte Werte: x64, x86</span><span class="sxs-lookup"><span data-stu-id="2afef-317">Supported values: x64, x86</span></span> |
| <span data-ttu-id="2afef-318">lid</span><span class="sxs-lookup"><span data-stu-id="2afef-318">lid</span></span> <br/>| <span data-ttu-id="2afef-319">Gibt die zu verwendenden Sprachdateien an.</span><span class="sxs-lookup"><span data-stu-id="2afef-319">Specifies the language files to include</span></span> <br/> <span data-ttu-id="2afef-320">Optional – Standardmäßig keine</span><span class="sxs-lookup"><span data-stu-id="2afef-320">Optional – defaults to none</span></span> <br/> <span data-ttu-id="2afef-321">Um mehrere Sprachen anzugeben, fügen Sie einen Deckelabfrageparameter für jede Sprache ein.</span><span class="sxs-lookup"><span data-stu-id="2afef-321">To specify multiple languages, include an lid query parameter for each language</span></span> <br/> <span data-ttu-id="2afef-322">Verwenden Sie das Sprachbezeichnerformat ex.</span><span class="sxs-lookup"><span data-stu-id="2afef-322">Use the language identifier format, ex.</span></span> <span data-ttu-id="2afef-323">"en-us", "fr-fr"</span><span class="sxs-lookup"><span data-stu-id="2afef-323">‘en-us’, ‘fr-fr’</span></span> |
| <span data-ttu-id="2afef-324">alllanguages</span><span class="sxs-lookup"><span data-stu-id="2afef-324">alllanguages</span></span> <br/>| <span data-ttu-id="2afef-325">Gibt an, dass alle Sprachdateien enthalten sind</span><span class="sxs-lookup"><span data-stu-id="2afef-325">Specifies to include all language files</span></span> <br/> <span data-ttu-id="2afef-326">Optional – Standardmäßig false</span><span class="sxs-lookup"><span data-stu-id="2afef-326">Optional – defaults to false</span></span> |

<span data-ttu-id="2afef-327">HTTP-Antwort</span><span class="sxs-lookup"><span data-stu-id="2afef-327">HTTP Response</span></span>

<span data-ttu-id="2afef-328">Wenn die Methode erfolgreich ist, werden der Antwortcode 200 OK und eine Auflistung von Dateiobjekten im Antworttext zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2afef-328">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>

<span data-ttu-id="2afef-329">Führen Sie die folgenden Schritte aus, um ein Bild zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="2afef-329">To create an image, follow these steps:</span></span>
1.  <span data-ttu-id="2afef-330">Rufen Sie die API auf, und geben Sie die entsprechenden Abfrageparameter für den Kanal, die Version und die Architektur des Updates an, an dem Sie interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="2afef-330">Call the API, providing the appropriate query parameters for the channel, version and architecture of the update you are interested in.</span></span>
<span data-ttu-id="2afef-331">Hinweis: File-Objekte mit dem Attribut "lcid": "0" sind sprachneutrale Dateien und müssen in das Bild eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="2afef-331">Note: File objects with the attribute "lcid": "0" are language neutral files and must be included in the image.</span></span>
2.  <span data-ttu-id="2afef-332">Erstellen Sie ein lokales Bild des CDN, indem Sie die Dateiobjekte durch iterieren und die CDN-Dateien kopieren und gleichzeitig die Ordnerstruktur erstellen, wie durch das relativePath-Attribut angegeben, das für jedes der Dateiobjekte definiert ist.</span><span class="sxs-lookup"><span data-stu-id="2afef-332">Construct a local image of the CDN by iterating through the file objects and copying the CDN files, while creating the folder structure as specified by the “relativePath” attribute defined for each of the file objects.</span></span>

<span data-ttu-id="2afef-333">Im folgenden Beispiel wird die Dateiliste für den aktuellen Kanal und version 16.0.4229.1004 für 64bit abgerufen und enthält die Dateien in französischer und englischer Sprache:</span><span class="sxs-lookup"><span data-stu-id="2afef-333">The following example retrieves the file list for the Current Channel and version 16.0.4229.1004 for 64bit and includes the French and English language files:</span></span>

```http
Get https://config.office.com/api/filelist?Channel=Current&Version=16.0.4229.1004&Arch=x64&Lid=fr-fr&Lid=en-US
```

### <a name="hash-verification-of-dat-files"></a><span data-ttu-id="2afef-334">Hashüberprüfung von #A0</span><span class="sxs-lookup"><span data-stu-id="2afef-334">Hash verification of .dat files</span></span>

<span data-ttu-id="2afef-335">Bilderstellungstools können die Integrität der heruntergeladenen .dat-Dateien überprüfen, indem ein berechneter Hashwert mit dem angegebenen Hashwert verglichen wird, der jeder #A0 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2afef-335">Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed hash value with the supplied hash value associated with each of the .dat files.</span></span> <span data-ttu-id="2afef-336">Es folgt ein Beispiel für ein Dateiobjekt, das hashLocation- und hashAlgorithm-Werte angibt:</span><span class="sxs-lookup"><span data-stu-id="2afef-336">Following is an example of a file object that specifies hashLocation and hashAlgorithm values:</span></span>
  
```xml
{
  "url": "https://officecdn.microsoft.com/pr/7ffbc6bf-bc32-4f92-8982-f9dd17fd3114/office/data/16.0.1234.1001/stream.x64.x-none.dat",
  "name": "stream.x64.x-none.dat",
  "relativePath": "/office/data/16.0.1234.1001/",
  "hashLocation": "s640.cab/stream.x64.x-none.hash",
  "hashAlgorithm": "Sha256",
  "lcid": "0"
},
```

- <span data-ttu-id="2afef-337">Das **hashLocation-Attribut** gibt den relativen Pfadspeicherort der .cab an, die den Hashwert enthält.</span><span class="sxs-lookup"><span data-stu-id="2afef-337">The **hashLocation** attribute specifies the relative path location of .cab file that contains the hash value.</span></span> <span data-ttu-id="2afef-338">Erstellen Sie den Speicherort der Hashdatei, indem Sie URL + relativePath + hashLocation verketten.</span><span class="sxs-lookup"><span data-stu-id="2afef-338">Construct the hash file location by concatenating URL + relativePath + hashLocation.</span></span> <span data-ttu-id="2afef-339">Im folgenden Beispiel würde der speicherort stream.x64.bg-bg.hash sein:</span><span class="sxs-lookup"><span data-stu-id="2afef-339">In the following example, the stream.x64.bg-bg.hash location would be:</span></span> 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- <span data-ttu-id="2afef-340">Das **hashAlgorithm-Attribut** gibt an, welcher Hashalgorithmus verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="2afef-340">The **hashAlgorithm** attribute specifies what hashing algorithm was used.</span></span> 
    
  <span data-ttu-id="2afef-341">Um die Integrität der datei stream.x64.bg-bg.dat zu überprüfen, öffnen Sie den stream.x64.bg-bg.hash, und lesen Sie den HASH-Wert, der die erste Textzeile in der Hashdatei ist.</span><span class="sxs-lookup"><span data-stu-id="2afef-341">To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the HASH value which is the first line of text in the hash file.</span></span> <span data-ttu-id="2afef-342">Vergleichen Sie dies mit dem berechneten Hashwert (mithilfe des angegebenen Hashalgorithmus), um die Integrität der heruntergeladenen #A0 zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="2afef-342">Compare this to the computed hash value (using the specified hashing algorithm) to verify the integrity of the downloaded .dat file.</span></span>
    
  <span data-ttu-id="2afef-343">Im folgenden Beispiel wird C# Code zum Lesen des Hashs gezeigt.</span><span class="sxs-lookup"><span data-stu-id="2afef-343">The following example shows the C# code to read the hash.</span></span>
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="microsoft-365-apps-updates"></a><span data-ttu-id="2afef-344">Microsoft 365 Apps Updates</span><span class="sxs-lookup"><span data-stu-id="2afef-344">Microsoft 365 Apps Updates</span></span>

<span data-ttu-id="2afef-345">Alle Microsoft 365 Apps werden im Microsoft [Update Catalog veröffentlicht.](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client)</span><span class="sxs-lookup"><span data-stu-id="2afef-345">All Microsoft 365 Apps Updates are published to the [Microsoft Update Catalog](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span></span>
  
<span data-ttu-id="2afef-346">Microsoft 365 Apps Updates ermöglichen es der Verwaltbarkeitssoftware, Microsoft 365 Apps Updates auf eine Weise zu behandeln, die jedem anderen #A0 mit einer Ausnahme sehr ähnlich ist. Die Clientupdates enthalten keine tatsächliche Nutzlast.</span><span class="sxs-lookup"><span data-stu-id="2afef-346">Microsoft 365 Apps Updates enable manageability software to treat Microsoft 365 Apps Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload.</span></span> <span data-ttu-id="2afef-347">Die Microsoft 365 Apps Updates sollten nicht auf Clients installiert werden, sondern zum Auslösen der Workflows verwendet werden, indem die Verwaltbarkeitssoftware den Installationsbefehl durch den oben gezeigten COM-basierten Installationsmechanismus ersetzt.</span><span class="sxs-lookup"><span data-stu-id="2afef-347">The Microsoft 365 Apps Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.</span></span>

<span data-ttu-id="2afef-348">**Die folgende Abbildung zeigt ein Diagramm des Office 365 Clientupdateworkflows.**</span><span class="sxs-lookup"><span data-stu-id="2afef-348">**The following figure shows a diagram of the Office 365 Client Update workflow.**</span></span>

<span data-ttu-id="2afef-349">![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflowdiagramm für O365PP-Clientupdates")</span><span class="sxs-lookup"><span data-stu-id="2afef-349">![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")</span></span>
  
<span data-ttu-id="2afef-350">Jedes Microsoft 365 Apps update, das veröffentlicht wird, enthält Metadaten zum Update.</span><span class="sxs-lookup"><span data-stu-id="2afef-350">Each Microsoft 365 Apps Update that is published includes metadata about the update.</span></span> <span data-ttu-id="2afef-351">Diese Metadaten enthalten den Parameter MoreInfoUrl, der zum Ableitung des API-Aufrufs an die Dateilisten-API für dieses spezifische Update verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2afef-351">This metadata includes a parameter called MoreInfoUrl which can be used to derive the API call to the file list API for that specific update.</span></span>

<span data-ttu-id="2afef-352">Im folgenden Beispiel wird die Dateilisten-API in die MoreInfoURL eingebettet und beginnt mit "ServicePath="</span><span class="sxs-lookup"><span data-stu-id="2afef-352">In the following example, the file list API is embedded in the MoreInfoURL and starts with “ServicePath=”</span></span>

<span data-ttu-id="2afef-353"> http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath=https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True</span><span class="sxs-lookup"><span data-stu-id="2afef-353">http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath=https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True</span></span>
  
### <a name="additional-metadata-for-automating-content-staging"></a><span data-ttu-id="2afef-354">Zusätzliche Metadaten für die Automatisierung der Inhaltsbereitstellung</span><span class="sxs-lookup"><span data-stu-id="2afef-354">Additional metadata for automating content staging</span></span>

<span data-ttu-id="2afef-355">**Veröffentlichungsverlaufs-API**</span><span class="sxs-lookup"><span data-stu-id="2afef-355">**Release History API**</span></span>
  
<span data-ttu-id="2afef-356">Die Microsoft 365 Apps Versionsverlaufs-API wird verwendet, um Details für jedes auf dem CDN veröffentlichte Update zusammen mit den Kanalnamen und anderen Kanalattributen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2afef-356">The Microsoft 365 Apps release history API is used to retrieve details for each of the updates published to the CDN along with the channel names and other channel attributes.</span></span>

<span data-ttu-id="2afef-357">HTTP-Anforderung</span><span class="sxs-lookup"><span data-stu-id="2afef-357">HTTP Request</span></span>

```http
GET https://config.office.com/api/filelist/channels 
```

<span data-ttu-id="2afef-358">Geben Sie für diese Methode keinen Anforderungstext an.</span><span class="sxs-lookup"><span data-stu-id="2afef-358">Do not supply a request body for this method.</span></span>

<span data-ttu-id="2afef-359">Zum Aufrufen dieser API sind keine Berechtigungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2afef-359">No permissions are required to call this API.</span></span>

<span data-ttu-id="2afef-360">HTTP-Antwort</span><span class="sxs-lookup"><span data-stu-id="2afef-360">HTTP Response</span></span>

<span data-ttu-id="2afef-361">Wenn die Methode erfolgreich ist, werden der Antwortcode 200 OK und eine Auflistung von Dateiobjekten im Antworttext zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2afef-361">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>

<span data-ttu-id="2afef-362">**SKUs-API**</span><span class="sxs-lookup"><span data-stu-id="2afef-362">**SKUs API**</span></span>
  
<span data-ttu-id="2afef-363">Die SKUs-API gibt Informationen zurück, die nützlich sind, um zu bestimmen, welche Produkte für die Bereitstellung und Wartung Office CDN verschiedenen Optionen für die einzelnen Produkte verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="2afef-363">The SKUs API returns information that is useful for determining which products are available for deployment and servicing from the Office CDN along with various options for each.</span></span>

<span data-ttu-id="2afef-364">HTTP-Anforderung</span><span class="sxs-lookup"><span data-stu-id="2afef-364">HTTP Request</span></span>

```http
GET https://config.office.com/api/filelist/skus 
```

<span data-ttu-id="2afef-365">Geben Sie für diese Methode keinen Anforderungstext an.</span><span class="sxs-lookup"><span data-stu-id="2afef-365">Do not supply a request body for this method.</span></span>

<span data-ttu-id="2afef-366">Zum Aufrufen dieser API sind keine Berechtigungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2afef-366">No permissions are required to call this API.</span></span>

<span data-ttu-id="2afef-367">HTTP-Antwort</span><span class="sxs-lookup"><span data-stu-id="2afef-367">HTTP Response</span></span>

<span data-ttu-id="2afef-368">Wenn die Methode erfolgreich ist, werden der Antwortcode 200 OK und eine Auflistung von Dateiobjekten im Antworttext zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2afef-368">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>
