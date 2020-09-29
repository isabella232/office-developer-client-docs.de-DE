---
title: Integrieren von Verwaltbarkeit-Anwendungen mit dem Click-to-Run-Installationsprogramm von Microsoft 365 apps
manager: lindalu
ms.date: 09/28/2020
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: In diesem Artikel erfahren Sie, wie Sie das Click-to-Run-Installationsprogramm von Microsoft 365 apps mit einer Software Verwaltungslösung integrieren.
ms.openlocfilehash: eccd634f7906acf25b521ed2deb456ca914f37da
ms.sourcegitcommit: c8c51bd3f51c0a59fe44c014c8e56f1ba7c7aa03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "48297314"
---
# <a name="integrating-manageability-applications-with-microsoft-365-apps-click-to-run-installer"></a><span data-ttu-id="a73b4-103">Integrieren von Verwaltbarkeit-Anwendungen mit dem Click-to-Run-Installationsprogramm von Microsoft 365 apps</span><span class="sxs-lookup"><span data-stu-id="a73b4-103">Integrating manageability applications with Microsoft 365 Apps Click-to-Run installer</span></span>

<span data-ttu-id="a73b4-104">In diesem Artikel erfahren Sie, wie Sie das Click-to-Run-Installationsprogramm von Microsoft 365 apps mit einer Software Verwaltungslösung integrieren.</span><span class="sxs-lookup"><span data-stu-id="a73b4-104">Learn how to integrate the Microsoft 365 Apps Click-to-Run installer with a software management solution.</span></span>
  
<span data-ttu-id="a73b4-105">Das Klick-und-Los-Installationsprogramm von Microsoft 365 apps stellt eine COM-Schnittstelle bereit, die IT-Experten und Software Verwaltungslösungen die programmgesteuerte Steuerung der Updateverwaltung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="a73b4-105">The Microsoft 365 Apps Click-to-Run installer provides a COM interface that allows IT Professionals and software management solutions programmatic control over update management.</span></span> <span data-ttu-id="a73b4-106">Diese Schnittstelle stellt zusätzliche Verwaltungsfunktionen bereit, die über das Office-Bereitstellungs Tool hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="a73b4-106">This interface provides additional management capabilities beyond what is provided by the Office Deployment Tool.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a73b4-107">Dieser Artikel bezieht sich auf Office-Apps, die das Klick-und-Los-Installationsprogramm verwenden.</span><span class="sxs-lookup"><span data-stu-id="a73b4-107">This article applies to Office apps that use the Click-to-Run installer.</span></span> 
  
## <a name="integrating-with-the-click-to-run"></a><span data-ttu-id="a73b4-108">Integrieren in das Klick-und-Los</span><span class="sxs-lookup"><span data-stu-id="a73b4-108">Integrating with the Click-to-Run</span></span>

<span data-ttu-id="a73b4-109">Um diese Schnittstelle zu verwenden, ruft eine verwaltbare Anwendung die COM-Schnittstelle auf und ruft freigegebene APIs auf, die direkt mit dem Klick-und-Los-Installationsdienst kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="a73b4-109">To use this interface, a manageability application invokes the COM interface and calls exposed APIs that communicate directly with the Click-to-Run installation service.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a73b4-110">Das Office-Klick-und-Los-Installationsprogramm kann über die Befehlszeile mit Parametern ausgeführt werden, die das Verhalten steuern können, wie im [Office-Bereitstellungs Tool für Klick-und-Los](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool)dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="a73b4-110">The Office Click-to-Run installer can be run from the command-line with parameters that can control the behavior, as documented in [Office Deployment Tool for Click-to-Run](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool).</span></span> 
  
<span data-ttu-id="a73b4-111">**Es folgt ein konzeptionelles Diagramm der COM-Schnittstelle.**</span><span class="sxs-lookup"><span data-stu-id="a73b4-111">**Following is a conceptual diagram of the COM interface**</span></span>

<span data-ttu-id="a73b4-112">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Ein Diagramm zur Verwendung der COM-Schnittstelle im Office-Klick-und-Los-Installationsprogramm")</span><span class="sxs-lookup"><span data-stu-id="a73b4-112">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on  the Office Click-To-Run installer")</span></span>
  
<span data-ttu-id="a73b4-113">Das Klick-und-Los-Installationsprogramm von Microsoft 365 apps implementiert eine COM-basierte Schnittstelle, die **IUpdateNotify** für CLSID **CLSID_UpdateNotifyObject**registriert ist.</span><span class="sxs-lookup"><span data-stu-id="a73b4-113">The Microsoft 365 Apps Click-to-Run installer implements a COM-based interface, **IUpdateNotify** registered to CLSID **CLSID_UpdateNotifyObject**.</span></span>
  
<span data-ttu-id="a73b4-114">Diese Schnittstelle kann wie folgt aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="a73b4-114">This interface can be invoked as follows:</span></span>
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

<span data-ttu-id="a73b4-115">Der Anruf ist nur erfolgreich, wenn der Anrufer unter erhöhten Rechten ausgeführt wird, da das Installationsprogramm für die Klick-und-Los-Installation mit erhöhten Rechten ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="a73b4-115">The call will only succeed if the caller is running under elevated privileges, as the Click-to-Run installation program must be run with elevated privileges.</span></span>
  
<span data-ttu-id="a73b4-116">Die **IUpdateNotify** -com-Schnittstelle stellt drei asynchrone Funktionen zur Verfügung, die für die Überprüfung der Befehle und Parameter und die Planung der Ausführung mit dem Klick-und-Los-Installationsdienst verantwortlich sind.</span><span class="sxs-lookup"><span data-stu-id="a73b4-116">The **IUpdateNotify** COM interface exposes three asynchronous functions responsible for validating the commands and parameters and scheduling execution with the Click-to-Run installation service.</span></span> 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

<span data-ttu-id="a73b4-117">Eine Forth-Methode, **Status**, kann verwendet werden, um Informationen über den Status des zuletzt ausgeführten Befehls oder den Status des derzeit ausgeführten Befehls abzurufen (also Erfolg, Fehler, detaillierte Fehlercodes).</span><span class="sxs-lookup"><span data-stu-id="a73b4-117">A forth method, **Status**, can be used to get information about the status of the last executed command or the status of the currently executing command (i.e. success, failure, detailed error codes).</span></span>
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

<span data-ttu-id="a73b4-118">Es gibt vier Zustände, in denen der Klick-und-Los-Installationsdienst während seines Lebenszyklus möglicherweise vorliegt, während dessen **IUpdateNotify** -Methoden aufgerufen werden können. Neustarten, Leerlauf, herunterladen und anwenden.</span><span class="sxs-lookup"><span data-stu-id="a73b4-118">There are four states that the Click-to-Run installation service may be in during its lifecycle, during which **IUpdateNotify** methods may be called; Rebooting, Idle, Downloading and Applying.</span></span> 
  
<span data-ttu-id="a73b4-119">**Im folgenden finden Sie das Diagramm "Statuscomputer" der COM-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a73b4-119">**Following is the COM Interface State Machine diagram**</span></span>

<span data-ttu-id="a73b4-120">![A state diagram for the COM interface.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Ein Statusdiagramm für die COM-Schnittstelle")</span><span class="sxs-lookup"><span data-stu-id="a73b4-120">![A state diagram for the COM interface.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "A state diagram for the COM interface")</span></span>
  
> [!NOTE]
> <span data-ttu-id="a73b4-121">**Neustart: beim**Booten des Computers gibt es einen Zeitraum, in dem der Klick-und-Los-Installationsdienst nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a73b4-121">**Rebooting**: When the machine is booting there is a period of time when the Click-to-Run installer service is not available.</span></span> <span data-ttu-id="a73b4-122">Ein erfolgreicher Aufruf der Status-Methode nach einem Neustart wird eUPDATE_UNKNOWN zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a73b4-122">A successful call to the Status method after a reboot will return eUPDATE_UNKNOWN.</span></span> 
  
<span data-ttu-id="a73b4-123">**Leerlauf:** Wenn sich das Klick-und-Los-Installationsprogramm im Leerlauf befindet, können Sie Folgendes aufrufen:</span><span class="sxs-lookup"><span data-stu-id="a73b4-123">**Idle:** When the Click-to-Run installer is in the idle state, you can call:</span></span> 
  
- <span data-ttu-id="a73b4-124">**Apply**: Installieren Sie zuvor heruntergeladenen Inhalt.</span><span class="sxs-lookup"><span data-stu-id="a73b4-124">**Apply**: Install previously downloaded content.</span></span>
    
- <span data-ttu-id="a73b4-125">**Cancel**: Gibt zurück  `0x800000e` , "eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen."</span><span class="sxs-lookup"><span data-stu-id="a73b4-125">**Cancel**: Returns  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="a73b4-126">**Download**: lädt neue Inhalte zur späteren Installation auf den Client herunter.</span><span class="sxs-lookup"><span data-stu-id="a73b4-126">**Download**: Downloads new content to the client for later installation.</span></span>
    
- <span data-ttu-id="a73b4-127">**Status**: gibt das Ergebnis der letzten abgeschlossenen Aktion oder eine Fehlermeldung zurück, wenn die Aktion mit einem Fehler beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="a73b4-127">**Status**: Returns the result of the last completed action, or an error message if the action ended in failure.</span></span> <span data-ttu-id="a73b4-128">Wenn keine vorherige Aktion vorliegt, wird der **Status** zurückgegeben  `eUPDATE_UNKNOWN` .</span><span class="sxs-lookup"><span data-stu-id="a73b4-128">If there is no previous action, **Status** returns  `eUPDATE_UNKNOWN`.</span></span>
    
<span data-ttu-id="a73b4-129">**Herunterladen:** Wenn sich das Klick-und-Los-Installationsprogramm im Download Zustand befindet, können Sie Folgendes aufrufen:</span><span class="sxs-lookup"><span data-stu-id="a73b4-129">**Downloading:** When the Click-to-Run installer is in the downloading state, you can call:</span></span> 
  
- <span data-ttu-id="a73b4-130">**Apply**: gibt ein **HRESULT** mit dem Wert  `0x800000e` "eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen." zurück.</span><span class="sxs-lookup"><span data-stu-id="a73b4-130">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="a73b4-131">**Abbrechen**: beendet den Download und entfernt die teilweise heruntergeladenen Inhalte.</span><span class="sxs-lookup"><span data-stu-id="a73b4-131">**Cancel**: Stops the download and removes the partially downloaded content.</span></span>
    
- <span data-ttu-id="a73b4-132">**Download**: gibt ein **HRESULT** mit dem Wert  `0x800000e` "eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen." zurück.</span><span class="sxs-lookup"><span data-stu-id="a73b4-132">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="a73b4-133">**Status**: gibt **DOWNLOAD_WIP** zurück, um anzugeben, dass die Download Arbeit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a73b4-133">**Status**: Returns **DOWNLOAD_WIP** to indicate that download work is in progress.</span></span> 
    
<span data-ttu-id="a73b4-134">**Anwendung:** Wenn das Klick-und-Los-Installationsprogramm den Download Inhalt bereits installiert hat:</span><span class="sxs-lookup"><span data-stu-id="a73b4-134">**Applying:** When the Click-to-Run installer is in the process of installing previously download content:</span></span> 
  
- <span data-ttu-id="a73b4-135">**Apply**: gibt ein **HRESULT** mit dem Wert  `0x800000e` "eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen." zurück.</span><span class="sxs-lookup"><span data-stu-id="a73b4-135">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="a73b4-136">**Cancel**: Gibt zurück  `0x800000e` , die Apply-Aktion kann nicht abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="a73b4-136">**Cancel**: Returns  `0x800000e`, the Apply action cannot be canceled.</span></span>
    
- <span data-ttu-id="a73b4-137">**Download**: gibt ein **HRESULT** mit dem Wert  `0x800000e` "eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen." zurück.</span><span class="sxs-lookup"><span data-stu-id="a73b4-137">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="a73b4-138">**Status**: gibt **APPLY_WIP** zurück, um anzugeben, dass die Anwendung "Arbeit" ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a73b4-138">**Status**: Returns **APPLY_WIP** to indicate that apply work is in progress.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="a73b4-139">Da OfficeC2RCOM ein com+-Dienst ist und dynamisch geladen wird, müssen Sie **CoCreateInstance** jedes Mal aufrufen, wenn Sie eine Methode für diese Klasse aufrufen, um sicherzustellen, dass Sie das erwartete Ergebnis erhalten.</span><span class="sxs-lookup"><span data-stu-id="a73b4-139">Since OfficeC2RCOM is a COM+ service and is dynamically loaded, you need to call **CoCreateInstance** every time you call a method on this class to ensure that you get the expected result.</span></span> <span data-ttu-id="a73b4-140">Der com+-Dienst behandelt das Erstellen einer neuen Instanz, wenn dies erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a73b4-140">The COM+ service will handle creating a new instance if necessary.</span></span> <span data-ttu-id="a73b4-141">Wenn eine der Methoden zum ersten Mal aufgerufen wird, lädt com+ das **IUpdateNotify** -Objekt, und es wird in einer der dllhost.exe-Instanzen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a73b4-141">When one of the methods is called for the first time, COM+ will load the **IUpdateNotify** object and run it within one of the dllhost.exe instances.</span></span> <span data-ttu-id="a73b4-142">Das neue Objekt bleibt im Leerlauf etwa 3 Minuten aktiv.</span><span class="sxs-lookup"><span data-stu-id="a73b4-142">The new object will stay active for about 3 minutes in idle.</span></span> <span data-ttu-id="a73b4-143">Wenn ein anschließender Aufruf innerhalb von drei Minuten nach dem letzten Aufruf erfolgt, bleibt das **IUpdateNotify** -Objekt geladen, und es wird keine neue Instanz erstellt.</span><span class="sxs-lookup"><span data-stu-id="a73b4-143">If a subsequent call is made within three minutes of the last call, the **IUpdateNotify** object will remain loaded and a new instance is not created.</span></span> <span data-ttu-id="a73b4-144">Wenn innerhalb von drei Minuten kein Aufruf erfolgt, wird das IUpdateNotify-Objekt entladen, und ein neues **IUpdateNotify** -Objekt wird erstellt, wenn der nächste Aufruf erfolgt.</span><span class="sxs-lookup"><span data-stu-id="a73b4-144">If no call is made within three minutes, the IUpdateNotify object will be unloaded and a new **IUpdateNotify** object will be created when the next call is made.</span></span> 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a><span data-ttu-id="a73b4-145">Leitfaden zur com-API-Referenz für Klick-und-Los-Installer</span><span class="sxs-lookup"><span data-stu-id="a73b4-145">Click-to-Run installer COM API reference guide</span></span>

<span data-ttu-id="a73b4-146">In der folgenden API-Referenzdokumentation:</span><span class="sxs-lookup"><span data-stu-id="a73b4-146">In the following API reference documentation:</span></span>
  
- <span data-ttu-id="a73b4-147">Parameter befinden sich in einem Schlüssel-Wert-Paar Format, das durch ein Leerzeichengetrennt ist.</span><span class="sxs-lookup"><span data-stu-id="a73b4-147">Parameters are in a key/value pair format separated by a space.</span></span>
    
- <span data-ttu-id="a73b4-148">Bei den Parametern wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="a73b4-148">The parameters are not case-sensitive.</span></span>
    
- <span data-ttu-id="a73b4-149">Es gibt eine [Liste von Parametern](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) mit verfügbarer Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="a73b4-149">There is a [list of parameters](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) with documentation available.</span></span> 
    
- <span data-ttu-id="a73b4-150">Zusammenfassung der IUpdateNotify2-Schnittstelle ist jetzt enthalten.</span><span class="sxs-lookup"><span data-stu-id="a73b4-150">Summary of IUpdateNotify2 interface is now included.</span></span>
    
### <a name="apply"></a><span data-ttu-id="a73b4-151">Anwenden</span><span class="sxs-lookup"><span data-stu-id="a73b4-151">Apply</span></span>

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a><span data-ttu-id="a73b4-152">Parameter</span><span class="sxs-lookup"><span data-stu-id="a73b4-152">Parameters</span></span>

-  <span data-ttu-id="a73b4-153">_Display Level_: **true** , um den Installationsstatus, einschließlich Fehlern, während des Updateprozesses anzuzeigen; **false** , um den Installationsstatus, einschließlich Fehlern, während des Aktualisierungsvorgangs auszublenden.</span><span class="sxs-lookup"><span data-stu-id="a73b4-153">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="a73b4-154">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="a73b4-154">The default is **false**.</span></span>
    
-  <span data-ttu-id="a73b4-155">_forceappshutdown_: **true** , um zu erzwingen, dass Office-Anwendungen sofort heruntergefahren werden, wenn die **Apply** -Aktion ausgelöst wird; **false** , wenn ein Fehler auftritt, wenn Office-Anwendungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a73b4-155">_forceappshutdown_: **true** to force Office applications to shut down immediately when the **Apply** action is triggered; **false** to fail if any Office applications are running.</span></span> <span data-ttu-id="a73b4-156">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="a73b4-156">The default is **false**.</span></span> <span data-ttu-id="a73b4-157">Weitere Informationen finden Sie unter [Hinweise](#bk_ApplyRemark) .</span><span class="sxs-lookup"><span data-stu-id="a73b4-157">See [Remarks](#bk_ApplyRemark) for more information.</span></span> 
    
  <span data-ttu-id="a73b4-158">Wenn eine Office-Anwendung ausgeführt wird, wenn die **Apply** -Aktion ausgelöst wird, tritt in der Regel die **Apply** -Aktion nicht mehr auf.</span><span class="sxs-lookup"><span data-stu-id="a73b4-158">If any Office application is running when the **Apply** action is triggered, the **Apply** action will usually fail.</span></span> <span data-ttu-id="a73b4-159">Die Übergabe  `forceappshutdown=true` an die **Apply** -Methode führt dazu, dass der **OfficeClickToRun** -Dienst die Anwendungen sofort herunterfährt und das Update anwendet.</span><span class="sxs-lookup"><span data-stu-id="a73b4-159">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down the applications and apply the update.</span></span> <span data-ttu-id="a73b4-160">Der Benutzer kann in diesem Fall Datenverlust auftreten.</span><span class="sxs-lookup"><span data-stu-id="a73b4-160">The user may experience data loss in this case.</span></span> 
    
#### <a name="return-results"></a><span data-ttu-id="a73b4-161">Ergebnisse zurückgeben</span><span class="sxs-lookup"><span data-stu-id="a73b4-161">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a73b4-162">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="a73b4-162">**S_OK**</span></span> <br/> |<span data-ttu-id="a73b4-163">Aktion wurde erfolgreich an den Klick-und-Los-Dienst zur Ausführung übermittelt.</span><span class="sxs-lookup"><span data-stu-id="a73b4-163">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="a73b4-164">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="a73b4-164">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="a73b4-165">Der Aufrufer wird nicht mit erhöhten Rechten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a73b4-165">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="a73b4-166">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="a73b4-166">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="a73b4-167">Ungültige Parameter wurden übergeben.</span><span class="sxs-lookup"><span data-stu-id="a73b4-167">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="a73b4-168">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="a73b4-168">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="a73b4-169">Die Aktion ist zu diesem Zeitpunkt nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="a73b4-169">Action is not allowed at this time.</span></span> <span data-ttu-id="a73b4-170">Weitere Informationen finden Sie unter [Hinweise](#bk_ApplyRemark) .</span><span class="sxs-lookup"><span data-stu-id="a73b4-170">See [Remarks](#bk_ApplyRemark) for more information.</span></span>  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="a73b4-171">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a73b4-171">Remarks</span></span>

- <span data-ttu-id="a73b4-172">Wenn eine Office-Anwendung ausgeführt wird, wenn die **Apply** -Aktion ausgelöst wird, tritt bei der **Apply** -Aktion ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="a73b4-172">If any Office application is running when the **Apply** action is triggered, the **Apply** action will fail.</span></span> <span data-ttu-id="a73b4-173">Die Übergabe  `forceappshutdown=true` an die **Apply** -Methode führt dazu, dass der **OfficeClickToRun** -Dienst sofort alle Office-Anwendungen herunterfährt, die ausgeführt werden und das Update anwenden.</span><span class="sxs-lookup"><span data-stu-id="a73b4-173">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down any Office applications that are running and apply the update.</span></span> <span data-ttu-id="a73b4-174">Dem Benutzer treten möglicherweise Daten auf, da Sie nicht zum Speichern von Änderungen an geöffneten Dokumenten aufgefordert werden..</span><span class="sxs-lookup"><span data-stu-id="a73b4-174">The user may experience data as they are not prompted to save changes to open documents..</span></span> 
    
- <span data-ttu-id="a73b4-175">Diese Aktion kann nur ausgelöst werden, wenn der com-Status einer der folgenden ist:</span><span class="sxs-lookup"><span data-stu-id="a73b4-175">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="a73b4-176">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="a73b4-176">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="a73b4-177">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="a73b4-177">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="a73b4-178">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="a73b4-178">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="a73b4-179">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="a73b4-179">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="a73b4-180">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="a73b4-180">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="a73b4-181">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="a73b4-181">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="a73b4-182">Wenn Sie die **Apply** -Methode aufrufen, ohne Inhalt zuvor herunterzuladen, wird die **Apply** -Methode den Bericht **erfolgreich ausgeführt** , da Sie festgestellt hat, dass nichts angewendet und der **Apply** -Prozess erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="a73b4-182">If you call the **Apply** method without previously downloading content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
### <a name="cancel"></a><span data-ttu-id="a73b4-183">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="a73b4-183">Cancel</span></span>

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a><span data-ttu-id="a73b4-184">Ergebnisse zurückgeben</span><span class="sxs-lookup"><span data-stu-id="a73b4-184">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a73b4-185">S_OK</span><span class="sxs-lookup"><span data-stu-id="a73b4-185">S_OK</span></span>  <br/> |<span data-ttu-id="a73b4-186">Aktion wurde erfolgreich an den Klick-und-Los-Dienst zur Ausführung übermittelt.</span><span class="sxs-lookup"><span data-stu-id="a73b4-186">Action was successfully submitted to the Click-to-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="a73b4-187">E_ILLEGAL_METHOD_CALL</span><span class="sxs-lookup"><span data-stu-id="a73b4-187">E_ILLEGAL_METHOD_CALL</span></span>  <br/> |<span data-ttu-id="a73b4-188">Die Aktion ist zu diesem Zeitpunkt nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="a73b4-188">Action is not allowed at this time.</span></span> <span data-ttu-id="a73b4-189">Weitere Informationen finden Sie im Abschnitt " [Hinweise](#bk_CancelRemarks) ".</span><span class="sxs-lookup"><span data-stu-id="a73b4-189">See the [Remarks](#bk_CancelRemarks) section for more information</span></span>  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a><span data-ttu-id="a73b4-190">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a73b4-190">Remarks</span></span>

- <span data-ttu-id="a73b4-191">Diese Methode kann nur ausgelöst werden, wenn die com-Status-ID **eDOWNLOAD_WIP**.</span><span class="sxs-lookup"><span data-stu-id="a73b4-191">This method can only be triggered when the COM status id **eDOWNLOAD_WIP**.</span></span> <span data-ttu-id="a73b4-192">Es wird versucht, die aktuelle Download Aktion abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="a73b4-192">It will attempt to cancel the current download action.</span></span> <span data-ttu-id="a73b4-193">Der com-Status wechselt in **eDOWNLOAD_CANCELLING** und ändert sich schließlich in **eDOWNLOAD_CANCELED**.</span><span class="sxs-lookup"><span data-stu-id="a73b4-193">The COM status will change to **eDOWNLOAD_CANCELLING** and eventually change to **eDOWNLOAD_CANCELED**.</span></span> <span data-ttu-id="a73b4-194">Der com-Status gibt **E_ILLEGAL_METHOD_CALL** zurück, wenn Sie zu einem anderen Zeitpunkt ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="a73b4-194">The COM status will return **E_ILLEGAL_METHOD_CALL** if triggered at any other time.</span></span> 
    
### <a name="download"></a><span data-ttu-id="a73b4-195">Herunterladen</span><span class="sxs-lookup"><span data-stu-id="a73b4-195">Download</span></span>

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a><span data-ttu-id="a73b4-196">Parameter</span><span class="sxs-lookup"><span data-stu-id="a73b4-196">Parameters</span></span>

-  <span data-ttu-id="a73b4-197">_Display Level_: **true** , um den Installationsstatus, einschließlich Fehlern, während des Updateprozesses anzuzeigen; **false** , um den Installationsstatus, einschließlich Fehlern, während des Aktualisierungsvorgangs auszublenden.</span><span class="sxs-lookup"><span data-stu-id="a73b4-197">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="a73b4-198">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="a73b4-198">The default is **false**.</span></span>
    
-  <span data-ttu-id="a73b4-199">_updatebaseurl_: URL zur alternativen Download Quelle.</span><span class="sxs-lookup"><span data-stu-id="a73b4-199">_updatebaseurl_: URL to the alternate download source.</span></span>
    
-  <span data-ttu-id="a73b4-200">_updatetoversion_: die Version, auf der Office aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a73b4-200">_updatetoversion_: The version to update Office to.</span></span> <span data-ttu-id="a73b4-201">Definieren Sie diesen Parameter, wenn Sie eine ältere Version als die aktuell installierte Version aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="a73b4-201">Define this parameter if you want to update to an older version than the version that is currently installed.</span></span>
    
-  <span data-ttu-id="a73b4-202">_downloadsource_: CLSID der angepassten **IBackgroundCopyManager** -Implementierung (Bits-Manager).</span><span class="sxs-lookup"><span data-stu-id="a73b4-202">_downloadsource_: CLSID of the customized **IBackgroundCopyManager** implementation (BITS manager).</span></span> 
    
-  <span data-ttu-id="a73b4-203">_Content_-Kennung: gibt den Inhalt an, der vom Inhaltsserver über den angepassten Bits-Manager heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a73b4-203">_contentid_: Identifies the content to download from the content server through the customized BITS manager.</span></span> <span data-ttu-id="a73b4-204">Dieser Wert wird über die Bits-Schnittstelle zur Interpretation übergeben.</span><span class="sxs-lookup"><span data-stu-id="a73b4-204">This value is passed through the BITS interface for interpretation.</span></span>
    
#### <a name="return-results"></a><span data-ttu-id="a73b4-205">Ergebnisse zurückgeben</span><span class="sxs-lookup"><span data-stu-id="a73b4-205">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a73b4-206">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="a73b4-206">**S_OK**</span></span> <br/> |<span data-ttu-id="a73b4-207">Aktion wurde erfolgreich an den Klick-und-Los-Dienst zur Ausführung übermittelt.</span><span class="sxs-lookup"><span data-stu-id="a73b4-207">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="a73b4-208">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="a73b4-208">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="a73b4-209">Der Aufrufer wird nicht mit erhöhten Rechten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a73b4-209">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="a73b4-210">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="a73b4-210">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="a73b4-211">Ungültige Parameter wurden übergeben.</span><span class="sxs-lookup"><span data-stu-id="a73b4-211">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="a73b4-212">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="a73b4-212">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="a73b4-213">Die Aktion ist zu diesem Zeitpunkt nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="a73b4-213">Action is not allowed at this time.</span></span> <span data-ttu-id="a73b4-214">Weitere Informationen finden Sie unter [Hinweise](#bk_DownloadRemark) .</span><span class="sxs-lookup"><span data-stu-id="a73b4-214">See [Remarks](#bk_DownloadRemark) for more information.</span></span>  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="a73b4-215">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a73b4-215">Remarks</span></span>

- <span data-ttu-id="a73b4-216">Sie müssen  _downloadsource_ und  _Content_ -Nr als Paar angeben.</span><span class="sxs-lookup"><span data-stu-id="a73b4-216">You must specify  _downloadsource_ and  _contentid_ as a pair.</span></span> <span data-ttu-id="a73b4-217">Wenn dies nicht der Fall ist, gibt die **Download** -Methode einen **E_INVALIDARG** Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="a73b4-217">If not, the **Download** method will return an **E_INVALIDARG** error.</span></span> 
    
- <span data-ttu-id="a73b4-218">Wenn  _downloadsource_,  _Content_-und  _updatebaseurl_ bereitgestellt werden, wird  _updatebaseurl_ ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a73b4-218">If  _downloadsource_,  _contentid_, and  _updatebaseurl_ are provided,  _updatebaseurl_ will be ignored.</span></span> 
    
- <span data-ttu-id="a73b4-219">Diese Aktion kann nur ausgelöst werden, wenn der com-Status einer der folgenden ist:</span><span class="sxs-lookup"><span data-stu-id="a73b4-219">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="a73b4-220">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="a73b4-220">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="a73b4-221">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="a73b4-221">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="a73b4-222">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="a73b4-222">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="a73b4-223">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="a73b4-223">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="a73b4-224">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="a73b4-224">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="a73b4-225">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="a73b4-225">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="a73b4-226">Wenn Sie die **Apply** -Methode ohne zuvor heruntergeladenen Inhalt aufrufen, wird die **Apply** -Methode den Bericht **erfolgreich ausgeführt** , da Sie festgestellt hat, dass nichts angewendet und der **Apply** -Prozess erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="a73b4-226">If you call the **Apply** method without previously downloaded content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
#### <a name="examples"></a><span data-ttu-id="a73b4-227">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a73b4-227">Examples</span></span>

- <span data-ttu-id="a73b4-228">So laden Sie den Inhalt aus dem angepassten Bits-Manager herunter: Rufen Sie die **Download ()** -Funktion auf, indem Sie die folgenden Parameter übergeben:</span><span class="sxs-lookup"><span data-stu-id="a73b4-228">To download the content from the customized BITS manager: Call the **download()** function passing the following parameters:</span></span> 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- <span data-ttu-id="a73b4-229">So laden Sie die Inhalte aus dem Office Content Delivery Network (CDN) herunter: Rufen Sie die **Download ()** -Funktion ohne Angabe der Parameter  _downloadsource_,  _contentbar_oder  _updatebaseurl_ .</span><span class="sxs-lookup"><span data-stu-id="a73b4-229">To download the content from the Office Content Delivery Network (CDN): Call the **download()** function without specifying the  _downloadsource_,  _contentid_, or  _updatebaseurl_ parameters.</span></span> 
    
- <span data-ttu-id="a73b4-230">So laden Sie die Inhalte von einem benutzerdefinierten Speicherort herunter: Rufen Sie die **Download ()-** Funktion auf, indem Sie den folgenden Parameter übergeben:</span><span class="sxs-lookup"><span data-stu-id="a73b4-230">To download the content from a customized location: Call the **download()** function passing the following parameter:</span></span> 
    
  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a><span data-ttu-id="a73b4-231">Status</span><span class="sxs-lookup"><span data-stu-id="a73b4-231">Status</span></span>

```cpp
typdef struct _UPDATE_STATUS_REPORT
{
    UPDATE_STATUS status;
    UINT error;
    LPCWSTR contentid;
}UPDATE_STATUS_REPORT;
HRESULT status([out] _UPDATE_STATUS_REPORT& pUpdateStatusReport) // Get status of current action
```

#### <a name="parameters"></a><span data-ttu-id="a73b4-232">Parameter</span><span class="sxs-lookup"><span data-stu-id="a73b4-232">Parameters</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="a73b4-233">_pUpdateStatusReport_</span><span class="sxs-lookup"><span data-stu-id="a73b4-233">_pUpdateStatusReport_</span></span> <br/> |<span data-ttu-id="a73b4-234">Zeiger auf eine UPDATE_STATUS_REPORT Struktur.</span><span class="sxs-lookup"><span data-stu-id="a73b4-234">Pointer to an UPDATE_STATUS_REPORT structure.</span></span>  <br/> |
   
#### <a name="return-results"></a><span data-ttu-id="a73b4-235">Ergebnisse zurückgeben</span><span class="sxs-lookup"><span data-stu-id="a73b4-235">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a73b4-236">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="a73b4-236">**S_OK**</span></span> <br/> |<span data-ttu-id="a73b4-237">Die **Status** -Methode gibt immer dieses Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="a73b4-237">The **Status** method always returns this result.</span></span> <span data-ttu-id="a73b4-238">Überprüfen Sie die  `UPDATE_STATUS_RESULT` Struktur auf den Status der aktuellen Aktion.</span><span class="sxs-lookup"><span data-stu-id="a73b4-238">Inspect the  `UPDATE_STATUS_RESULT` structure for the status of the current action.</span></span>  <br/> |
   
#### <a name="remarks"></a><span data-ttu-id="a73b4-239">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a73b4-239">Remarks</span></span>

- <span data-ttu-id="a73b4-240">Das Feld Status des  `UPDATE_STATUS_REPORT` enthält den Status der aktuellen Aktion.</span><span class="sxs-lookup"><span data-stu-id="a73b4-240">The status field of the  `UPDATE_STATUS_REPORT` contains the status of the current action.</span></span> <span data-ttu-id="a73b4-241">Einer der folgenden Statuswerte wird zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="a73b4-241">One of the following status values is returned:</span></span> 
    
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

- <span data-ttu-id="a73b4-242">Wenn der letzte Befehl zu einem Fehler geführt hat, enthält das Feld Error des-Fehlers  `UPDATE_STATUS_REPORT` detaillierte Informationen zu dem Fehler.</span><span class="sxs-lookup"><span data-stu-id="a73b4-242">If the last command resulted in an error, the error field of the  `UPDATE_STATUS_REPORT` contains detailed information about the error.</span></span> <span data-ttu-id="a73b4-243">Zwei Arten von Fehlercodes werden von der **Status** -Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a73b4-243">Two types of error codes are returned from the **Status** method.</span></span> 
    
- <span data-ttu-id="a73b4-244">Wenn der Fehler kleiner als  `UPDATE_ERROR_CODE::eUNKNOWN` ist, ist der Fehler einer der folgenden vordefinierten Fehlercodes:</span><span class="sxs-lookup"><span data-stu-id="a73b4-244">If the error less than  `UPDATE_ERROR_CODE::eUNKNOWN`, the error is one of the following pre-defined error codes:</span></span>
    
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

  <span data-ttu-id="a73b4-245">Wenn der Rückgabefehlercode größer als  `UPDATE_ERROR_CODE::eUNKNOWN` der **HRESULT** -Wert eines fehlgeschlagenen Funktionsaufrufs ist.</span><span class="sxs-lookup"><span data-stu-id="a73b4-245">If the return error code is larger than  `UPDATE_ERROR_CODE::eUNKNOWN` it is the **HRESULT** of a failed function call.</span></span> <span data-ttu-id="a73b4-246">So extrahieren Sie das HRESULT subtrahieren  `UPDATE_ERROR_CODE::eUNKNOWN` aus dem Wert, der im Feld Error von zurückgegeben wird  `UPDATE_STATUS_REPORT` .</span><span class="sxs-lookup"><span data-stu-id="a73b4-246">To extract the HRESULT subtract  `UPDATE_ERROR_CODE::eUNKNOWN` from the value returned in the error field of the  `UPDATE_STATUS_REPORT`.</span></span>
    
  <span data-ttu-id="a73b4-247">Die vollständige Liste der Status-und Fehlerwerte kann angezeigt werden, indem die in OfficeC2RCom.dll eingebettete **IUpdateNotify** -Typbibliothek überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="a73b4-247">The complete list of status and error values can be viewed by inspecting the **IUpdateNotify** type library embedded in OfficeC2RCom.dll.</span></span> 
    
- <span data-ttu-id="a73b4-248">Das Feld "Content-Nr" wird für Aufrufe von **Status** verwendet, nachdem der **Download** initiiert wurde, und gibt die Inhalts-Nr zurück, die an den **Download** Aufruf übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="a73b4-248">The contentid field is used for calls to **Status** after **Download** has initiated and returns the contentid that was passed in to the **Download** call.</span></span> <span data-ttu-id="a73b4-249">Es wird empfohlen, dieses Feld vor dem Aufrufen der **Status** -Methode auf **null** zu initialisieren und anschließend den Wert nach dem Zurückgeben des **Status** zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a73b4-249">It is a best practice to initialize this field to **null** before you call the **Status** method and then check the value after **Status** has been returned.</span></span> <span data-ttu-id="a73b4-250">Wenn der Wert immer noch **null**ist, bedeutet dies, dass keine Inhalts-Nr vorhanden ist, die zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="a73b4-250">If the value is still **null**, that means there is no contentid to return.</span></span> <span data-ttu-id="a73b4-251">Wenn der Wert nicht **null**ist, müssen Sie ihn mit einem Aufruf von **sysfree String ()** freigeben.</span><span class="sxs-lookup"><span data-stu-id="a73b4-251">If the value is not **null**, you need to free it with a call to **SysFreeString()**.</span></span> <span data-ttu-id="a73b4-252">Im folgenden finden Sie einen Codeausschnitt zum Aufrufen des **Status** nach dem **Download**.</span><span class="sxs-lookup"><span data-stu-id="a73b4-252">Here is a code snippet of how to call **Status** after **Download**.</span></span>
    
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

### <a name="summary-of-iupdatenotify2-interface"></a><span data-ttu-id="a73b4-253">Zusammenfassung der IUpdateNotify2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a73b4-253">Summary of IUpdateNotify2 interface</span></span>

<span data-ttu-id="a73b4-254">In Version [16.0.8208.6352] wurde eine neue **IUpdateNotify2** -Schnittstelle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a73b4-254">From version [16.0.8208.6352] we have added a new **IUpdateNotify2** interface.</span></span> 
  
- <span data-ttu-id="a73b4-255">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span><span class="sxs-lookup"><span data-stu-id="a73b4-255">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span></span>
    
- <span data-ttu-id="a73b4-256">Diese Schnittstelle hat auch die ursprüngliche IUpdateNotify-Schnittstelle gehostet, um Abwärtskompatibilität zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="a73b4-256">This interface also hosted the original IUpdateNotify interface to provide backward compatibility.</span></span> <span data-ttu-id="a73b4-257">Das heißt, wenn Sie diese Schnittstelle verwenden, haben Sie Zugriff auf alle Methoden, die in der **UpdateNotifyObject** -Schnittstelle bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a73b4-257">Which means if you use this interface, you have access to all the methods provided in **UpdateNotifyObject** interface.</span></span> 
    
- <span data-ttu-id="a73b4-258">Neue Methoden zu IUpdateNotify2 hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="a73b4-258">New methods added to IUpdateNotify2:</span></span>
    
  - <span data-ttu-id="a73b4-259">**HRESULT** GetBlockingApps (BSTR \* -appsliste).</span><span class="sxs-lookup"><span data-stu-id="a73b4-259">**HRESULT** GetBlockingApps([out] BSTR \* AppsList).</span></span> <span data-ttu-id="a73b4-260">Updates blockieren apps-Liste abrufen.</span><span class="sxs-lookup"><span data-stu-id="a73b4-260">Get updates blocking apps list.</span></span> <span data-ttu-id="a73b4-261">Bei diesem Aufruf werden ausgeführte Office-Apps zurückgegeben, wodurch der Aktualisierungsprozess blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="a73b4-261">This call will return running Office apps which will block the update process from proceeding.</span></span> 
    
  - <span data-ttu-id="a73b4-262">**HRESULT** GetOfficeDeploymentData ([in] int DataType, [in] **ein LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span><span class="sxs-lookup"><span data-stu-id="a73b4-262">**HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span></span> <span data-ttu-id="a73b4-263">Abrufen von Office-Bereitstellungsdaten</span><span class="sxs-lookup"><span data-stu-id="a73b4-263">Get Office deployment Data.</span></span> 
    
- <span data-ttu-id="a73b4-264">Wenn Sie die neuen Methoden verwenden möchten, müssen Sie Folgendes sicherstellen:</span><span class="sxs-lookup"><span data-stu-id="a73b4-264">If you want to use the new methods, you need to make sure:</span></span>
    
  - <span data-ttu-id="a73b4-265">Ihre C2R-Version ist neuer als der obige Build ( \> = June Fork Build).</span><span class="sxs-lookup"><span data-stu-id="a73b4-265">Your C2R version is newer than the above build (\>= June fork build).</span></span>
    
  - <span data-ttu-id="a73b4-266">Verwenden Sie UpdateNotifyObject2 anstelle von **UpdateNotifyObject** , um **CoCreateInstance**aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="a73b4-266">Use UpdateNotifyObject2, instead of **UpdateNotifyObject** to call **CoCreateInstance**.</span></span>
    
<span data-ttu-id="a73b4-267">Wenn Sie keine der neuen Methoden verwenden, müssen Sie nichts ändern.</span><span class="sxs-lookup"><span data-stu-id="a73b4-267">If you don't use any of the new methods, you don't need to change anything.</span></span> <span data-ttu-id="a73b4-268">Alle vorhandenen Methoden funktionieren genauso genau wie zuvor.</span><span class="sxs-lookup"><span data-stu-id="a73b4-268">All the existing methods will work as exact the same way as before.</span></span>
  
## <a name="implementing-the-bits-interface"></a><span data-ttu-id="a73b4-269">Implementieren der Bits-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a73b4-269">Implementing the BITS interface</span></span>

<span data-ttu-id="a73b4-270">Der [intelligente Hintergrundübertragungsdienst (Background Intelligent Transfer Service](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) , Bits) ist ein von Microsoft bereitgestellter Dienst zum Übertragen von Dateien zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="a73b4-270">The [Background Intelligent Transfer Service](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) (BITS) is a service provided by Microsoft to transfer files between a client and server.</span></span> <span data-ttu-id="a73b4-271">Bits ist einer der Kanäle, die von einem Office-Klick-und-Los-Installationsprogramm zum Herunterladen von Inhalten verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a73b4-271">BITS is one of the channels that Office Click-To-Run installer can use to download content.</span></span> <span data-ttu-id="a73b4-272">Standardmäßig verwendet das Click-to-Run-Installationsprogramm von Microsoft 365 Apps die in der Implementierung von Bits integrierte Windows-Datei, um den Inhalt aus dem CDN herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="a73b4-272">By default, the Microsoft 365 Apps Click-To-Run installer uses the Windows' built in implementation of BITS to download the content from the CDN.</span></span> 
  
<span data-ttu-id="a73b4-273">Durch die Bereitstellung einer angepassten Bits-Implementierung für die **Download ()** -Methode der **IUpdateNotify** -Schnittstelle kann Ihre Verwaltbarkeit-Software steuern, wo und wie der Client den Inhalt herunterlädt.</span><span class="sxs-lookup"><span data-stu-id="a73b4-273">By providing a customized BITS implementation to the **download()** method of the **IUpdateNotify** interface, your manageability software can control where and how the client downloads the content.</span></span> <span data-ttu-id="a73b4-274">Eine angepasste Bits-Schnittstelle ist nützlich, wenn ein benutzerdefinierter Inhalts Verteilungskanal als die integrierten Klick-und-Los-Kanäle bereitgestellt wird, beispielsweise die CDN-, IIS-Server oder Dateifreigaben.</span><span class="sxs-lookup"><span data-stu-id="a73b4-274">A customized BITS interface is useful when providing a custom content distribution channel other than the Click-to-Run built-in channels, such as the CDN, IIS servers, or file shares.</span></span> 
  
<span data-ttu-id="a73b4-275">Die Mindestanforderung für eine angepasste Bits-Schnittstelle für die Verwendung des Office C2R-Diensts lautet:</span><span class="sxs-lookup"><span data-stu-id="a73b4-275">The minimum requirement for a customized BITS interface to work with Office C2R service is:</span></span>
  
- <span data-ttu-id="a73b4-276">Für **IBackgroundCopyManager**:</span><span class="sxs-lookup"><span data-stu-id="a73b4-276">For **IBackgroundCopyManager**:</span></span>
    
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

- <span data-ttu-id="a73b4-277">Für **IBackgroundCopyJob**:</span><span class="sxs-lookup"><span data-stu-id="a73b4-277">For **IBackgroundCopyJob**:</span></span>
    
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

- <span data-ttu-id="a73b4-278">Für **IBackgroundCopyJob3**:</span><span class="sxs-lookup"><span data-stu-id="a73b4-278">For **IBackgroundCopyJob3**:</span></span>
    
  ```cpp
  HRESULT _stdcall AddFileWithRanges(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName,
                      [in] DWORD RangeCount,
                      [in] BG_FILE_RANGE Ranges[])
  
  ```

- <span data-ttu-id="a73b4-279">Für die  `Addfile` -und-  `AddFileWithRanges` Funktionen hat die Remote-URL folgendes Format:</span><span class="sxs-lookup"><span data-stu-id="a73b4-279">For the  `Addfile` and  `AddFileWithRanges` functions, the remote URL is in the following format:</span></span> 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - <span data-ttu-id="a73b4-280">cmbits ist hart codiert und steht für angepasste Bits.</span><span class="sxs-lookup"><span data-stu-id="a73b4-280">cmbits is hard coded, and stands for customized BITS.</span></span>
    
  -  <span data-ttu-id="a73b4-281">_\<contentid\>_ ist der  _Inhaltstyp_ -Parameter für die **Download ()** -Methode.</span><span class="sxs-lookup"><span data-stu-id="a73b4-281">_\<contentid\>_ is the  _contentid_ parameter for the **Download()** method.</span></span> 
    
  -  <span data-ttu-id="a73b4-282">_\<relative path to target file\>_ Gibt den Speicherort und den Dateinamen der herunterzuladenden Datei an.</span><span class="sxs-lookup"><span data-stu-id="a73b4-282">_\<relative path to target file\>_ provides the location and file name of the file to download.</span></span> 
    
    <span data-ttu-id="a73b4-283">Wenn Sie beispielsweise eine  _Inhalts_ -Nr für  `f732af58-5d86-4299-abe9-7595c35136ef` die **Download ()** -Methode bereitgestellt haben und Office C2R die Version der CAB-Datei (beispielsweise Datei) herunterladen möchte,  `v32.cab` wird **AddFile ()** mit folgendem Aufruf aufgerufen  `RemoteUrl` :</span><span class="sxs-lookup"><span data-stu-id="a73b4-283">For example, if you have provided a  _contentid_ of  `f732af58-5d86-4299-abe9-7595c35136ef` to the **Download()** method, and Office C2R wants to download the version cab file, such as  `v32.cab` file, it will call **AddFile()** with the following  `RemoteUrl`:</span></span>
    
  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- <span data-ttu-id="a73b4-284">Für **IBackgroundCopyError**:</span><span class="sxs-lookup"><span data-stu-id="a73b4-284">For **IBackgroundCopyError**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- <span data-ttu-id="a73b4-285">Für **IBackgroundCopyFile**:</span><span class="sxs-lookup"><span data-stu-id="a73b4-285">For **IBackgroundCopyFile**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetLocalName([out] LPWSTR *ppName); 
  HRESULT _stdcall GetRemoteName([out] LPWSTR *ppName);
  
  ```
## <a name="automating-content-staging"></a><span data-ttu-id="a73b4-286">Automatisieren der Inhaltsbereitstellung</span><span class="sxs-lookup"><span data-stu-id="a73b4-286">Automating content staging</span></span>

<span data-ttu-id="a73b4-287">IT-Administratoren können festlegen, dass Desktop Clients automatisch Updates erhalten, wenn Sie direkt im CDN zur Verfügung stehen, oder Sie können auswählen, ob die Bereitstellung von Updates gesteuert werden soll, die über die Update Kanäle mit dem Office-Bereitstellungs Tool oder dem Microsoft Endpoint Configuration Manager zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="a73b4-287">IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the CDN or they can choose to control the deployment of updates available from the update channels using the Office Deployment Tool or Microsoft Endpoint Configuration Manager.</span></span>
  
<span data-ttu-id="a73b4-288">Der Dienst unterstützt die Möglichkeit für Verwaltungstools, den Download der Inhalte zu erkennen und zu automatisieren, wenn Updates zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a73b4-288">The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.</span></span>
  
<span data-ttu-id="a73b4-289">**Die folgende Abbildung ist eine Übersicht über das Herunterladen eines benutzerdefinierten Bilds.**</span><span class="sxs-lookup"><span data-stu-id="a73b4-289">**The following image is an overview of downloading a custom image**</span></span>

<span data-ttu-id="a73b4-290">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Ein Diagramm zur Verwendung der COM-Schnittstelle im Office-Klick-und-Los-Installationsprogramm")</span><span class="sxs-lookup"><span data-stu-id="a73b4-290">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on the Office Click-To-Run installer")</span></span>
  
### <a name="overview-of-downloading-a-custom-image"></a><span data-ttu-id="a73b4-291">Übersicht über das Herunterladen eines benutzerdefinierten Bilds</span><span class="sxs-lookup"><span data-stu-id="a73b4-291">Overview of downloading a custom image</span></span>
  
<span data-ttu-id="a73b4-292">Im vorherigen Diagramm sehen Sie, dass ein neues Microsoft 365-apps-Bild im CDN zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="a73b4-292">In the previous diagram, you see that a new Microsoft 365 Apps image is available on the CDN.</span></span> <span data-ttu-id="a73b4-293">Zusammen mit dem Microsoft 365-apps-Image steht eine API zur Verfügung, die die erforderlichen Informationen zum Aktivieren der Verwaltungssoftware zum direkten erstellen angepasster Bilder enthält, die die Verwendung des Office-Bereitstellungstools ersetzen.</span><span class="sxs-lookup"><span data-stu-id="a73b4-293">Along with the Microsoft 365 Apps image, an API is available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.</span></span>

<span data-ttu-id="a73b4-294">Ein Unternehmen konfiguriert seine WSUS so, dass die Microsoft 365-apps-Updates synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a73b4-294">An enterprise configures their WSUS to sync the Microsoft 365 Apps updates.</span></span> <span data-ttu-id="a73b4-295">Diese Updates enthalten nicht die tatsächliche Bild Nutzlast, aber die Verwaltungssoftware kann erkennen, wenn neue Inhalte verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a73b4-295">These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available.</span></span> <span data-ttu-id="a73b4-296">Die Verwaltbarkeit-Software kann dann die Microsoft 365 apps Update-Metadaten lesen, um zu verstehen, für welche Version von Office das Update gilt.</span><span class="sxs-lookup"><span data-stu-id="a73b4-296">The manageability software can then read the Microsoft 365 Apps Update metadata to understand what version of Office the update applies to.</span></span>

<span data-ttu-id="a73b4-297">Wenn das Update anwendbar ist, kann die Verwaltbarkeit-Software den CDN-Inhalt und die Dateiliste verwenden, um das benutzerdefinierte Abbild zu erstellen und es auf dem Dateifreigabespeicherort zu speichern, der für die Verwendung konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="a73b4-297">If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.</span></span>
  
### <a name="using-the-microsoft-365-apps-file-list-api"></a><span data-ttu-id="a73b4-298">Verwenden der API für Dateilisten von Microsoft 365-apps</span><span class="sxs-lookup"><span data-stu-id="a73b4-298">Using the Microsoft 365 Apps file list API</span></span>

<span data-ttu-id="a73b4-299">Die Dateilisten-API von Microsoft 365 apps dient zum Abrufen der Namen der Dateien, die für ein bestimmtes Microsoft 365-apps-Update benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="a73b4-299">The Microsoft 365 Apps file list API is used to retrieve the names of the files needed for a particular Microsoft 365 Apps update.</span></span>

<span data-ttu-id="a73b4-300">HTTP-Anforderung</span><span class="sxs-lookup"><span data-stu-id="a73b4-300">HTTP Request</span></span>

<span data-ttu-id="a73b4-301">GET https://config.office.com/api/filelist</span><span class="sxs-lookup"><span data-stu-id="a73b4-301">GET https://config.office.com/api/filelist</span></span>

<span data-ttu-id="a73b4-302">Geben Sie für diese Methode keinen Anforderungstext an.</span><span class="sxs-lookup"><span data-stu-id="a73b4-302">Do not supply a request body for this method.</span></span>

<span data-ttu-id="a73b4-303">Zum Aufrufen dieser API sind keine Berechtigungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a73b4-303">No permissions are required to call this API.</span></span>

<span data-ttu-id="a73b4-304">Optionale Abfrageparameter</span><span class="sxs-lookup"><span data-stu-id="a73b4-304">Optional query parameters</span></span>

|<span data-ttu-id="a73b4-305">**Name**</span><span class="sxs-lookup"><span data-stu-id="a73b4-305">**Name**</span></span>|<span data-ttu-id="a73b4-306">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a73b4-306">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a73b4-307">channel</span><span class="sxs-lookup"><span data-stu-id="a73b4-307">channel</span></span> <br/>| <span data-ttu-id="a73b4-308">Gibt den Kanalnamen an.</span><span class="sxs-lookup"><span data-stu-id="a73b4-308">Specifies the channel name</span></span>  <br/> <span data-ttu-id="a73b4-309">Optional – standardmäßig auf ' Halbjahresbericht '</span><span class="sxs-lookup"><span data-stu-id="a73b4-309">Optional – default to ‘SemiAnnual’</span></span> <br/> <span data-ttu-id="a73b4-310">Unterstützte Werte https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element</span><span class="sxs-lookup"><span data-stu-id="a73b4-310">Supported values https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element</span></span> |
| <span data-ttu-id="a73b4-311">Version</span><span class="sxs-lookup"><span data-stu-id="a73b4-311">version</span></span> <br/>| <span data-ttu-id="a73b4-312">Gibt die Update Version an.</span><span class="sxs-lookup"><span data-stu-id="a73b4-312">Specifies the update version</span></span> <br/> <span data-ttu-id="a73b4-313">Optional – Standardwert ist die neueste Version, die für den angegebenen Kanal verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a73b4-313">Optional – defaults to the latest version available for the specified channel</span></span> |
| <span data-ttu-id="a73b4-314">Bogen</span><span class="sxs-lookup"><span data-stu-id="a73b4-314">arch</span></span> <br/>| <span data-ttu-id="a73b4-315">Gibt die Clientarchitektur an.</span><span class="sxs-lookup"><span data-stu-id="a73b4-315">Specifies client architecture</span></span> <br/> <span data-ttu-id="a73b4-316">Optional – standardmäßig "x64"</span><span class="sxs-lookup"><span data-stu-id="a73b4-316">Optional – defaults to ‘x64’</span></span> <br/> <span data-ttu-id="a73b4-317">Unterstützte Werte: x64, x86</span><span class="sxs-lookup"><span data-stu-id="a73b4-317">Supported values: x64, x86</span></span> |
| <span data-ttu-id="a73b4-318">lid</span><span class="sxs-lookup"><span data-stu-id="a73b4-318">lid</span></span> <br/>| <span data-ttu-id="a73b4-319">Gibt die Sprachdateien an, die eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a73b4-319">Specifies the language files to include</span></span> <br/> <span data-ttu-id="a73b4-320">Optional – Standardwert: None</span><span class="sxs-lookup"><span data-stu-id="a73b4-320">Optional – defaults to none</span></span> <br/> <span data-ttu-id="a73b4-321">Um mehrere Sprachen anzugeben, schließen Sie einen Lid-Abfrageparameter für jede Sprache ein.</span><span class="sxs-lookup"><span data-stu-id="a73b4-321">To specify multiple languages, include an lid query parameter for each language</span></span> <br/> <span data-ttu-id="a73b4-322">Verwenden Sie das Format für die Sprachen-ID, ex.</span><span class="sxs-lookup"><span data-stu-id="a73b4-322">Use the language identifier format, ex.</span></span> <span data-ttu-id="a73b4-323">"en-US", "fr-FR"</span><span class="sxs-lookup"><span data-stu-id="a73b4-323">‘en-us’, ‘fr-fr’</span></span> |
| <span data-ttu-id="a73b4-324">AllLanguages</span><span class="sxs-lookup"><span data-stu-id="a73b4-324">alllanguages</span></span> <br/>| <span data-ttu-id="a73b4-325">Gibt an, dass alle Sprachdateien eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a73b4-325">Specifies to include all language files</span></span> <br/> <span data-ttu-id="a73b4-326">Optional – Standardwert ist false</span><span class="sxs-lookup"><span data-stu-id="a73b4-326">Optional – defaults to false</span></span> |

<span data-ttu-id="a73b4-327">HTTP-Antwort</span><span class="sxs-lookup"><span data-stu-id="a73b4-327">HTTP Response</span></span>

<span data-ttu-id="a73b4-328">Wenn die Methode erfolgreich verläuft, werden der Antwortcode 200 OK und eine Sammlung von File-Objekten im Antworttext zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a73b4-328">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>

<span data-ttu-id="a73b4-329">Führen Sie die folgenden Schritte aus, um ein Bild zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="a73b4-329">To create an image, follow these steps:</span></span>
1.  <span data-ttu-id="a73b4-330">Rufen Sie die API auf, und stellen Sie die entsprechenden Abfrageparameter für den Kanal, die Version und die Architektur des Updates bereit, das Sie interessieren.</span><span class="sxs-lookup"><span data-stu-id="a73b4-330">Call the API, providing the appropriate query parameters for the channel, version and architecture of the update you are interested in.</span></span>
<span data-ttu-id="a73b4-331">Hinweis: Dateiobjekte mit dem Attribut "LCID": "0" sind sprachneutrale Dateien und müssen in das Bild aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="a73b4-331">Note: File objects with the attribute "lcid": "0" are language neutral files and must be included in the image.</span></span>
2.  <span data-ttu-id="a73b4-332">Erstellen Sie ein lokales Image des CDN, indem Sie die File-Objekte durchlaufen und die CDN-Dateien kopieren, während Sie die Ordnerstruktur entsprechend dem Attribut "relativePath" erstellen, das für die einzelnen Dateiobjekte definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a73b4-332">Construct a local image of the CDN by iterating through the file objects and copying the CDN files, while creating the folder structure as specified by the “relativePath” attribute defined for each of the file objects.</span></span>

<span data-ttu-id="a73b4-333">Im folgenden Beispiel wird die Dateiliste für den aktuellen Kanal und die Version 16.0.4229.1004 für 64bit abgerufen und die Sprachdateien Französisch und Englisch eingeschlossen:</span><span class="sxs-lookup"><span data-stu-id="a73b4-333">The following example retrieves the file list for the Current Channel and version 16.0.4229.1004 for 64bit and includes the French and English language files:</span></span>

```http
Get https://config.office.com/api/filelist?Channel=Current&Version=16.0.4229.1004&Arch=x64&Lid=fr-fr&Lid=en-US
```

### <a name="hash-verification-of-dat-files"></a><span data-ttu-id="a73b4-334">Hash Überprüfung von DAT-Dateien</span><span class="sxs-lookup"><span data-stu-id="a73b4-334">Hash verification of .dat files</span></span>

<span data-ttu-id="a73b4-335">Bilder Erstellungstools können die Integrität der heruntergeladenen DAT-Dateien überprüfen, indem Sie einen berechneten Hashwert mit dem bereitgestellten Hashwert vergleichen, der den einzelnen DAT-Dateien zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a73b4-335">Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed hash value with the supplied hash value associated with each of the .dat files.</span></span> <span data-ttu-id="a73b4-336">Es folgt ein Beispiel für ein File-Objekt, das hashLocation-und hashAlgorithm-Werte angibt:</span><span class="sxs-lookup"><span data-stu-id="a73b4-336">Following is an example of a file object that specifies hashLocation and hashAlgorithm values:</span></span>
  
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

- <span data-ttu-id="a73b4-337">Das **hashLocation** -Attribut gibt den relativen Pfadspeicherort der CAB-Datei an, die den Hashwert enthält.</span><span class="sxs-lookup"><span data-stu-id="a73b4-337">The **hashLocation** attribute specifies the relative path location of .cab file that contains the hash value.</span></span> <span data-ttu-id="a73b4-338">Erstellen Sie den Speicherort der Hash Datei, indem Sie URL + relativePath + hashLocation verketten.</span><span class="sxs-lookup"><span data-stu-id="a73b4-338">Construct the hash file location by concatenating URL + relativePath + hashLocation.</span></span> <span data-ttu-id="a73b4-339">Im folgenden Beispiel wäre der Speicherort Stream.x64.bg-bg. Hash wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a73b4-339">In the following example, the stream.x64.bg-bg.hash location would be:</span></span> 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- <span data-ttu-id="a73b4-340">Das Attribut **hashAlgorithm** gibt an, welcher Hashalgorithmus verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="a73b4-340">The **hashAlgorithm** attribute specifies what hashing algorithm was used.</span></span> 
    
  <span data-ttu-id="a73b4-341">Um die Integrität der Datei Stream.x64.bg-bg. dat zu überprüfen, öffnen Sie den Stream.x64.bg-bg. Hash und lesen Sie den Hashwert, der die erste Textzeile in der Hash Datei ist.</span><span class="sxs-lookup"><span data-stu-id="a73b4-341">To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the HASH value which is the first line of text in the hash file.</span></span> <span data-ttu-id="a73b4-342">Vergleichen Sie diesen Wert mit dem berechneten Hashwert (mithilfe des angegebenen Hashalgorithmus), um die Integrität der heruntergeladenen DAT-Datei zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a73b4-342">Compare this to the computed hash value (using the specified hashing algorithm) to verify the integrity of the downloaded .dat file.</span></span>
    
  <span data-ttu-id="a73b4-343">Im folgenden Beispiel wird der C#-Code zum Lesen des Hashs gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a73b4-343">The following example shows the C# code to read the hash.</span></span>
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="microsoft-365-apps-updates"></a><span data-ttu-id="a73b4-344">Updates für Microsoft 365-apps</span><span class="sxs-lookup"><span data-stu-id="a73b4-344">Microsoft 365 Apps Updates</span></span>

<span data-ttu-id="a73b4-345">Alle Microsoft 365-apps-Updates werden im [Microsoft Update-Katalog](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client)veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="a73b4-345">All Microsoft 365 Apps Updates are published to the [Microsoft Update Catalog](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span></span>
  
<span data-ttu-id="a73b4-346">Microsoft 365 apps-Updates ermöglichen eine verwaltbare Software zur Behandlung von Microsoft 365-apps Updates auf eine Art und Weise, die einem anderen Wu-Update mit einer Ausnahme ähnelt. die Clientupdates enthalten keine tatsächliche Nutzlast.</span><span class="sxs-lookup"><span data-stu-id="a73b4-346">Microsoft 365 Apps Updates enable manageability software to treat Microsoft 365 Apps Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload.</span></span> <span data-ttu-id="a73b4-347">Die Updates für Microsoft 365-apps sollten nicht auf allen Clients installiert werden, sondern verwendet werden, um die Workflows mit der Verwaltungssoftware auszulösen, wobei der Installationsbefehl durch den oben gezeigten com-basierten Installationsmechanismus ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="a73b4-347">The Microsoft 365 Apps Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.</span></span>

<span data-ttu-id="a73b4-348">**In der folgenden Abbildung ist ein Diagramm des Office 365-Client Update Workflows dargestellt.**</span><span class="sxs-lookup"><span data-stu-id="a73b4-348">**The following figure shows a diagram of the Office 365 Client Update workflow.**</span></span>

<span data-ttu-id="a73b4-349">![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow Diagramm für O365PP-Clientupdates")</span><span class="sxs-lookup"><span data-stu-id="a73b4-349">![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")</span></span>
  
<span data-ttu-id="a73b4-350">Jedes veröffentlichte Microsoft 365-apps-Update enthält Metadaten zum Update.</span><span class="sxs-lookup"><span data-stu-id="a73b4-350">Each Microsoft 365 Apps Update that is published includes metadata about the update.</span></span> <span data-ttu-id="a73b4-351">Diese Metadaten enthalten einen Parameter namens MoreInfoUrl, der zum Ableiten des API-Aufrufs an die Dateilisten-API für das jeweilige Update verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a73b4-351">This metadata includes a parameter called MoreInfoUrl which can be used to derive the API call to the file list API for that specific update.</span></span>

<span data-ttu-id="a73b4-352">Im folgenden Beispiel wird die Dateilisten-API in das MoreInfoUrl-Verzeichnis eingebettet und beginnt mit "ServicePath =".</span><span class="sxs-lookup"><span data-stu-id="a73b4-352">In the following example, the file list API is embedded in the MoreInfoURL and starts with “ServicePath=”</span></span>

<span data-ttu-id="a73b4-353">http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath =https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True</span><span class="sxs-lookup"><span data-stu-id="a73b4-353">http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath=https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True</span></span>
  
### <a name="additional-metadata-for-automating-content-staging"></a><span data-ttu-id="a73b4-354">Zusätzliche Metadaten zum Automatisieren der Inhaltsbereitstellung</span><span class="sxs-lookup"><span data-stu-id="a73b4-354">Additional metadata for automating content staging</span></span>

<span data-ttu-id="a73b4-355">**Versionsverlaufs-API**</span><span class="sxs-lookup"><span data-stu-id="a73b4-355">**Release History API**</span></span>
  
<span data-ttu-id="a73b4-356">Die Microsoft 365 apps-Versionsverlaufs-API dient zum Abrufen von Details für jedes der im CDN veröffentlichten Updates zusammen mit den Kanalnamen und anderen Kanal Attributen.</span><span class="sxs-lookup"><span data-stu-id="a73b4-356">The Microsoft 365 Apps release history API is used to retrieve details for each of the updates published to the CDN along with the channel names and other channel attributes.</span></span>

<span data-ttu-id="a73b4-357">HTTP-Anforderung</span><span class="sxs-lookup"><span data-stu-id="a73b4-357">HTTP Request</span></span>

```http
GET https://config.office.com/api/filelist/channels 
```

<span data-ttu-id="a73b4-358">Geben Sie für diese Methode keinen Anforderungstext an.</span><span class="sxs-lookup"><span data-stu-id="a73b4-358">Do not supply a request body for this method.</span></span>

<span data-ttu-id="a73b4-359">Zum Aufrufen dieser API sind keine Berechtigungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a73b4-359">No permissions are required to call this API.</span></span>

<span data-ttu-id="a73b4-360">HTTP-Antwort</span><span class="sxs-lookup"><span data-stu-id="a73b4-360">HTTP Response</span></span>

<span data-ttu-id="a73b4-361">Wenn die Methode erfolgreich verläuft, werden der Antwortcode 200 OK und eine Sammlung von File-Objekten im Antworttext zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a73b4-361">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>

<span data-ttu-id="a73b4-362">**SKUs-API**</span><span class="sxs-lookup"><span data-stu-id="a73b4-362">**SKUs API**</span></span>
  
<span data-ttu-id="a73b4-363">Die SKUs-API gibt Informationen zurück, die für die Ermittlung geeignet sind, welche Produkte für die Bereitstellung und Wartung aus dem Office CDN zur Verfügung stehen, zusammen mit verschiedenen Optionen.</span><span class="sxs-lookup"><span data-stu-id="a73b4-363">The SKUs API returns information that is useful for determining which products are available for deployment and servicing from the Office CDN along with various options for each.</span></span>

<span data-ttu-id="a73b4-364">HTTP-Anforderung</span><span class="sxs-lookup"><span data-stu-id="a73b4-364">HTTP Request</span></span>

```http
GET https://config.office.com/api/filelist/skus 
```

<span data-ttu-id="a73b4-365">Geben Sie für diese Methode keinen Anforderungstext an.</span><span class="sxs-lookup"><span data-stu-id="a73b4-365">Do not supply a request body for this method.</span></span>

<span data-ttu-id="a73b4-366">Zum Aufrufen dieser API sind keine Berechtigungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a73b4-366">No permissions are required to call this API.</span></span>

<span data-ttu-id="a73b4-367">HTTP-Antwort</span><span class="sxs-lookup"><span data-stu-id="a73b4-367">HTTP Response</span></span>

<span data-ttu-id="a73b4-368">Wenn die Methode erfolgreich verläuft, werden der Antwortcode 200 OK und eine Sammlung von File-Objekten im Antworttext zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a73b4-368">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>
