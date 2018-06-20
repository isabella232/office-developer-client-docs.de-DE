---
title: Über die Wiederherstellung von MAPI-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 34589860ed25f8236a343e16679c2e7a6bdd1e2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791237"
---
# <a name="about-the-mapi-crash-recovery-api"></a>Über die Wiederherstellung von MAPI-API

  
  
**Betrifft**: Outlook 
  
MAPI-abstürzen Wiederherstellung API überprüft der Status der Persönliche Ordner-Datei (PST) oder Offlineordnerdatei (OST) freigegebenen Speicher, um sicherzustellen, dass die Daten in einer konsistenten Zustand befindet. Ist in einen konsistenten Status, verschiebt die Daten aus dem open PST-Dateien oder OSTs auf dem Datenträger die [MAPICrashRecovery](mapicrashrecovery.md) -Funktion und sperrt die PST-Dateien oder OSTs und lässt keine Lese- oder Schreibzugriff auf die Daten. Dadurch wird sichergestellt, dass die Konsistenz der gelesenen Daten, bis der Prozess beendet wird. Sicherstellen, dass die PST-Dateien oder OSTs einen konsistenten Status befinden, bevor der Prozess beendet wird, können Sie verhindern, dass Microsoft Outlook 2013 und Microsoft Outlook 2010 die folgende Fehlermeldung angezeigt und Leistungsprobleme vermeiden. 
  
 **Eine Datei wurde nicht ordnungsgemäß geschlossen zuletzt verwendet wurde, und es wird überprüft für Probleme. Während das Kontrollkästchen ausgeführt wird, kann die Leistung beeinträchtigen.**
  
Diese API bietet folgende Funktionen:
  
Konstanten:
  
- [MAPI-Konstanten](mapi-constants.md)
    
Funktionen:
  
- [MAPICrashRecovery](mapicrashrecovery.md)
    
## <a name="see-also"></a>Siehe auch



[Verwenden Sie die Wiederherstellung von MAPI-API](how-to-use-the-mapi-crash-recovery-api.md)

