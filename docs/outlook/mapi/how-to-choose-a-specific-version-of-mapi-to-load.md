---
title: Auswählen einer bestimmten zu ladenden MAPI-Version
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d353eba55e33b8ab48b3c47d2f31f1b5e0973b58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344520"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a><span data-ttu-id="71116-103">Auswählen einer bestimmten zu ladenden MAPI-Version</span><span class="sxs-lookup"><span data-stu-id="71116-103">Choose a specific version of MAPI to load</span></span>

<span data-ttu-id="71116-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71116-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71116-105">Wenn Sie explizit eine Verbindung mit einer MAPI-Implementierung herstellen, müssen Sie die zu ladende Implementierung sorgfältig auswählen.</span><span class="sxs-lookup"><span data-stu-id="71116-105">When linking explicitly to an implementation of MAPI, you must carefully select which implementation to load.</span></span> 
  
<span data-ttu-id="71116-106">Es gibt zwei Methoden, um eine explizite Verknüpfung mit einer MAPI-Implementierung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="71116-106">There are two methods to link explicitly to an implementation of MAPI.</span></span> 
  
1. <span data-ttu-id="71116-107">Sie können die MAPI-Stub-Bibliothek laden und in der Registrierung eine benutzerdefinierte DLL zum Laden und Senden von MAPI-Aufrufen an angeben.</span><span class="sxs-lookup"><span data-stu-id="71116-107">You can load the MAPI stub library, and specify in the registry a custom DLL to load and dispatch MAPI calls to.</span></span>
    
2. <span data-ttu-id="71116-108">Sie können den MAPI-Client Suchalgorithmus implementieren, um die vom Standard-e-Mail-Client verwendete Version von MAPI zu suchen und zu laden.</span><span class="sxs-lookup"><span data-stu-id="71116-108">You can implement the MAPI client lookup algorithm to look up the version of MAPI used by the default mail client and load it.</span></span>
    
<span data-ttu-id="71116-109">Da Sie die [Mapi32. dll-Stub-Registrierungseinstellungen](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) so ändern können, dass Ihre Anwendung eine beliebige Implementierung von MAPI verwendet, wird empfohlen, dass Sie Ihre Anwendung darauf verweisen, eine MAPI-Implementierung zu verwenden, mit der Sie getestet haben.</span><span class="sxs-lookup"><span data-stu-id="71116-109">Because you can change the [Mapi32.dll Stub Registry Settings](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) to direct your application to use any implementation of MAPI, we recommend that you direct your application to use an implementation of MAPI that you have tested with.</span></span> <span data-ttu-id="71116-110">Im folgenden werden beide Methoden der expliziten Verknüpfung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="71116-110">The following describes both methods of linking explicitly.</span></span> 
  
## <a name="reading-from-the-registry"></a><span data-ttu-id="71116-111">Lesen aus der Registrierung</span><span class="sxs-lookup"><span data-stu-id="71116-111">Reading from the registry</span></span>

### <a name="to-read-mapi-implementation-information-from-the-registry"></a><span data-ttu-id="71116-112">So lesen Sie Informationen zur MAPI-Implementierung aus der Registrierung</span><span class="sxs-lookup"><span data-stu-id="71116-112">To read MAPI implementation information from the registry</span></span>

1. <span data-ttu-id="71116-113">Die Registrierungsschlüssel, die eine benutzerdefinierte DLL für einen e-Mail-Client `HKLM\Software\Clients\Mail` angeben, befinden sich unter dem Schlüssel des e-Mail-Clients.</span><span class="sxs-lookup"><span data-stu-id="71116-113">The registry keys that indicate a custom DLL for a mail client are located under the  `HKLM\Software\Clients\Mail` key of the mail client.</span></span> 
    
   <span data-ttu-id="71116-114">In der folgenden Tabelle werden die folgenden Schlüssel beschrieben:</span><span class="sxs-lookup"><span data-stu-id="71116-114">The following table describes these keys:</span></span>
    
   |<span data-ttu-id="71116-115">**Taste**</span><span class="sxs-lookup"><span data-stu-id="71116-115">**Key**</span></span>|<span data-ttu-id="71116-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="71116-116">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="71116-117">MSIComponentID</span><span class="sxs-lookup"><span data-stu-id="71116-117">MSIComponentID</span></span>  <br/> |<span data-ttu-id="71116-118">Eine Windows Installer-PublishComponent Kategorie-ID (GUID), die die DLL identifiziert, die einfache MAPI-oder MAPI-Aufrufe exportiert.</span><span class="sxs-lookup"><span data-stu-id="71116-118">A Windows Installer PublishComponent category ID (GUID) that identifies the DLL that exports simple MAPI or MAPI calls.</span></span> <span data-ttu-id="71116-119">Wenn dieser Wert festgelegt ist, hat dieser Schlüssel Vorrang vor dem **DllPath** -oder **DLLPathEx** -Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="71116-119">If set, this key takes precedence over the **DLLPath** or **DLLPathEx** key.</span></span>  <br/> |
   |<span data-ttu-id="71116-120">MSIApplicationLCID</span><span class="sxs-lookup"><span data-stu-id="71116-120">MSIApplicationLCID</span></span>  <br/> |<span data-ttu-id="71116-121">Gebietsschemabezeichner (Locale Identifier, LCID) für Ihre Anwendung.</span><span class="sxs-lookup"><span data-stu-id="71116-121">Locale identifier (LCID) for your application.</span></span> <span data-ttu-id="71116-122">Der erste Zeichenfolgenwert identifiziert einen Unterschlüssel `HKLM\Software` und nachfolgende Zeichenfolgenwerte identifizieren Registrierungswerte unterhalb dieses Schlüssels, die Gebietsschemainformationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="71116-122">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key that contain locale information.</span></span>  <br/> |
   |<span data-ttu-id="71116-123">MSIOfficeLCID</span><span class="sxs-lookup"><span data-stu-id="71116-123">MSIOfficeLCID</span></span>  <br/> |<span data-ttu-id="71116-124">LCIDs für Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="71116-124">LCIDs for Microsoft Office.</span></span> <span data-ttu-id="71116-125">Der erste Zeichenfolgenwert identifiziert einen Unterschlüssel `HKLM\Software` , und nachfolgende Zeichenfolgenwerte identifizieren Registrierungswerte unterhalb dieses Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="71116-125">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key.</span></span>  <br/> |
   
   <span data-ttu-id="71116-126">Rufen Sie die Informationen aus diesen Schlüsseln ab.</span><span class="sxs-lookup"><span data-stu-id="71116-126">Obtain the information from these keys.</span></span>
    
2. <span data-ttu-id="71116-127">Übergeben Sie die Werte, die Sie aus dem vorherigen Schritt abgerufen haben, an die [FGetComponentPath](fgetcomponentpath.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="71116-127">Pass the values that you obtained from the previous step to the [FGetComponentPath](fgetcomponentpath.md) function.</span></span> <span data-ttu-id="71116-128">**FGetComponentPath** ist eine Funktion, die von der MAPI-Stub-Bibliothek mapistub. dll exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="71116-128">**FGetComponentPath** is a function that is exported by the MAPI stub library Mapistub.dll.</span></span> <span data-ttu-id="71116-129">Es gibt den Pfad der benutzerdefinierten Version von MAPI zurück.</span><span class="sxs-lookup"><span data-stu-id="71116-129">It returns the path of the custom version of MAPI.</span></span> 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a><span data-ttu-id="71116-130">So laden Sie die Implementierung von MAPI als Standard markiert</span><span class="sxs-lookup"><span data-stu-id="71116-130">To load the implementation of MAPI marked as default</span></span>

1. <span data-ttu-id="71116-131">Lesen Sie `HKLM\Software\Clients\Mail::(default)` den Registrierungswert.</span><span class="sxs-lookup"><span data-stu-id="71116-131">Read the  `HKLM\Software\Clients\Mail::(default)` registry value.</span></span> 
    
2. <span data-ttu-id="71116-132">Suchen Sie nach den Informationen für den angegebenen Client, wie zuvor beschrieben.</span><span class="sxs-lookup"><span data-stu-id="71116-132">Look up the information for the indicated client as described earlier.</span></span>
    
> [!NOTE]
> <span data-ttu-id="71116-133">Beachten Sie, dass der Standard-e-Mail-Client möglicherweise nicht Extended MAPI implementiert.</span><span class="sxs-lookup"><span data-stu-id="71116-133">Note that the default mail client might not implement Extended MAPI.</span></span> 
  
#### <a name="example"></a><span data-ttu-id="71116-134">Beispiel</span><span class="sxs-lookup"><span data-stu-id="71116-134">Example</span></span>

<span data-ttu-id="71116-135">Wenn Sie MAPI wie von Outlook implementiert laden möchten, suchen Sie die Registrierungs `HKLM\Software\Clients\Mail\Microsoft Outlook` Schlüssel unter, und übergeben Sie Sie an **FGetComponentPath**.</span><span class="sxs-lookup"><span data-stu-id="71116-135">To load MAPI as implemented by Outlook, look up the registry keys under  `HKLM\Software\Clients\Mail\Microsoft Outlook` and pass them to **FGetComponentPath**.</span></span> <span data-ttu-id="71116-136">**FGetComponentPath** gibt den Pfad für die MAPI-Implementierung von Outlook zurück.</span><span class="sxs-lookup"><span data-stu-id="71116-136">**FGetComponentPath** will return the path for Outlook's implementation of MAPI.</span></span> 
  
<span data-ttu-id="71116-137">Wenn die Schlüssel **MSIComponentID**, **MSIApplicationLCID**und **MSIOfficeLCID** nicht festgelegt sind, überprüfen Sie den Registrierungswert **DLLPathEx** .</span><span class="sxs-lookup"><span data-stu-id="71116-137">If the keys **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID** are not set, check the **DLLPathEx** registry value.</span></span> <span data-ttu-id="71116-138">Wenn die Schlüssel festgelegt sind, gibt **FGetComponentPath** den Pfad zur Implementierung der MAPI durch den Client an.</span><span class="sxs-lookup"><span data-stu-id="71116-138">If the keys are set, **FGetComponentPath** gives the path of the client's implementation of MAPI.</span></span> 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a><span data-ttu-id="71116-139">Implementieren des MAPI-Client Suchalgorithmus</span><span class="sxs-lookup"><span data-stu-id="71116-139">Implementing the MAPI Client Lookup algorithm</span></span>

<span data-ttu-id="71116-140">In der folgenden Tabelle sind die vier Funktionen von MfcMapi aufgeführt, die zum Nachschlagen des Pfads für eine benutzerdefinierte MAPI-Implementierung verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="71116-140">The following table lists the four functions from MFCMAPI that are used to look up the path for a custom implementation of MAPI:</span></span>
  
|<span data-ttu-id="71116-141">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="71116-141">**Function**</span></span>|<span data-ttu-id="71116-142">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="71116-142">**Description**</span></span>|
|:-----|:-----|
| `GetMAPIPath` <br/> |<span data-ttu-id="71116-143">Ruft den MAPI-Bibliothekspfad ab.</span><span class="sxs-lookup"><span data-stu-id="71116-143">Gets the MAPI library path.</span></span>  <br/> |
| `GetMailKey` <br/> |<span data-ttu-id="71116-144">Ruft den MAPI-e-Mail-Registrierungsschlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="71116-144">Gets the MAPI mail registry key.</span></span>  <br/> |
| `GetMapiMsiIds` <br/> |<span data-ttu-id="71116-145">Ruft den Windows Installer-Bezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="71116-145">Gets the Windows Installer identifier.</span></span>  <br/> |
| `GetComponentPath` <br/> |<span data-ttu-id="71116-146">Ruft den Komponentenpfad mithilfe von [FGetComponentPath](fgetcomponentpath.md)ab.</span><span class="sxs-lookup"><span data-stu-id="71116-146">Gets the component path using [FGetComponentPath](fgetcomponentpath.md).</span></span>  <br/> |
   
<span data-ttu-id="71116-147">Da MfcMapi die standardmäßige Implementierung von MAPI standardmäßig lädt, müssen Sie ihn explizit darauf verweisen, wenn Sie eine andere MAPI-Implementierung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="71116-147">Because MFCMAPI loads the default implementation of MAPI by default, if you want to use a different implementation of MAPI, you must explicitly direct it to do so.</span></span> <span data-ttu-id="71116-148">Dies wird mithilfe der Session\Load- **MAPI** -Routine ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71116-148">This is performed by using the **Session\Load MAPI** routine.</span></span> 
  
### <a name="how-these-functions-work"></a><span data-ttu-id="71116-149">Funktionsweise dieser Funktionen</span><span class="sxs-lookup"><span data-stu-id="71116-149">How these functions work</span></span>

1. <span data-ttu-id="71116-150">MfcMapi ruft `GetMAPIPath`an und übergibt NULL für den Parameter Client, um die MAPI-Standardimplementierung zu laden.</span><span class="sxs-lookup"><span data-stu-id="71116-150">MFCMAPI calls  `GetMAPIPath`, passing NULL for the client parameter, to load the default MAPI implementation.</span></span>
    
2.  <span data-ttu-id="71116-151">`GetMAPIPath`Aufrufe `GetMapiMsiIds` zum Lesen der Werte für **MSIComponentID**, **MSIApplicationLCID**und **MSIOfficeLCID**.</span><span class="sxs-lookup"><span data-stu-id="71116-151">`GetMAPIPath` calls  `GetMapiMsiIds` to read the values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
3.  <span data-ttu-id="71116-152">`GetMapiMsiIds`Aufrufe `GetMailKey` zum Öffnen des Registrierungsschlüssels für den standardmäßigen e-Mail-Client.</span><span class="sxs-lookup"><span data-stu-id="71116-152">`GetMapiMsiIds` calls  `GetMailKey` to open the registry key for the default mail client.</span></span> 
    
4.  <span data-ttu-id="71116-153">`GetMapiMsiIds`verwendet das Registrierungshandle, das `GetMailKey` von zurückgegeben wird, um Werte für **MSIComponentID**, **MSIApplicationLCID**und **MSIOfficeLCID**zu suchen.</span><span class="sxs-lookup"><span data-stu-id="71116-153">`GetMapiMsiIds` uses the registry handle returned by  `GetMailKey` to look up values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
5. <span data-ttu-id="71116-154">Die Werte für **MSIComponentID**, **MSIApplicationLCID**und **MSIOfficeLCID**werden an `GetMAPIPath`zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="71116-154">The values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**, are returned to  `GetMAPIPath`.</span></span>  <span data-ttu-id="71116-155">`GetMAPIPath`übergibt Sie dann an `GetComponentPath`.</span><span class="sxs-lookup"><span data-stu-id="71116-155">`GetMAPIPath` then passes them to  `GetComponentPath`.</span></span>
    
6.  <span data-ttu-id="71116-156">`GetComponentPath`lädt die MAPI-Stub-Bibliothek, Mapi32. dll, aus dem Systemverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="71116-156">`GetComponentPath` loads the MAPI stub library, Mapi32.dll, from the system directory.</span></span> 
    
7.  <span data-ttu-id="71116-157">`GetComponentPath`Ruft dann die Adresse der **FGetComponentPath** -Funktion aus Mapi32. dll ab, vorausgesetzt, Mapi32. dll exportiert **FGetComponentPath**.</span><span class="sxs-lookup"><span data-stu-id="71116-157">`GetComponentPath` then retrieves the address of the **FGetComponentPath** function from Mapi32.dll, assuming that Mapi32.dll exports **FGetComponentPath**.</span></span>
    
8. <span data-ttu-id="71116-158">Wenn beim Abrufen der Adresse von **FGetComponentPath** aus Mapi32. dll ein `GetComponentPath` Fehler auftritt, wird die Adresse aus mapistub. dll abgerufen.</span><span class="sxs-lookup"><span data-stu-id="71116-158">If getting the address of **FGetComponentPath** from Mapi32.dll fails,  `GetComponentPath` retrieves the address from Mapistub.dll.</span></span> 
    
9.  <span data-ttu-id="71116-159">`GetComponentPath`Ruft dann **FGetComponentPath**auf, wobei der Pfad der Standard Version von MAPI abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="71116-159">`GetComponentPath` then calls **FGetComponentPath**, obtaining the path of the default version of MAPI.</span></span>
    
10.  <span data-ttu-id="71116-160">`GetMAPIPath`gibt dann diesen Pfad an den Aufrufer zurück, der dann MAPI und explizit Links zu ihm lädt, wie unter [Link zu MAPI-Funktionen](how-to-link-to-mapi-functions.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="71116-160">`GetMAPIPath` then returns this path to the caller, which then loads MAPI and explicitly links to it as described in [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="71116-161">Zur Unterstützung lokalisierter Kopien von MAPI für englischsprachige und nicht Englisch `GetMAPIPath` sprachige Gebietsschemas werden die Werte für die Unterschlüssel **MSIApplicationLCID** und **MSIOfficeLCID** gelesen.</span><span class="sxs-lookup"><span data-stu-id="71116-161">To support localized copies of MAPI for English and non-English locales,  `GetMAPIPath` reads the values for the **MSIApplicationLCID** and **MSIOfficeLCID** subkeys.</span></span>  <span data-ttu-id="71116-162">`GetMAPIPath`Ruft dann **FGetComponentPath**auf, wobei zunächst **MSIApplicationLCID** als **szQualifier**und erneut **MSIOfficeLCID** als **szQualifier**angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="71116-162">`GetMAPIPath` then calls **FGetComponentPath**, first specifying **MSIApplicationLCID** as **szQualifier**, and again specifying **MSIOfficeLCID** as **szQualifier**.</span></span> <span data-ttu-id="71116-163">Weitere Informationen zu Registrierungsschlüsseln für e-Mail-Clients, die nicht englischsprachige Sprachen unterstützen, finden Sie unter [Einrichten der MSI-Schlüssel für Ihre MAPI-DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="71116-163">For more information about registry keys for mail clients that support non-English languages, see [Setting Up the MSI Keys for Your MAPI DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).</span></span>   
> - <span data-ttu-id="71116-164">Wenn MfcMapi keinen Pfad für MAPI mithilfe `GetMAPIPath`von erhält, lädt es die MAPI-Stub-Bibliothek aus dem Systemverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="71116-164">If MFCMAPI does not receive a path for MAPI using  `GetMAPIPath`, it loads the MAPI stub library from the system directory.</span></span>
> - <span data-ttu-id="71116-165">Der **MSMapiApps** -Registrierungswert, der unter [explizites Zuordnen von MAPI-aufrufen zu MAPI-DLLs](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) erörtert wird, gilt nur, wenn die MAPI-Stub-Bibliothek verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="71116-165">The **MSMapiApps** registry value discussed in [Explicitly Mapping MAPI Calls to MAPI DLLs](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) only applies when the MAPI Stub library is used.</span></span> <span data-ttu-id="71116-166">Anwendungen, die eine bestimmte MAPI-Implementierung laden oder die Standardimplementierung laden, müssen den Registrierungsschlüssel **MSMapiApps** nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="71116-166">Applications that load a specific implementation of MAPI or load the default implementation do not have to set the **MSMapiApps** registry key.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="71116-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71116-167">See also</span></span>

- [<span data-ttu-id="71116-168">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="71116-168">FGetComponentPath</span></span>](fgetcomponentpath.md)
- [<span data-ttu-id="71116-169">Übersicht über die MAPI-Programmierung</span><span class="sxs-lookup"><span data-stu-id="71116-169">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="71116-170">Verweisen auf MAPI-Funktionen</span><span class="sxs-lookup"><span data-stu-id="71116-170">Link to MAPI Functions</span></span>](how-to-link-to-mapi-functions.md)
- [<span data-ttu-id="71116-171">Registrierungseinstellungen für Mapi32. dll-Stub</span><span class="sxs-lookup"><span data-stu-id="71116-171">Mapi32.dll Stub Registry Settings</span></span>](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)
- [<span data-ttu-id="71116-172">Einrichten der MSI-Schlüssel für die MAPI-DLL</span><span class="sxs-lookup"><span data-stu-id="71116-172">Setting Up the MSI Keys for Your MAPI DLL</span></span>](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
- [<span data-ttu-id="71116-173">Explizites Zuordnen von MAPI-aufrufen zu MAPI-DLLs</span><span class="sxs-lookup"><span data-stu-id="71116-173">Explicitly Mapping MAPI Calls to MAPI DLLs</span></span>](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)

