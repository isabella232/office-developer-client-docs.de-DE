---
title: Verwenden der API zur MAPI-Wiederherstellung nach einem Absturz
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 1a9871c2-b9bb-332e-b67e-85c50f7f685c
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 5398e11320c110e48930f60efb6dc513349d575a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561677"
---
# <a name="use-the-mapi-crash-recovery-api"></a>Verwenden der API zur MAPI-Wiederherstellung nach einem Absturz

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieses Thema enthält ein Codebeispiel in C++, das zeigt, wie die [MAPICrashRecovery-Funktion](mapicrashrecovery.md) aus der [UnhandledExceptionFilter-Funktion](https://msdn.microsoft.com/library/ms681401%28VS.85%29.aspx) aufgerufen wird. Die [MAPICrashRecovery-Funktion](mapicrashrecovery.md) überprüft den Status des freigegebenen Arbeitsspeichers für die Persönliche Ordner-Datei (PST) oder die Offlineordnerdatei (OST). 

Wenn sich der Speicher in einem konsistenten Zustand befindet, verschiebt die [MAPICrashRecovery-Funktion](mapicrashrecovery.md) die Daten auf den Datenträger und verhindert weiteren Lese- oder Schreibzugriff, bis der Prozess beendet wird. Indem Sie sicherstellen, dass sich die PSTs oder OSTs in einem konsistenten Zustand befinden, bevor der Prozess beendet wird, können Sie verhindern, dass Microsoft Outlook 2010 oder Microsoft Outlook 2013 die folgende Fehlermeldung anzeigen und Leistungsprobleme vermeiden: 
  
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

