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
# <a name="use-the-mapi-crash-recovery-api"></a>Verwenden der API zur MAPI-Wiederherstellung nach einem Absturz

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieses Thema enthält ein Codebeispiel in C++, das zeigt, wie die [MAPICrashRecovery](mapicrashrecovery.md) -Funktion von der [UnhandledExceptionFilter](https://msdn.microsoft.com/library/ms681401%28VS.85%29.aspx) -Funktion aufgerufen wird. Die [MAPICrashRecovery](mapicrashrecovery.md) -Funktion überprüft den Status des freigegebenen Speichers (PST) oder der Offline Ordner Datei (Ost). 

Wenn sich der Speicher in einem konsistenten Zustand befindet, verschiebt die [MAPICrashRecovery](mapicrashrecovery.md) -Funktion die Daten auf den Datenträger und verhindert den weiteren Lese-oder Schreibzugriff, bis der Prozess beendet wird. Wenn Sie sicherstellen, dass sich PST oder Kosten in einem konsistenten Zustand befinden, bevor der Prozess beendet wird, können Sie verhindern, dass Microsoft Outlook 2010 oder Microsoft Outlook 2013 folgende Fehlermeldung angezeigt wird und Leistungsprobleme vermeiden: 
  
**Eine Datendatei wurde bei der letzten Verwendung nicht ordnungsgemäß geschlossen und wird auf Probleme überprüft. Die Leistung kann beeinträchtigt werden, während die Überprüfung ausgeführt wird.**
  
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

## <a name="see-also"></a>Siehe auch

- [Informationen über die API zur MAPI-Wiederherstellung nach einem Absturz](about-the-mapi-crash-recovery-api.md) 
- [MAPICrashRecovery](mapicrashrecovery.md)

