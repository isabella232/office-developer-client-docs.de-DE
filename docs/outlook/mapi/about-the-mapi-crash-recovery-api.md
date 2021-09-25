---
title: Informationen über die API zur MAPI-Wiederherstellung nach einem Absturz
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: c429cee936390066499a85f9f130790c105481a4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605237"
---
# <a name="about-the-mapi-crash-recovery-api"></a>Informationen über die API zur MAPI-Wiederherstellung nach einem Absturz

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die MAPI-Absturzwiederherstellungs-API überprüft den Status des freigegebenen Speichers für die Persönliche Ordner-Datei (PST) oder die Offlineordnerdatei (OST), um sicherzustellen, dass sich die Daten in einem konsistenten Zustand befinden. Wenn sich die [MAPICrashRecovery-Funktion](mapicrashrecovery.md) in einem konsistenten Zustand befindet, verschiebt sie die Daten von den geöffneten PSTs oder OSTs auf den Datenträger und sperrt die PSTs oder OSTs und lässt keinen Lese- oder Schreibzugriff auf die Daten zu. Dadurch wird sichergestellt, dass die Daten in einem konsistenten Zustand bleiben, bis der Prozess beendet wird. Indem Sie sicherstellen, dass sich die PSTs oder OSTs in einem konsistenten Zustand befinden, bevor der Prozess beendet wird, können Sie verhindern, dass Microsoft Outlook 2013 und Microsoft Outlook 2010 die folgende Fehlermeldung anzeigen und Leistungsprobleme vermeiden. 
  
 **Eine Datendatei wurde bei der letzten Verwendung nicht ordnungsgemäß geschlossen und wird auf Probleme überprüft. Die Leistung kann beeinträchtigt werden, während die Überprüfung ausgeführt wird.**
  
Diese API bietet Folgendes:
  
Konstanten:
  
- [MAPI-Konstanten](mapi-constants.md)
    
Funktionen:
  
- [MAPICrashRecovery](mapicrashrecovery.md)
    
## <a name="see-also"></a>Siehe auch



[Verwenden der API zur MAPI-Wiederherstellung nach einem Absturz](how-to-use-the-mapi-crash-recovery-api.md)

