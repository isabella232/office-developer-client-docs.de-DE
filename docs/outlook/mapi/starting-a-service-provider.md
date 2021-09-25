---
title: Starten eines Dienstanbieters
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c4b61cc3-d9fe-4616-a05c-d1e4096b5abd
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: dd72648a03b0f304f2ac239bb26154ac8c332b3f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619701"
---
# <a name="starting-a-service-provider"></a>Starten eines Dienstanbieters

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zu einem bestimmten Zeitpunkt, nachdem ein Client eine Sitzung mit MAPI gestartet hat, wird Ihr Dienstanbieter gestartet. Transportanbieter werden gestartet, wenn ein Client eine Anforderung für seine Dienste sendet. Adressbuch- und Nachrichtenspeicheranbieter werden während des Anmeldevorgangs des Clients gestartet.
  
Ein Client ruft [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) auf, um jeden im Profil enthaltenen Adressbuchanbieter und [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) zum Laden eines bestimmten Nachrichtenspeicheranbieters zu laden. Adressbuchanbieter, die Teil eines Nachrichtendiensts sind, werden vor einem der anderen Anbieter im Dienst gestartet. 
  
Die MAPI startet jeden Dienstanbieter im aktiven Profil wie folgt:
  
- Suchen des Namens der DLL im Profil. Sie müssen den Namen der Anbieter-DLL in der Konfigurationsdatei Mapisvc.inf registrieren, um sicherzustellen, dass er im Profil angezeigt wird. Wenn Ihr Dienstanbieter einem Profil entweder einzeln oder als Teil eines Nachrichtendiensts hinzugefügt wird, werden alle **[Dienstanbieter]-Abschnitte** von Mapisvc.inf, die für Ihren Anbieter gelten, in das Profil kopiert. Weitere Informationen zur Struktur von Mapisvc.inf finden Sie unter [Dateiformat von MapiSvc.inf](file-format-of-mapisvc-inf.md).
    
- Aufrufen der Windows API-Funktion **LoadLibrary** zum Laden der DLL. Da die MAPI **LoadLibrary** entweder jedes Mal aufruft, wenn sie eine Dienstanbieter-DLL verwendet (unabhängig davon, ob sie bereits geladen wurde) oder nur beim ersten Mal, darf Ihr Dienstanbieter nicht davon ausgehen, wie oft es geladen wird. Für jeden Aufruf von **LoadLibrary** ruft MAPI die Windows API-Funktion **FreeLibrary** auf, wenn keine Dienstanbieter-DLL mehr benötigt wird. 
    
- Aufrufen der Einstiegspunktfunktion für den Anbieter. MAPI ruft die Einstiegspunktfunktion Ihres Anbieters auf, um den Anmeldevorgang zu initiieren. Einstiegspunktfunktionen stellen sicher, dass Sie eine Version der Dienstanbieterschnittstelle (SPI) verwenden, die mit der von mapi verwendeten Version kompatibel ist. Diese Funktionen geben auch Zeiger auf neu erstellte Anbieterobjekte zurück. Weitere Informationen zum Erstellen einer Einstiegspunktfunktion für Ihren Anbieter finden Sie unter [Implementieren einer Dienstanbieter-Einstiegspunktfunktion.](implementing-a-service-provider-entry-point-function.md)
    
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

