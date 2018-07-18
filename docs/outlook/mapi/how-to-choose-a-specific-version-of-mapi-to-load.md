---
title: Wählen Sie eine bestimmte Version von MAPI geladen werden
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d0bce7b3a12f259b7ac5f28219c8a92dd2200f07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19791836"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a><span data-ttu-id="3637b-103">Wählen Sie eine bestimmte Version von MAPI geladen werden</span><span class="sxs-lookup"><span data-stu-id="3637b-103">Choose a specific version of MAPI to load</span></span>

<span data-ttu-id="3637b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3637b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3637b-105">Beim explizit auf eine Implementierung der MAPI zu verknüpfen, müssen Sie die Implementierung zum Laden sorgfältig auswählen.</span><span class="sxs-lookup"><span data-stu-id="3637b-105">When linking explicitly to an implementation of MAPI, you must carefully select which implementation to load.</span></span> 
  
<span data-ttu-id="3637b-106">Es gibt zwei Methoden zum expliziten eine Implementierung von MAPI verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="3637b-106">There are two methods to link explicitly to an implementation of MAPI.</span></span> 
  
1. <span data-ttu-id="3637b-107">Sie können die MAPI-Stub-Bibliothek zu laden, und geben in der Registrierung, die eine benutzerdefinierte DLL zum Laden und Versenden von MAPI-Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="3637b-107">You can load the MAPI stub library, and specify in the registry a custom DLL to load and dispatch MAPI calls to.</span></span>
    
2. <span data-ttu-id="3637b-108">Sie können implementieren den MAPI-Client-Lookup-Algorithmus zum Nachschlagen von der Version von MAPI, die von der standardmäßige e-Mail-Client verwendet und Laden es.</span><span class="sxs-lookup"><span data-stu-id="3637b-108">You can implement the MAPI client lookup algorithm to look up the version of MAPI used by the default mail client and load it.</span></span>
    
<span data-ttu-id="3637b-109">Da die [Mapi32.dll Stub Registrierungseinstellungen](http://msdn.microsoft.com/en-us/library/ms531218%28EXCHG.10%29.aspx) , um die Anwendung für jede Implementierung von MAPI zu leiten nicht geändert werden kann, wird empfohlen, Sie leiten die Anwendung eine Implementierung von MAPI verwendet, die Sie mit getestet haben.</span><span class="sxs-lookup"><span data-stu-id="3637b-109">Because you can change the [Mapi32.dll Stub Registry Settings](http://msdn.microsoft.com/en-us/library/ms531218%28EXCHG.10%29.aspx) to direct your application to use any implementation of MAPI, we recommend that you direct your application to use an implementation of MAPI that you have tested with.</span></span> <span data-ttu-id="3637b-110">Im folgenden werden beide Methoden explizit verknüpfen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3637b-110">The following describes both methods of linking explicitly.</span></span> 
  
## <a name="reading-from-the-registry"></a><span data-ttu-id="3637b-111">Lesen aus der Registrierung</span><span class="sxs-lookup"><span data-stu-id="3637b-111">Reading from the registry</span></span>

### <a name="to-read-mapi-implementation-information-from-the-registry"></a><span data-ttu-id="3637b-112">MAPI-Implementierungsinformationen aus der Registrierung lesen</span><span class="sxs-lookup"><span data-stu-id="3637b-112">To read MAPI implementation information from the registry</span></span>

1. <span data-ttu-id="3637b-113">Die Registrierungsschlüssel, die eine benutzerdefinierte DLL für e-Mail-Client angeben, befinden sich unter dem `HKLM\Software\Clients\Mail` -Schlüssel des e-Mail-Client.</span><span class="sxs-lookup"><span data-stu-id="3637b-113">The registry keys that indicate a custom DLL for a mail client are located under the  `HKLM\Software\Clients\Mail` key of the mail client.</span></span> 
    
   <span data-ttu-id="3637b-114">In der folgenden Tabelle werden diese Schlüssel beschrieben:</span><span class="sxs-lookup"><span data-stu-id="3637b-114">The following table describes these keys:</span></span>
    
   |<span data-ttu-id="3637b-115">**Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="3637b-115">**Key**</span></span>|<span data-ttu-id="3637b-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3637b-116">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="3637b-117">MSIComponentID</span><span class="sxs-lookup"><span data-stu-id="3637b-117">MSIComponentID</span></span>  <br/> |<span data-ttu-id="3637b-118">Ruft auf eine Windows Installer PublishComponent Kategorie-ID (GUID), die die DLL identifiziert, die simple MAPI-als auch die MAPI exportiert.</span><span class="sxs-lookup"><span data-stu-id="3637b-118">A Windows Installer PublishComponent category ID (GUID) that identifies the DLL that exports simple MAPI or MAPI calls.</span></span> <span data-ttu-id="3637b-119">Wenn dieser Schlüssel festlegen, Vorrang vor der **DLL-Pfad** oder **DLLPathEx** Schlüssel hat.</span><span class="sxs-lookup"><span data-stu-id="3637b-119">If set, this key takes precedence over the **DLLPath** or **DLLPathEx** key.</span></span>  <br/> |
   |<span data-ttu-id="3637b-120">MSIApplicationLCID</span><span class="sxs-lookup"><span data-stu-id="3637b-120">MSIApplicationLCID</span></span>  <br/> |<span data-ttu-id="3637b-121">Gebietsschema-ID (LCID) für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="3637b-121">Locale identifier (LCID) for your application.</span></span> <span data-ttu-id="3637b-122">Die erste Zeichenfolge Wert identifiziert einen Unterschlüssel aus `HKLM\Software` und nachfolgende Zeichenfolgenwerte identifizieren Registrierungswerte unter diesem Schlüssel, die Gebietsschemainformationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="3637b-122">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key that contain locale information.</span></span>  <br/> |
   |<span data-ttu-id="3637b-123">MSIOfficeLCID</span><span class="sxs-lookup"><span data-stu-id="3637b-123">MSIOfficeLCID</span></span>  <br/> |<span data-ttu-id="3637b-124">LCIDs für Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="3637b-124">LCIDs for Microsoft Office.</span></span> <span data-ttu-id="3637b-125">Die erste Zeichenfolge Wert identifiziert einen Unterschlüssel aus `HKLM\Software` und nachfolgende Zeichenfolgenwerte Registrierungswerte unter diesem Schlüssel zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="3637b-125">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key.</span></span>  <br/> |
   
   <span data-ttu-id="3637b-126">Rufen Sie die Informationen aus dieser Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="3637b-126">Obtain the information from these keys.</span></span>
    
2. <span data-ttu-id="3637b-127">Übergeben Sie die Werte, die Sie an die Funktion [FGetComponentPath](fgetcomponentpath.md) aus dem vorherigen Schritt abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3637b-127">Pass the values that you obtained from the previous step to the [FGetComponentPath](fgetcomponentpath.md) function.</span></span> <span data-ttu-id="3637b-128">**FGetComponentPath** ist eine Funktion, die durch die MAPI-Stub-Bibliothek Mapistub.dll exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="3637b-128">**FGetComponentPath** is a function that is exported by the MAPI stub library Mapistub.dll.</span></span> <span data-ttu-id="3637b-129">Es gibt den Pfad der benutzerdefinierten MAPI-Version.</span><span class="sxs-lookup"><span data-stu-id="3637b-129">It returns the path of the custom version of MAPI.</span></span> 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a><span data-ttu-id="3637b-130">Laden Sie die Implementierung der MAPI als Standard markiert</span><span class="sxs-lookup"><span data-stu-id="3637b-130">To load the implementation of MAPI marked as default</span></span>

1. <span data-ttu-id="3637b-131">Lesen der `HKLM\Software\Clients\Mail::(default)` Registrierungswert.</span><span class="sxs-lookup"><span data-stu-id="3637b-131">Read the  `HKLM\Software\Clients\Mail::(default)` registry value.</span></span> 
    
2. <span data-ttu-id="3637b-132">Die Informationen für den angegebenen Client Nachschlagen Sie wie oben beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3637b-132">Look up the information for the indicated client as described earlier.</span></span>
    
> [!NOTE]
> <span data-ttu-id="3637b-133">Beachten Sie, dass der Standard-Mailclient Extended MAPI nicht implementieren kann.</span><span class="sxs-lookup"><span data-stu-id="3637b-133">Note that the default mail client might not implement Extended MAPI.</span></span> 
  
#### <a name="example"></a><span data-ttu-id="3637b-134">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3637b-134">Example</span></span>

<span data-ttu-id="3637b-135">Um MAPI gemäß der Implementierung von Outlook zu laden, Nachschlagen der Registrierungsschlüssel unter `HKLM\Software\Clients\Mail\Microsoft Outlook` und an **FGetComponentPath**übergeben.</span><span class="sxs-lookup"><span data-stu-id="3637b-135">To load MAPI as implemented by Outlook, look up the registry keys under  `HKLM\Software\Clients\Mail\Microsoft Outlook` and pass them to **FGetComponentPath**.</span></span> <span data-ttu-id="3637b-136">**FGetComponentPath** gibt den Pfad für die Implementierung von Outlook MAPI-zurück.</span><span class="sxs-lookup"><span data-stu-id="3637b-136">**FGetComponentPath** will return the path for Outlook's implementation of MAPI.</span></span> 
  
<span data-ttu-id="3637b-137">Wenn der Schlüssel **MSIComponentID**, **MSIApplicationLCID**und **MSIOfficeLCID** nicht festgelegt sind, überprüfen Sie den Registrierungswert **DLLPathEx** .</span><span class="sxs-lookup"><span data-stu-id="3637b-137">If the keys **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID** are not set, check the **DLLPathEx** registry value.</span></span> <span data-ttu-id="3637b-138">Wenn der Schlüssel festgelegt sind, gibt **FGetComponentPath** den Pfad der Client-Implementierung von MAPI.</span><span class="sxs-lookup"><span data-stu-id="3637b-138">If the keys are set, **FGetComponentPath** gives the path of the client's implementation of MAPI.</span></span> 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a><span data-ttu-id="3637b-139">Implementieren des MAPI-Client-Lookup-Algorithmus</span><span class="sxs-lookup"><span data-stu-id="3637b-139">Implementing the MAPI Client Lookup algorithm</span></span>

<span data-ttu-id="3637b-140">Die folgende Tabelle enthält die vier Funktionen von MFCMAPI (engl.), die zum Nachschlagen von den Pfad für eine benutzerdefinierte Implementierung der MAPI verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="3637b-140">The following table lists the four functions from MFCMAPI that are used to look up the path for a custom implementation of MAPI:</span></span>
  
|<span data-ttu-id="3637b-141">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="3637b-141">**Function**</span></span>|<span data-ttu-id="3637b-142">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3637b-142">**Description**</span></span>|
|:-----|:-----|
| `GetMAPIPath` <br/> |<span data-ttu-id="3637b-143">Ruft den Pfad der MAPI-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="3637b-143">Gets the MAPI library path.</span></span>  <br/> |
| `GetMailKey` <br/> |<span data-ttu-id="3637b-144">Ruft den MAPI-Mail-Registrierungsschlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="3637b-144">Gets the MAPI mail registry key.</span></span>  <br/> |
| `GetMapiMsiIds` <br/> |<span data-ttu-id="3637b-145">Ruft die Windows Installer-ID ab.</span><span class="sxs-lookup"><span data-stu-id="3637b-145">Gets the Windows Installer identifier.</span></span>  <br/> |
| `GetComponentPath` <br/> |<span data-ttu-id="3637b-146">Ruft den Komponentenpfad [FGetComponentPath](fgetcomponentpath.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="3637b-146">Gets the component path using [FGetComponentPath](fgetcomponentpath.md).</span></span>  <br/> |
   
<span data-ttu-id="3637b-147">Da MFCMAPI (engl.) die standardmäßige Implementierung von MAPI standardmäßig geladen wird, wenn Sie eine andere Implementierung von MAPI verwenden möchten, müssen Sie dies explizit anweisen.</span><span class="sxs-lookup"><span data-stu-id="3637b-147">Because MFCMAPI loads the default implementation of MAPI by default, if you want to use a different implementation of MAPI, you must explicitly direct it to do so.</span></span> <span data-ttu-id="3637b-148">Dies erfolgt mithilfe der **Session\Load MAPI** -Routine.</span><span class="sxs-lookup"><span data-stu-id="3637b-148">This is performed by using the **Session\Load MAPI** routine.</span></span> 
  
### <a name="how-these-functions-work"></a><span data-ttu-id="3637b-149">Wie funktionieren diese Funktionen</span><span class="sxs-lookup"><span data-stu-id="3637b-149">How these functions work</span></span>

1. <span data-ttu-id="3637b-150">MFCMAPI (engl.) Anrufe `GetMAPIPath`, das Übergeben von NULL für den Clientparameter, um die standardmäßige MAPI-Implementierung zu laden.</span><span class="sxs-lookup"><span data-stu-id="3637b-150">MFCMAPI calls  `GetMAPIPath`, passing NULL for the client parameter, to load the default MAPI implementation.</span></span>
    
2.  <span data-ttu-id="3637b-151">`GetMAPIPath`Anrufe `GetMapiMsiIds` zum Lesen der Werte für **MSIComponentID**, **MSIApplicationLCID**und **MSIOfficeLCID**.</span><span class="sxs-lookup"><span data-stu-id="3637b-151">`GetMAPIPath` calls  `GetMapiMsiIds` to read the values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
3.  <span data-ttu-id="3637b-152">`GetMapiMsiIds`Anrufe `GetMailKey` auf den Registrierungsschlüssel für den Standard-Mail-Client zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3637b-152">`GetMapiMsiIds` calls  `GetMailKey` to open the registry key for the default mail client.</span></span> 
    
4.  <span data-ttu-id="3637b-153">`GetMapiMsiIds`verwendet das Registrierung Handle zurückgegebene `GetMailKey` zum Nachschlagen von Werten für **MSIComponentID**, **MSIApplicationLCID**und **MSIOfficeLCID**.</span><span class="sxs-lookup"><span data-stu-id="3637b-153">`GetMapiMsiIds` uses the registry handle returned by  `GetMailKey` to look up values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
5. <span data-ttu-id="3637b-154">Die Werte für **MSIComponentID**, **MSIApplicationLCID**und **MSIOfficeLCID**, kehren zum `GetMAPIPath`.</span><span class="sxs-lookup"><span data-stu-id="3637b-154">The values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**, are returned to  `GetMAPIPath`.</span></span>  <span data-ttu-id="3637b-155">`GetMAPIPath`Anschließend übergibt sie an `GetComponentPath`.</span><span class="sxs-lookup"><span data-stu-id="3637b-155">`GetMAPIPath` then passes them to  `GetComponentPath`.</span></span>
    
6.  <span data-ttu-id="3637b-156">`GetComponentPath`Lädt die MAPI-Stub-Bibliothek Mapi32.dll, aus dem Verzeichnis des Systems.</span><span class="sxs-lookup"><span data-stu-id="3637b-156">`GetComponentPath` loads the MAPI stub library, Mapi32.dll, from the system directory.</span></span> 
    
7.  <span data-ttu-id="3637b-157">`GetComponentPath`die Adresse der **FGetComponentPath** -Funktion von Mapi32.dll, vorausgesetzt, dass Mapi32.dll **FGetComponentPath**exportiert wird abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3637b-157">`GetComponentPath` then retrieves the address of the **FGetComponentPath** function from Mapi32.dll, assuming that Mapi32.dll exports **FGetComponentPath**.</span></span>
    
8. <span data-ttu-id="3637b-158">Wenn die Adresse des **FGetComponentPath** von Mapi32.dll fehlschlägt, erste `GetComponentPath` die Adresse aus Mapistub.dll abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3637b-158">If getting the address of **FGetComponentPath** from Mapi32.dll fails,  `GetComponentPath` retrieves the address from Mapistub.dll.</span></span> 
    
9.  <span data-ttu-id="3637b-159">`GetComponentPath`Ruft dann **FGetComponentPath**, um den Pfad des die Standardversion des MAPI.</span><span class="sxs-lookup"><span data-stu-id="3637b-159">`GetComponentPath` then calls **FGetComponentPath**, obtaining the path of the default version of MAPI.</span></span>
    
10.  <span data-ttu-id="3637b-160">`GetMAPIPath`Klicken Sie dann gibt dieser Pfad an den Anrufer, die anschließend geladen MAPI und explizit darauf verknüpft, wie in [Verbindung zu MAPI-Funktionen](how-to-link-to-mapi-functions.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3637b-160">`GetMAPIPath` then returns this path to the caller, which then loads MAPI and explicitly links to it as described in [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="3637b-161">Zur Unterstützung von lokalisierter Kopien der MAPI für Englisch und nicht-englischen Gebietsschemas `GetMAPIPath` liest die Werte für die Unterschlüssel **MSIApplicationLCID** und **MSIOfficeLCID** .</span><span class="sxs-lookup"><span data-stu-id="3637b-161">To support localized copies of MAPI for English and non-English locales,  `GetMAPIPath` reads the values for the **MSIApplicationLCID** and **MSIOfficeLCID** subkeys.</span></span>  <span data-ttu-id="3637b-162">`GetMAPIPath`Ruft dann **FGetComponentPath**, zuerst **MSIApplicationLCID** als **SzQualifier**angeben und erneut **MSIOfficeLCID** als **SzQualifier**angeben.</span><span class="sxs-lookup"><span data-stu-id="3637b-162">`GetMAPIPath` then calls **FGetComponentPath**, first specifying **MSIApplicationLCID** as **szQualifier**, and again specifying **MSIOfficeLCID** as **szQualifier**.</span></span> <span data-ttu-id="3637b-163">Weitere Informationen zu Registrierungsschlüsseln für e-Mail-Clients, die nicht-englischen Sprachen unterstützen, finden Sie unter [Einstellung der MSI-Schlüssel für Ihr MAPI-DLL](http://msdn.microsoft.com/en-us/library/ee909494%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="3637b-163">For more information about registry keys for mail clients that support non-English languages, see [Setting Up the MSI Keys for Your MAPI DLL](http://msdn.microsoft.com/en-us/library/ee909494%28VS.85%29.aspx).</span></span>   
> - <span data-ttu-id="3637b-164">Wenn keine MFCMAPI (engl.) einen Pfad für die Verwendung von MAPI empfängt `GetMAPIPath`, es lädt die MAPI-Stub-Bibliothek aus dem Verzeichnis des Systems.</span><span class="sxs-lookup"><span data-stu-id="3637b-164">If MFCMAPI does not receive a path for MAPI using  `GetMAPIPath`, it loads the MAPI stub library from the system directory.</span></span>
> - <span data-ttu-id="3637b-165">Der **MSMapiApps** Registrierungswert in [Explizit Zuordnen von MAPI-Aufrufe zu MAPI-DLLs](http://msdn.microsoft.com/en-us/library/ee909490%28VS.85%29.aspx) erläuterten gilt nur, wenn die MAPI-Stub-Bibliothek verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3637b-165">The **MSMapiApps** registry value discussed in [Explicitly Mapping MAPI Calls to MAPI DLLs](http://msdn.microsoft.com/en-us/library/ee909490%28VS.85%29.aspx) only applies when the MAPI Stub library is used.</span></span> <span data-ttu-id="3637b-166">Anwendungen, die eine bestimmte Implementierung der MAPI laden oder laden die standardmäßige Implementierung müssen nicht den **MSMapiApps** Registrierungsschlüssel festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3637b-166">Applications that load a specific implementation of MAPI or load the default implementation do not have to set the **MSMapiApps** registry key.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="3637b-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3637b-167">See also</span></span>

- [<span data-ttu-id="3637b-168">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="3637b-168">FGetComponentPath</span></span>](fgetcomponentpath.md)
- [<span data-ttu-id="3637b-169">�bersicht �ber die MAPI-Programmierung</span><span class="sxs-lookup"><span data-stu-id="3637b-169">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="3637b-170">Verweisen auf MAPI-Funktionen</span><span class="sxs-lookup"><span data-stu-id="3637b-170">Link to MAPI Functions</span></span>](how-to-link-to-mapi-functions.md)
- [<span data-ttu-id="3637b-171">Mapi32.dll Stub Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="3637b-171">Mapi32.dll Stub Registry Settings</span></span>](http://msdn.microsoft.com/en-us/library/ms531218%28EXCHG.10%29.aspx)
- [<span data-ttu-id="3637b-172">Einrichten der MSI-Keys für die MAPI-DLL</span><span class="sxs-lookup"><span data-stu-id="3637b-172">Setting Up the MSI Keys for Your MAPI DLL</span></span>](http://msdn.microsoft.com/en-us/library/ee909494%28VS.85%29.aspx)
- [<span data-ttu-id="3637b-173">Zuordnen von explizit MAPI-Aufrufe zu MAPI-DLLs</span><span class="sxs-lookup"><span data-stu-id="3637b-173">Explicitly Mapping MAPI Calls to MAPI DLLs</span></span>](http://msdn.microsoft.com/en-us/library/ee909490%28VS.85%29.aspx)

