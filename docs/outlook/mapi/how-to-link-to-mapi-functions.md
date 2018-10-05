---
title: Link zu MAPI-Funktionen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be72a893-a3bc-4dea-8234-47f3e1db4515
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 71108da8bb9914bb7ed0ad0b3adacc24e1d69e63
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400145"
---
# <a name="link-to-mapi-functions"></a><span data-ttu-id="8bb99-103">Link zu MAPI-Funktionen</span><span class="sxs-lookup"><span data-stu-id="8bb99-103">Link to MAPI functions</span></span>

<span data-ttu-id="8bb99-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8bb99-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8bb99-105">Es gibt drei Methoden verknüpfen: implizite Verknüpfung, explizite Verknüpfung und die MAPI-Stub-Bibliothek mit neuen Hybridmodell bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="8bb99-105">There are three methods of linking: implicit linking, explicit linking, and a new hybrid model using the MAPI Stub Library.</span></span>
  
## <a name="implicit-linking"></a><span data-ttu-id="8bb99-106">Implizite Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="8bb99-106">Implicit linking</span></span>

<span data-ttu-id="8bb99-107">In der Vergangenheit beteiligt Aufrufen von MAPI-Funktionen in einer e-Mail-Anwendung immer auf die Objektbibliothek Mapi32.lib verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="8bb99-107">Historically, calling MAPI functions in a messaging application always involved linking to the Mapi32.lib library.</span></span> <span data-ttu-id="8bb99-108">Diese enthalten, MAPI-Anrufe an die die Windows-MAPI-Stub-Bibliothek "Mapi32.dll", die die Anrufe an die Implementierung der standardmäßigen MAPI-Client zur Laufzeit dann weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="8bb99-108">This included routing MAPI calls to the Windows MAPI stub library, Mapi32.dll, which then forwarded the calls to the default MAPI client implementation at run time.</span></span> <span data-ttu-id="8bb99-109">Dieser Prozess der Anruf wird als implizite Verknüpfung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8bb99-109">This call process is known as implicit linking.</span></span> <span data-ttu-id="8bb99-110">Links in der folgenden Abbildung zeigt ein Beispiel für implizite Verknüpfung in einem MAPI-Funktion Anruf Prozess verwendet.</span><span class="sxs-lookup"><span data-stu-id="8bb99-110">The left side of the following figure shows an example of implicit linking used in a MAPI function call process.</span></span> <span data-ttu-id="8bb99-111">Der Prozess wird durch eine MAPI-Anwendung initiiert und umfasst die MAPI-Bibliothek (Mapi32.lib) und den Windows-MAPI-Stub (Mapi32.dll) und abgeschlossen ist, indem Sie die Outlook-MAPI-Client-Implementierung der MAPI-Stub (Msmapi32.dll).</span><span class="sxs-lookup"><span data-stu-id="8bb99-111">The process is initiated by a MAPI application and involves the MAPI library (Mapi32.lib) and the Windows MAPI stub (Mapi32.dll) and is completed by the Outlook MAPI client implementation of the MAPI stub (Msmapi32.dll).</span></span>
  
<span data-ttu-id="8bb99-112">**Vergleich von impliziter und expliziter links.**</span><span class="sxs-lookup"><span data-stu-id="8bb99-112">**Comparison of implicit and explicit linking.**</span></span>

<span data-ttu-id="8bb99-113">![Vergleich von impliziter und expliziter links] (media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Vergleich von impliziter und expliziter links")</span><span class="sxs-lookup"><span data-stu-id="8bb99-113">![Comparison of implicit and explicit linking](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparison of implicit and explicit linking")</span></span>
  
## <a name="explicit-linking"></a><span data-ttu-id="8bb99-114">Explizites verknüpfen</span><span class="sxs-lookup"><span data-stu-id="8bb99-114">Explicit linking</span></span>

<span data-ttu-id="8bb99-115">Da der Standard-MAPI-Client Installation bei Bedarf mithilfe von Windows Installer (MSI) unterstützt, können Sie direkt auf die Outlook-MAPI-Stub statt der MAPI-Bibliothek und Windows MAPI-Stub Messaginganwendungen entwickeln.</span><span class="sxs-lookup"><span data-stu-id="8bb99-115">Because the default MAPI client supports on-demand installation using the Windows Installer (MSI), you can develop messaging applications directly on the Outlook MAPI stub instead of using the MAPI library and Windows MAPI stub.</span></span> <span data-ttu-id="8bb99-116">Im rechten Teil der vorherigen Abbildung zeigt ein Beispiel für einen MAPI-Funktion Anruf-Prozess, beginnend mit einem MAPI-Anwendung für den Pfad und Namen der DLL-Datei für den Outlook-MAPI-Stub (Schritt 2 im folgenden Abschnitt) suchen und tätigen von Anrufen in der Outlook-MAPI-Stub (Funktion Schritt 3 im folgenden Abschnitt).</span><span class="sxs-lookup"><span data-stu-id="8bb99-116">The right side of the previous figure shows an example of a MAPI function call process, starting with a MAPI application looking for the path and DLL name for the Outlook MAPI stub (step 2 in the following section), and making function calls into the Outlook MAPI stub (step 3 in the following section).</span></span> <span data-ttu-id="8bb99-117">Das folgende Verfahren zeigt, wie MAPI-Funktionen aufrufen, mithilfe von expliziten verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="8bb99-117">The following procedure shows how to call MAPI functions by using explicit linking.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8bb99-118">Diese Informationen zum Verknüpfen von expliziten möglicherweise überflüssig auf Ihre Bedürfnisse mit der Einführung von der MAPIStubLibrary.lib im folgenden Abschnitt erläutert.</span><span class="sxs-lookup"><span data-stu-id="8bb99-118">This information about explicit linking may be superfluous to your needs with the introduction of the MAPIStubLibrary.lib discussed in the following section.</span></span> <span data-ttu-id="8bb99-119">Wie die implizite Modell der neue Bibliothek alles verwaltet und implementiert die explizite verknüpfende Logik, die von Outlook lädt MAPI direkt.</span><span class="sxs-lookup"><span data-stu-id="8bb99-119">Like the implicit model, the new library manages everything and implements the explicit linking logic that loads Outlook's MAPI directly.</span></span> 
  
<span data-ttu-id="8bb99-120">Weitere Informationen zum expliziten Verknüpfen finden Sie unter explizit verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="8bb99-120">For more information about explicit linking, see Linking Explicitly.</span></span>
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a><span data-ttu-id="8bb99-121">MAPI-API-Elemente ohne die MAPI-Bibliothek und den Windows-MAPI-Stub aufrufen</span><span class="sxs-lookup"><span data-stu-id="8bb99-121">To call MAPI API elements without the MAPI library and the Windows MAPI stub</span></span>

1. <span data-ttu-id="8bb99-122">Erstellen Sie in der Programmdatei eine globale Liste Funktionszeiger für die einzelnen MAPI-API-Elemente, die Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="8bb99-122">In your program file, create a global list of function pointers for each MAPI API element that you are using.</span></span> 
    
   <span data-ttu-id="8bb99-123">Das folgende Beispiel zeigt diesen Schritt.</span><span class="sxs-lookup"><span data-stu-id="8bb99-123">The following example shows this step.</span></span>
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. <span data-ttu-id="8bb99-124">Erstellen Sie eine Funktion, die MAPI-Funktionen zum Verknüpfen der MAPI-DLL des Standard-MAPI-Client (beispielsweise Msmapi32.dll von Microsoft Outlook) initialisiert.</span><span class="sxs-lookup"><span data-stu-id="8bb99-124">Create a function that initializes MAPI functions to link to the MAPI DLL of the default MAPI client (for example, Msmapi32.dll of Microsoft Outlook).</span></span> <span data-ttu-id="8bb99-125">Folgendermaßen Sie in dieser Funktion vor:</span><span class="sxs-lookup"><span data-stu-id="8bb99-125">In this function, do the following:</span></span> 
    
    1. <span data-ttu-id="8bb99-126">Laden Sie mapi32.dll aus dem entsprechenden Systemverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="8bb99-126">Load mapi32.dll from the appropriate system directory.</span></span> 
        
       |||
       |:-----|:-----|
       |<span data-ttu-id="8bb99-127">X64 oder X86 systemintern</span><span class="sxs-lookup"><span data-stu-id="8bb99-127">x64 or x86 natively</span></span>  <br/> |<span data-ttu-id="8bb99-128">**%windir%\system32\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="8bb99-128">**%windir%\system32\mapi32.dll**</span></span> <br/> |
       |<span data-ttu-id="8bb99-129">X86 auf WoW-Modus</span><span class="sxs-lookup"><span data-stu-id="8bb99-129">x86 on WoW mode</span></span>  <br/> |<span data-ttu-id="8bb99-130">**%windir%\syswow64\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="8bb99-130">**%windir%\syswow64\mapi32.dll**</span></span> <br/> |
    
    2. <span data-ttu-id="8bb99-131">Rufen Sie die [FGetComponentPath](fgetcomponentpath.md) -Funktion, wenn Sie den Pfad und Name-DLL, die MAPI-Subsystems implementiert erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="8bb99-131">Call the [FGetComponentPath](fgetcomponentpath.md) function to get the path and DLL name that implements the MAPI subsystem.</span></span> <span data-ttu-id="8bb99-132">Weitere Informationen finden Sie unter [Wählen Sie eine bestimmte Version von MAPI zu laden](how-to-choose-a-specific-version-of-mapi-to-load.md).</span><span class="sxs-lookup"><span data-stu-id="8bb99-132">For more information, see [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span>
        
    3. <span data-ttu-id="8bb99-133">Laden der DLL-Datei durch Aufrufen der LoadLibrary-Funktion.</span><span class="sxs-lookup"><span data-stu-id="8bb99-133">Load the DLL by calling the LoadLibrary function.</span></span> 
        
    4. <span data-ttu-id="8bb99-134">Initialisieren Sie das MAPI-Funktion Zeiger Array durch Aufrufen der GetProcAddress-Funktion.</span><span class="sxs-lookup"><span data-stu-id="8bb99-134">Initialize the MAPI function pointer array by calling the GetProcAddress function.</span></span> 
        
    <span data-ttu-id="8bb99-135">Das folgende Beispiel zeigt die vorherigen Schritte:</span><span class="sxs-lookup"><span data-stu-id="8bb99-135">The following example shows the previous steps:</span></span>
        
   ```cpp
    void InitializeMapiFunctions()
    {
    {
        // Get the DLL path and name of the actual MAPI implementation.
        FGetComponentPath(g_szMapiComponentGUID, NULL, szMAPIDLL, MAX_PATH);
        // Load the DLL.
        hMod = LoadLibrary(szMAPIDLL);
        // Initialize MAPI functions.
        pfnMAPIInitialize = GetProcAddress(hMod, "MAPIInitialize");
        pfnMAPIUninitialize = GetProcAddress(hMod, "MAPIUninitialize");
    }
   ```

3. <span data-ttu-id="8bb99-136">Rufen Sie anschließend die Funktion, die Sie in Schritt 2 in Ihrer messaging-Anwendung erstellten, bevor Sie MAPI-API-Elemente aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8bb99-136">Finally, call the function that you created in step 2 in your messaging application before you make calls to MAPI API elements.</span></span> 
    
   > [!CAUTION]
   > <span data-ttu-id="8bb99-137">Sie müssen die MAPI-Subsystems Aufhebung der Initialisierung der vor dem Schließen der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="8bb99-137">You must uninitialize the MAPI subsystem before closing your application.</span></span> 
  
   <span data-ttu-id="8bb99-138">Das folgende Beispiel zeigt diesen Schritt:</span><span class="sxs-lookup"><span data-stu-id="8bb99-138">The following example shows this step:</span></span> 
    
   ```cpp
    int main()
    {
        HRESULT hr;
        InitializeMapiFunctions();
        // Initialize the MAPI subsystem.
        hr = (*pfnMAPIInitialize)(NULL);
        if (hr!= S_OK)
        {
            // Handle the error case.
        }
        // Here is where you make calls to other MAPI interfaces.
        // Uninitialize the MAPI subsystem.
        (*pfnMAPIUninitialize)();
    return (0);
    }
   ```

## <a name="mapistublibrarylib"></a><span data-ttu-id="8bb99-139">MAPIStubLibrary.lib</span><span class="sxs-lookup"><span data-stu-id="8bb99-139">MAPIStubLibrary.lib</span></span>

<span data-ttu-id="8bb99-140">Die Einführung von Microsoft Outlook 2010 und 64-Bit-MAPI, jetzt Erweitern der Microsoft Outlook 2013, erfordert mehr als die herkömmliche 32-Bit-API für eine vollständige Implementierung.</span><span class="sxs-lookup"><span data-stu-id="8bb99-140">The advent of Microsoft Outlook 2010 and 64-bit MAPI, now extending to the Microsoft Outlook 2013, requires more than the traditional 32-bit API for full implementation.</span></span> <span data-ttu-id="8bb99-141">Ein neues Projekt die MAPI-Stub-Bibliothek veröffentlicht, auf der CodePlex-Website enthält Technik Ersatz für Mapi32.lib, die Erstellung von 32-Bit- und 64-Bit-MAPI-Anwendungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8bb99-141">A new project, the MAPI Stub Library, posted on the CodePlex website provides a drop-in replacement for Mapi32.lib that supports building both 32-bit and 64-bit MAPI applications.</span></span> <span data-ttu-id="8bb99-142">MAPIStubLibrary.lib entfällt die Notwendigkeit zum expliziten MAPI verknüpfen und erstellt es, können Sie Mapi32.lib aus entfernen Einstelllungen Linker durch MAPIStubLibrary.lib ersetzen; keine weiteren Änderungen an Ihrem Code sollte erforderlich sein.</span><span class="sxs-lookup"><span data-stu-id="8bb99-142">MAPIStubLibrary.lib eliminates the need to explicitly link to MAPI, and having built it, you can remove Mapi32.lib from your linker settings, replacing it with MAPIStubLibrary.lib; no further modifications to your code should be needed.</span></span> <span data-ttu-id="8bb99-143">Er überflüssig auch das Schreiben **LoadLibrary**und **GetProcAddress** **FreeLibrary** Code zum Behandeln von neuere Exporte enthalten in dieser Bibliotheksdatei jedoch nicht im Mapi32.lib, die erforderlich wäre, wenn Sie explizite Verknüpfung verwendet.</span><span class="sxs-lookup"><span data-stu-id="8bb99-143">It also eliminates the need to write **LoadLibrary**, **GetProcAddress**, and **FreeLibrary** code to handle newer exports included in this library file but not in Mapi32.lib, which would be needed if you used explicit linking.</span></span> 
  
<span data-ttu-id="8bb99-144">Einige der neuen Funktionen aus dieser Bibliothek verknüpft, die in Mapi32.lib nicht verfügbar sind die folgenden:</span><span class="sxs-lookup"><span data-stu-id="8bb99-144">Some of the new functions linked from this library that are not available in Mapi32.lib include the following:</span></span>
  
- [<span data-ttu-id="8bb99-145">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="8bb99-145">GetDefCachedMode</span></span>](getdefcachedmode.md)    
- [<span data-ttu-id="8bb99-146">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="8bb99-146">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)   
- [<span data-ttu-id="8bb99-147">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="8bb99-147">HrOpenOfflineObj</span></span>](hropenofflineobj.md)    
- [<span data-ttu-id="8bb99-148">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="8bb99-148">MAPICrashRecovery</span></span>](mapicrashrecovery.md)   
- [<span data-ttu-id="8bb99-149">OpenStreamOnFileW</span><span class="sxs-lookup"><span data-stu-id="8bb99-149">OpenStreamOnFileW</span></span>](openstreamonfilew.md)    
- [<span data-ttu-id="8bb99-150">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="8bb99-150">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)
    
<span data-ttu-id="8bb99-151">Einbinden der MAPI-Stub-Bibliothek eine alternative Methode ist die Quelldateien, MapiStubLibrary.cpp und StubUtils.cpp, direkt in Ihr Projekt kopieren und entfernen jegliche Verknüpfung zu Mapi32.lib und Code, der explizit MAPI verknüpft.</span><span class="sxs-lookup"><span data-stu-id="8bb99-151">An alternate method of incorporating the MAPI Stub Library is to copy the source files, MapiStubLibrary.cpp and StubUtils.cpp, directly into your project and remove any linkage to Mapi32.lib and any code that explicitly links to MAPI.</span></span>
  
<span data-ttu-id="8bb99-152">MAPI-Stub-Bibliothek Computerdateien und Informationen zum Erstellen und integrieren sie in Ihrem Projekt als auch Fragen zu dieser Bibliothek wie wann und warum verwenden, finden Sie unter der [MAPI-Stub-Bibliothek](https://mapistublibrary.codeplex.com/documentation) auf der CodePlex-Website.</span><span class="sxs-lookup"><span data-stu-id="8bb99-152">To access the MAPI Stub Library files and for information about how to build and integrate it into your project, as well as questions about this library such as when and why to use it, see the [MAPI Stub Library](https://mapistublibrary.codeplex.com/documentation) on the CodePlex site.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8bb99-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8bb99-153">See also</span></span>

- [<span data-ttu-id="8bb99-154">Übersicht über die MAPI-Programmierung</span><span class="sxs-lookup"><span data-stu-id="8bb99-154">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="8bb99-155">Installieren des MAPI-Subsystems</span><span class="sxs-lookup"><span data-stu-id="8bb99-155">Installing the MAPI Subsystem</span></span>](installing-the-mapi-subsystem.md)
- [<span data-ttu-id="8bb99-156">Installieren der MAPI-Headerdateien</span><span class="sxs-lookup"><span data-stu-id="8bb99-156">Install MAPI Header Files</span></span>](how-to-install-mapi-header-files.md)
- [<span data-ttu-id="8bb99-157">Auswählen einer bestimmten zu ladenden MAPI-Version</span><span class="sxs-lookup"><span data-stu-id="8bb99-157">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [<span data-ttu-id="8bb99-158">Bestimmen der zu verwendenden verknüpfen Methode</span><span class="sxs-lookup"><span data-stu-id="8bb99-158">Determining Which Linking Method to Use</span></span>](https://msdn.microsoft.com/library/253b8k2c.aspx)
- [<span data-ttu-id="8bb99-159">Verknüpfen einer ausführbaren Datei mit einer DLL</span><span class="sxs-lookup"><span data-stu-id="8bb99-159">Linking an Executable to a DLL</span></span>](https://msdn.microsoft.com/library/9yd93633.aspx)
- [<span data-ttu-id="8bb99-160">Einrichten der MSI-Keys für die MAPI-DLL</span><span class="sxs-lookup"><span data-stu-id="8bb99-160">Setting Up the MSI Keys for Your MAPI DLL</span></span>](https://msdn.microsoft.com/library/ee909494%28v=VS.85%29.aspx)

