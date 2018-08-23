---
title: Verwenden der API zur MAPI-Wiederherstellung nach einem Absturz
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1a9871c2-b9bb-332e-b67e-85c50f7f685c
description: 'Letzte Änderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 41d70c2ab94712e40de9011bc752c79d8c859161
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595181"
---
# <a name="use-the-mapi-crash-recovery-api"></a><span data-ttu-id="95fd0-103">Verwenden der API zur MAPI-Wiederherstellung nach einem Absturz</span><span class="sxs-lookup"><span data-stu-id="95fd0-103">Use the MAPI Crash Recovery API</span></span>

<span data-ttu-id="95fd0-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95fd0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95fd0-105">Dieses Thema enthält ein Codebeispiel in C++, das zeigt, wie die [MAPICrashRecovery](mapicrashrecovery.md) -Funktion aus der [UnhandledExceptionFilter](http://msdn.microsoft.com/en-us/library/ms681401%28VS.85%29.aspx) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="95fd0-105">This topic contains a code sample in C++ that shows how to call the [MAPICrashRecovery](mapicrashrecovery.md) function from the [UnhandledExceptionFilter](http://msdn.microsoft.com/en-us/library/ms681401%28VS.85%29.aspx) function.</span></span> <span data-ttu-id="95fd0-106">Die Funktion [MAPICrashRecovery](mapicrashrecovery.md) überprüft, ob der Zustand des Persönliche Ordner-Datei (PST) oder Offlineordnerdatei (OST) Arbeitsspeicher freigegeben.</span><span class="sxs-lookup"><span data-stu-id="95fd0-106">The [MAPICrashRecovery](mapicrashrecovery.md) function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> 

<span data-ttu-id="95fd0-107">Wenn der Arbeitsspeicher in einen konsistenten Status befindet, wird die [MAPICrashRecovery](mapicrashrecovery.md) -Funktion verschiebt die Daten auf dem Datenträger und verhindert, dass weitere Lese- oder Schreibzugriff, bis der Prozess beendet wird.</span><span class="sxs-lookup"><span data-stu-id="95fd0-107">If the memory is in a consistent state, the [MAPICrashRecovery](mapicrashrecovery.md) function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> <span data-ttu-id="95fd0-108">Sicherstellen, dass die PST-Dateien oder OSTs einen konsistenten Status befinden, bevor der Prozess beendet wird, können Sie verhindern, dass Microsoft Outlook 2010 oder Microsoft Outlook 2013 die folgende Fehlermeldung angezeigt und Leistungsprobleme vermeiden:</span><span class="sxs-lookup"><span data-stu-id="95fd0-108">By ensuring that the PSTs or OSTs are in a consistent state before the process is terminated, you can prevent Microsoft Outlook 2010 or Microsoft Outlook 2013 from displaying the following error message and avoid performance problems:</span></span> 
  
<span data-ttu-id="95fd0-109">**Eine Datei wurde nicht ordnungsgemäß geschlossen zuletzt verwendet wurde, und es wird überprüft für Probleme. Während das Kontrollkästchen ausgeführt wird, kann die Leistung beeinträchtigen.**</span><span class="sxs-lookup"><span data-stu-id="95fd0-109">**A data file did not close properly the last time it was used and is being checked for problems. Performance might be affected while the check is in progress.**</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="95fd0-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95fd0-110">See also</span></span>

- [<span data-ttu-id="95fd0-111">Informationen über die API zur MAPI-Wiederherstellung nach einem Absturz</span><span class="sxs-lookup"><span data-stu-id="95fd0-111">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md) 
- [<span data-ttu-id="95fd0-112">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="95fd0-112">MAPICrashRecovery</span></span>](mapicrashrecovery.md)

