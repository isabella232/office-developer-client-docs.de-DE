---
title: Verwenden der API zur MAPI-Wiederherstellung nach einem Absturz
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1a9871c2-b9bb-332e-b67e-85c50f7f685c
description: 'Letzte Änderung: Montag, 25. Juni 2012'
ms.openlocfilehash: a73889982e4aa72fb664a8eafd6fc8704e581e98
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388504"
---
# <a name="use-the-mapi-crash-recovery-api"></a>Verwenden der API zur MAPI-Wiederherstellung nach einem Absturz

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieses Thema enthält ein Codebeispiel in C++, das zeigt, wie die [MAPICrashRecovery](mapicrashrecovery.md) -Funktion aus der [UnhandledExceptionFilter](https://msdn.microsoft.com/library/ms681401%28VS.85%29.aspx) -Funktion aufgerufen wird. Die Funktion [MAPICrashRecovery](mapicrashrecovery.md) überprüft, ob der Zustand des Persönliche Ordner-Datei (PST) oder Offlineordnerdatei (OST) Arbeitsspeicher freigegeben. 

Wenn der Arbeitsspeicher in einen konsistenten Status befindet, wird die [MAPICrashRecovery](mapicrashrecovery.md) -Funktion verschiebt die Daten auf dem Datenträger und verhindert, dass weitere Lese- oder Schreibzugriff, bis der Prozess beendet wird. Sicherstellen, dass die PST-Dateien oder OSTs einen konsistenten Status befinden, bevor der Prozess beendet wird, können Sie verhindern, dass Microsoft Outlook 2010 oder Microsoft Outlook 2013 die folgende Fehlermeldung angezeigt und Leistungsprobleme vermeiden: 
  
**Eine Datei wurde nicht ordnungsgemäß geschlossen zuletzt verwendet wurde, und es wird überprüft für Probleme. Während das Kontrollkästchen ausgeführt wird, kann die Leistung beeinträchtigen.**
  
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

