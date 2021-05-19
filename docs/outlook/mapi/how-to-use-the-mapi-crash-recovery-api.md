---
title: Verwenden der API zur MAPI-Wiederherstellung nach einem Absturz
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1a9871c2-b9bb-332e-b67e-85c50f7f685c
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: a73889982e4aa72fb664a8eafd6fc8704e581e98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346424"
---
# <a name="use-the-mapi-crash-recovery-api"></a><span data-ttu-id="92361-103">Verwenden der API zur MAPI-Wiederherstellung nach einem Absturz</span><span class="sxs-lookup"><span data-stu-id="92361-103">Use the MAPI Crash Recovery API</span></span>

<span data-ttu-id="92361-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92361-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92361-105">Dieses Thema enthält ein Codebeispiel in C++, das zeigt, wie die [MAPICrashRecovery-Funktion](mapicrashrecovery.md) aus der [UnhandledExceptionFilter-Funktion aufruft.](https://msdn.microsoft.com/library/ms681401%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92361-105">This topic contains a code sample in C++ that shows how to call the [MAPICrashRecovery](mapicrashrecovery.md) function from the [UnhandledExceptionFilter](https://msdn.microsoft.com/library/ms681401%28VS.85%29.aspx) function.</span></span> <span data-ttu-id="92361-106">Die [MAPICrashRecovery-Funktion](mapicrashrecovery.md) überprüft den Status des freigegebenen Speichers für persönliche Ordner (PST) oder Offlineordnerdatei (OST).</span><span class="sxs-lookup"><span data-stu-id="92361-106">The [MAPICrashRecovery](mapicrashrecovery.md) function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> 

<span data-ttu-id="92361-107">Wenn sich der Arbeitsspeicher in einem konsistenten Zustand befindet, verschiebt die [MAPICrashRecovery-Funktion](mapicrashrecovery.md) die Daten auf den Datenträger und verhindert weiteren Lese- oder Schreibzugriff, bis der Prozess beendet wird.</span><span class="sxs-lookup"><span data-stu-id="92361-107">If the memory is in a consistent state, the [MAPICrashRecovery](mapicrashrecovery.md) function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> <span data-ttu-id="92361-108">Indem Sie sicherstellen, dass sich die PSTs oder BETRIEBSSYSTEME in einem konsistenten Zustand befinden, bevor der Prozess beendet wird, können Sie verhindern, dass Microsoft Outlook 2010 oder Microsoft Outlook 2013 die folgende Fehlermeldung anzeigen und Leistungsprobleme vermeiden:</span><span class="sxs-lookup"><span data-stu-id="92361-108">By ensuring that the PSTs or OSTs are in a consistent state before the process is terminated, you can prevent Microsoft Outlook 2010 or Microsoft Outlook 2013 from displaying the following error message and avoid performance problems:</span></span> 
  
<span data-ttu-id="92361-109">**Eine Datendatei wurde bei der letzten Verwendung nicht ordnungsgemäß geschlossen und wird auf Probleme überprüft. Die Leistung kann während der Überprüfung beeinträchtigt werden.**</span><span class="sxs-lookup"><span data-stu-id="92361-109">**A data file did not close properly the last time it was used and is being checked for problems. Performance might be affected while the check is in progress.**</span></span>
  
```cpp
LONG WINAPI UnhandledExceptionFilter(__in EXCEPTION_POINTERS* pep) 
{ 
    // Let the OS terminate the process upon return. 
    LONG retval = EXCEPTION_EXECUTE_HANDLER; 
 
    switch (pep->ExceptionRecord->ExceptionCode) 
    { 
        case EXCEPTION_BREAKPOINT: 
        case EXCEPTION_SINGLE_STEP: 
            // Ignore debugging exceptions. 
            retval = EXCEPTION_CONTINUE_SEARCH; 
            break; 
 
        default: 
            // The process is going to be terminated, so disconnect the MAPI database. 
            MAPICrashRecovery(MAPICRASH_RECOVER); 
            // Optionally, you can display a crash reporting dialog box here. 
            // If the user chooses to debug,  
            // call MAPICrashRecovery(MAPICRASH_CONTINUE). 
            break; 
    } 
 
    return retval; 
}
```

## <a name="see-also"></a><span data-ttu-id="92361-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92361-110">See also</span></span>

- [<span data-ttu-id="92361-111">Informationen über die API zur MAPI-Wiederherstellung nach einem Absturz</span><span class="sxs-lookup"><span data-stu-id="92361-111">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md) 
- [<span data-ttu-id="92361-112">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="92361-112">MAPICrashRecovery</span></span>](mapicrashrecovery.md)

