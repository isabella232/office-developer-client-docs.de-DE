---
title: Verweisen auf MAPI-Funktionen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be72a893-a3bc-4dea-8234-47f3e1db4515
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 71108da8bb9914bb7ed0ad0b3adacc24e1d69e63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346883"
---
# <a name="link-to-mapi-functions"></a><span data-ttu-id="972f0-103">Verweisen auf MAPI-Funktionen</span><span class="sxs-lookup"><span data-stu-id="972f0-103">Link to MAPI functions</span></span>

<span data-ttu-id="972f0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="972f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="972f0-105">Es gibt drei Methoden der Verknüpfung: implizites verknüpfen, explizites verknüpfen und ein neues Hybridmodell mithilfe der MAPI-Stub-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="972f0-105">There are three methods of linking: implicit linking, explicit linking, and a new hybrid model using the MAPI Stub Library.</span></span>
  
## <a name="implicit-linking"></a><span data-ttu-id="972f0-106">Implizite Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="972f0-106">Implicit linking</span></span>

<span data-ttu-id="972f0-107">Historisch gesehen war das Aufrufen von MAPI-Funktionen in einer Messaginganwendung immer mit der Verknüpfung mit der Bibliothek Mapi32. lib verbunden.</span><span class="sxs-lookup"><span data-stu-id="972f0-107">Historically, calling MAPI functions in a messaging application always involved linking to the Mapi32.lib library.</span></span> <span data-ttu-id="972f0-108">Dies umfasste das Weiterleiten von MAPI-Aufrufen an die Windows MAPI-Stub-Bibliothek, Mapi32. dll, die die Aufrufe dann zur Laufzeit an die standardmäßige MAPI-Clientimplementierung weitergeleitet hat.</span><span class="sxs-lookup"><span data-stu-id="972f0-108">This included routing MAPI calls to the Windows MAPI stub library, Mapi32.dll, which then forwarded the calls to the default MAPI client implementation at run time.</span></span> <span data-ttu-id="972f0-109">Dieser Aufrufprozess wird als implizite Verknüpfung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="972f0-109">This call process is known as implicit linking.</span></span> <span data-ttu-id="972f0-110">Die linke Seite der folgenden Abbildung zeigt ein Beispiel für die implizite Verknüpfung, die in einem MAPI-Funktionsaufruf Prozess verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="972f0-110">The left side of the following figure shows an example of implicit linking used in a MAPI function call process.</span></span> <span data-ttu-id="972f0-111">Der Prozess wird von einer MAPI-Anwendung initiiert und umfasst die MAPI-Bibliothek (Mapi32. lib) und den Windows-MAPI-Stub (Mapi32. dll) und wird durch die Outlook-MAPI-Clientimplementierung des MAPI-Stub (msmapi32. dll) abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="972f0-111">The process is initiated by a MAPI application and involves the MAPI library (Mapi32.lib) and the Windows MAPI stub (Mapi32.dll) and is completed by the Outlook MAPI client implementation of the MAPI stub (Msmapi32.dll).</span></span>
  
<span data-ttu-id="972f0-112">**Vergleich zwischen impliziter und expliziter Verknüpfung.**</span><span class="sxs-lookup"><span data-stu-id="972f0-112">**Comparison of implicit and explicit linking.**</span></span>

<span data-ttu-id="972f0-113">![Vergleich zwischen impliziter und expliziter Verknüpfung] (media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Vergleich zwischen impliziter und expliziter Verknüpfung")</span><span class="sxs-lookup"><span data-stu-id="972f0-113">![Comparison of implicit and explicit linking](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparison of implicit and explicit linking")</span></span>
  
## <a name="explicit-linking"></a><span data-ttu-id="972f0-114">Explizite Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="972f0-114">Explicit linking</span></span>

<span data-ttu-id="972f0-115">Da der MAPI-Standard Client die bedarfsgesteuerte Installation mithilfe von Windows Installer (MSI) unterstützt, können Sie Messaginganwendungen direkt im Outlook-MAPI-Stub entwickeln, anstatt die MAPI-Bibliothek und Windows MAPI-Stub zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="972f0-115">Because the default MAPI client supports on-demand installation using the Windows Installer (MSI), you can develop messaging applications directly on the Outlook MAPI stub instead of using the MAPI library and Windows MAPI stub.</span></span> <span data-ttu-id="972f0-116">Die Rechte Seite der vorherigen Abbildung zeigt ein Beispiel für einen MAPI-Funktionsaufruf Prozess, beginnend mit einer MAPI-Anwendung, die nach dem Pfad und dem DLL-Namen für den Outlook-MAPI-Stub sucht (Schritt 2 im folgenden Abschnitt) und durch Ausführen von Funktionsaufrufen in den Outlook-MAPI-Stub ( Schritt 3 im folgenden Abschnitt).</span><span class="sxs-lookup"><span data-stu-id="972f0-116">The right side of the previous figure shows an example of a MAPI function call process, starting with a MAPI application looking for the path and DLL name for the Outlook MAPI stub (step 2 in the following section), and making function calls into the Outlook MAPI stub (step 3 in the following section).</span></span> <span data-ttu-id="972f0-117">Im folgenden Verfahren wird gezeigt, wie MAPI-Funktionen mithilfe der expliziten Verknüpfung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="972f0-117">The following procedure shows how to call MAPI functions by using explicit linking.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="972f0-118">Diese Informationen zur expliziten Verknüpfung sind möglicherweise für Ihre Anforderungen mit der im folgenden Abschnitt erläuterten Einführung der MAPIStubLibrary. lib überflüssig.</span><span class="sxs-lookup"><span data-stu-id="972f0-118">This information about explicit linking may be superfluous to your needs with the introduction of the MAPIStubLibrary.lib discussed in the following section.</span></span> <span data-ttu-id="972f0-119">Wie das implizite Modell wird in der neuen Bibliothek alles verwaltet und die explizite Verknüpfungslogik implementiert, die die MAPI von Outlook direkt lädt.</span><span class="sxs-lookup"><span data-stu-id="972f0-119">Like the implicit model, the new library manages everything and implements the explicit linking logic that loads Outlook's MAPI directly.</span></span> 
  
<span data-ttu-id="972f0-120">Weitere Informationen zur expliziten Verknüpfung finden Sie unter explizites verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="972f0-120">For more information about explicit linking, see Linking Explicitly.</span></span>
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a><span data-ttu-id="972f0-121">So rufen Sie MAPI-API-Elemente ohne die MAPI-Bibliothek und den Windows-MAPI-Stub auf</span><span class="sxs-lookup"><span data-stu-id="972f0-121">To call MAPI API elements without the MAPI library and the Windows MAPI stub</span></span>

1. <span data-ttu-id="972f0-122">Erstellen Sie in Ihrer Programmdatei eine globale Liste von Funktionszeigern für jedes MAPI-API-Element, das Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="972f0-122">In your program file, create a global list of function pointers for each MAPI API element that you are using.</span></span> 
    
   <span data-ttu-id="972f0-123">Im folgenden Beispiel wird dieser Schritt veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="972f0-123">The following example shows this step.</span></span>
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. <span data-ttu-id="972f0-124">Erstellen Sie eine Funktion, die MAPI-Funktionen initialisiert, um eine Verknüpfung mit der MAPI-DLL des standardmäßigen MAPI-Clients herzustellen (beispielsweise msmapi32. dll von Microsoft Outlook).</span><span class="sxs-lookup"><span data-stu-id="972f0-124">Create a function that initializes MAPI functions to link to the MAPI DLL of the default MAPI client (for example, Msmapi32.dll of Microsoft Outlook).</span></span> <span data-ttu-id="972f0-125">Führen Sie in dieser Funktion folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="972f0-125">In this function, do the following:</span></span> 
    
    1. <span data-ttu-id="972f0-126">Laden Sie Mapi32. dll aus dem entsprechenden Systemverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="972f0-126">Load mapi32.dll from the appropriate system directory.</span></span> 
        
       |||
       |:-----|:-----|
       |<span data-ttu-id="972f0-127">x64 oder x86 nativ</span><span class="sxs-lookup"><span data-stu-id="972f0-127">x64 or x86 natively</span></span>  <br/> |<span data-ttu-id="972f0-128">**%windir%\system32\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="972f0-128">**%windir%\system32\mapi32.dll**</span></span> <br/> |
       |<span data-ttu-id="972f0-129">x86 im WOW-Modus</span><span class="sxs-lookup"><span data-stu-id="972f0-129">x86 on WoW mode</span></span>  <br/> |<span data-ttu-id="972f0-130">**%windir%\syswow64\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="972f0-130">**%windir%\syswow64\mapi32.dll**</span></span> <br/> |
    
    2. <span data-ttu-id="972f0-131">Rufen Sie die [FGetComponentPath](fgetcomponentpath.md) -Funktion auf, um den Pfad und den DLL-Namen abzurufen, der das MAPI-Subsystem implementiert.</span><span class="sxs-lookup"><span data-stu-id="972f0-131">Call the [FGetComponentPath](fgetcomponentpath.md) function to get the path and DLL name that implements the MAPI subsystem.</span></span> <span data-ttu-id="972f0-132">Weitere Informationen finden Sie unter [Choose a specific Version of MAPI to laden](how-to-choose-a-specific-version-of-mapi-to-load.md).</span><span class="sxs-lookup"><span data-stu-id="972f0-132">For more information, see [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span>
        
    3. <span data-ttu-id="972f0-133">Laden Sie die dll durch Aufrufen der LoadLibrary-Funktion.</span><span class="sxs-lookup"><span data-stu-id="972f0-133">Load the DLL by calling the LoadLibrary function.</span></span> 
        
    4. <span data-ttu-id="972f0-134">Initialisieren Sie das MAPI-Funktionszeiger Array, indem Sie die GetProcAddress-Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="972f0-134">Initialize the MAPI function pointer array by calling the GetProcAddress function.</span></span> 
        
    <span data-ttu-id="972f0-135">Das folgende Beispiel zeigt die vorherigen Schritte:</span><span class="sxs-lookup"><span data-stu-id="972f0-135">The following example shows the previous steps:</span></span>
        
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

3. <span data-ttu-id="972f0-136">Rufen Sie schließlich die Funktion, die Sie in Schritt 2 in ihrer Messaginganwendung erstellt haben, bevor Sie Aufrufe an MAPI-API-Elemente vornehmen.</span><span class="sxs-lookup"><span data-stu-id="972f0-136">Finally, call the function that you created in step 2 in your messaging application before you make calls to MAPI API elements.</span></span> 
    
   > [!CAUTION]
   > <span data-ttu-id="972f0-137">Sie müssen das MAPI-Subsystem vor dem Schließen Ihrer Anwendung deinitialisieren.</span><span class="sxs-lookup"><span data-stu-id="972f0-137">You must uninitialize the MAPI subsystem before closing your application.</span></span> 
  
   <span data-ttu-id="972f0-138">Das folgende Beispiel zeigt diesen Schritt:</span><span class="sxs-lookup"><span data-stu-id="972f0-138">The following example shows this step:</span></span> 
    
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

## <a name="mapistublibrarylib"></a><span data-ttu-id="972f0-139">MAPIStubLibrary. lib</span><span class="sxs-lookup"><span data-stu-id="972f0-139">MAPIStubLibrary.lib</span></span>

<span data-ttu-id="972f0-140">Das Aufkommen von Microsoft Outlook 2010 und 64-Bit-MAPI, das nun auf die Microsoft Outlook 2013 erweitert wird, erfordert mehr als die herkömmliche 32-Bit-API für die vollständige Implementierung.</span><span class="sxs-lookup"><span data-stu-id="972f0-140">The advent of Microsoft Outlook 2010 and 64-bit MAPI, now extending to the Microsoft Outlook 2013, requires more than the traditional 32-bit API for full implementation.</span></span> <span data-ttu-id="972f0-141">Ein neues Projekt, die MAPI-Stub-Bibliothek, die auf der CodePlex-Website bereitgestellt wird, stellt eine Ersatzteil Anwendung für Mapi32. lib bereit, die das Erstellen von sowohl 32-Bit-als auch 64-Bit-MAPI-Anwendungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="972f0-141">A new project, the MAPI Stub Library, posted on the CodePlex website provides a drop-in replacement for Mapi32.lib that supports building both 32-bit and 64-bit MAPI applications.</span></span> <span data-ttu-id="972f0-142">MAPIStubLibrary. lib entfällt die Notwendigkeit, eine explizite Verknüpfung mit MAPI vorzunehmen, und nachdem Sie Sie erstellt haben, können Sie Mapi32. lib aus ihren Linker-Einstellungen entfernen und durch MAPIStubLibrary. lib ersetzen. Es sollten keine weiteren Änderungen am Code erforderlich sein.</span><span class="sxs-lookup"><span data-stu-id="972f0-142">MAPIStubLibrary.lib eliminates the need to explicitly link to MAPI, and having built it, you can remove Mapi32.lib from your linker settings, replacing it with MAPIStubLibrary.lib; no further modifications to your code should be needed.</span></span> <span data-ttu-id="972f0-143">Außerdem ist es nicht erforderlich, **LoadLibrary**-, **GetProcAddress**-und **FreeLibrary** -Code zu schreiben, um neuere Exporte zu verarbeiten, die in dieser Bibliotheksdatei enthalten sind, jedoch nicht in Mapi32. lib, was bei Verwendung der expliziten Verknüpfung erforderlich wäre.</span><span class="sxs-lookup"><span data-stu-id="972f0-143">It also eliminates the need to write **LoadLibrary**, **GetProcAddress**, and **FreeLibrary** code to handle newer exports included in this library file but not in Mapi32.lib, which would be needed if you used explicit linking.</span></span> 
  
<span data-ttu-id="972f0-144">Einige der neuen mit dieser Bibliothek verknüpften Funktionen, die in Mapi32. lib nicht verfügbar sind, umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="972f0-144">Some of the new functions linked from this library that are not available in Mapi32.lib include the following:</span></span>
  
- [<span data-ttu-id="972f0-145">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="972f0-145">GetDefCachedMode</span></span>](getdefcachedmode.md)    
- [<span data-ttu-id="972f0-146">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="972f0-146">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)   
- [<span data-ttu-id="972f0-147">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="972f0-147">HrOpenOfflineObj</span></span>](hropenofflineobj.md)    
- [<span data-ttu-id="972f0-148">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="972f0-148">MAPICrashRecovery</span></span>](mapicrashrecovery.md)   
- [<span data-ttu-id="972f0-149">OpenStreamOnFileW</span><span class="sxs-lookup"><span data-stu-id="972f0-149">OpenStreamOnFileW</span></span>](openstreamonfilew.md)    
- [<span data-ttu-id="972f0-150">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="972f0-150">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)
    
<span data-ttu-id="972f0-151">Eine alternative Methode zum Integrieren der MAPI-Stub-Bibliothek besteht darin, die Quelldateien MapiStubLibrary. cpp und StubUtils. cpp direkt in Ihr Projekt zu kopieren und eine Verknüpfung mit Mapi32. lib und Code zu entfernen, der explizit mit MAPI verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="972f0-151">An alternate method of incorporating the MAPI Stub Library is to copy the source files, MapiStubLibrary.cpp and StubUtils.cpp, directly into your project and remove any linkage to Mapi32.lib and any code that explicitly links to MAPI.</span></span>
  
<span data-ttu-id="972f0-152">Informationen zum Zugreifen auf die MAPI-Stub-Bibliotheksdateien und Informationen zum Erstellen und integrieren in Ihr Projekt sowie Fragen zu dieser Bibliothek, beispielsweise wann und warum Sie Sie verwenden sollten, finden Sie unter der [MAPI-Stub-Bibliothek](https://mapistublibrary.codeplex.com/documentation) auf der CodePlex-Website.</span><span class="sxs-lookup"><span data-stu-id="972f0-152">To access the MAPI Stub Library files and for information about how to build and integrate it into your project, as well as questions about this library such as when and why to use it, see the [MAPI Stub Library](https://mapistublibrary.codeplex.com/documentation) on the CodePlex site.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="972f0-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="972f0-153">See also</span></span>

- [<span data-ttu-id="972f0-154">Übersicht über die MAPI-Programmierung</span><span class="sxs-lookup"><span data-stu-id="972f0-154">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="972f0-155">Installieren des MAPI-Subsystems</span><span class="sxs-lookup"><span data-stu-id="972f0-155">Installing the MAPI Subsystem</span></span>](installing-the-mapi-subsystem.md)
- [<span data-ttu-id="972f0-156">Installieren von MAPI-Header Dateien</span><span class="sxs-lookup"><span data-stu-id="972f0-156">Install MAPI Header Files</span></span>](how-to-install-mapi-header-files.md)
- [<span data-ttu-id="972f0-157">Auswählen einer bestimmten zu ladenden MAPI-Version</span><span class="sxs-lookup"><span data-stu-id="972f0-157">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [<span data-ttu-id="972f0-158">Bestimmen der zu verwendenden Verknüpfungsmethode</span><span class="sxs-lookup"><span data-stu-id="972f0-158">Determining Which Linking Method to Use</span></span>](https://msdn.microsoft.com/library/253b8k2c.aspx)
- [<span data-ttu-id="972f0-159">Verknüpfen einer ausführbaren Datei mit einer dll</span><span class="sxs-lookup"><span data-stu-id="972f0-159">Linking an Executable to a DLL</span></span>](https://msdn.microsoft.com/library/9yd93633.aspx)
- [<span data-ttu-id="972f0-160">Einrichten der MSI-Schlüssel für die MAPI-DLL</span><span class="sxs-lookup"><span data-stu-id="972f0-160">Setting Up the MSI Keys for Your MAPI DLL</span></span>](https://msdn.microsoft.com/library/ee909494%28v=VS.85%29.aspx)

