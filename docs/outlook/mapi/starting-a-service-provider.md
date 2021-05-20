---
title: Starten eines Dienstanbieters
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4b61cc3-d9fe-4616-a05c-d1e4096b5abd
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: f67976681ef0283c86e1c09c49e531572668ff50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439555"
---
# <a name="starting-a-service-provider"></a>Starten eines Dienstanbieters

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zu einem bestimmten Zeitpunkt, nachdem ein Client eine Sitzung mit MAPI gestartet hat, wird Ihr Dienstanbieter gestartet. Transportanbieter werden gestartet, wenn ein Client eine Anforderung für ihre Dienste stellt. Adressbuch- und Nachrichtenspeicheranbieter werden während des Anmeldevorgangs des Clients gestartet.
  
Ein Client ruft [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) auf, um jeden im Profil enthaltenen Adressbuchanbieter und [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) zu laden, um einen bestimmten Nachrichtenspeicheranbieter zu laden. Adressbuchanbieter, die Teil eines Nachrichtendiensts sind, werden vor einem der anderen Anbieter im Dienst gestartet. 
  
MAPI startet jeden Dienstanbieter im aktiven Profil, indem er folgendes vorgeht:
  
- Suchen des Namens der DLL im Profil. Sie müssen den Namen Ihrer Anbieter-DLL in der Konfigurationsdatei Mapisvc.inf registrieren, um sicherzustellen, dass sie im Profil angezeigt wird. Wenn Ihr Dienstanbieter einem Profil entweder einzeln oder als Teil eines Nachrichtendiensts hinzugefügt wird, werden alle **[Dienstanbieter]-Abschnitte** von Mapisvc.inf, die für Ihren Anbieter gelten, in das Profil kopiert. Weitere Informationen zur Struktur von Mapisvc.inf finden Sie unter [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).
    
- Aufrufen der **Windows-API-Funktion LoadLibrary** zum Laden der DLL. Da MAPI **LoadLibrary** entweder jedes Mal aufruft, wenn eine Dienstanbieter-DLL verwendet wird (unabhängig davon, ob sie bereits geladen wurde) oder nur beim ersten Mal, darf Ihr Dienstanbieter keine Annahmen zur Anzahl der Ladezeiten treffen. Bei jedem Aufruf von **LoadLibrary** nimmt MAPI einen Aufruf der Windows-API-Funktion **FreeLibrary** vor, wenn keine Dienstanbieter-DLL mehr benötigt wird. 
    
- Aufrufen der Einstiegspunktfunktion für den Anbieter. MAPI ruft die Einstiegspunktfunktion Ihres Anbieters auf, um den Anmeldevorgang zu initiieren. Einstiegspunktfunktionen stellen sicher, dass Sie eine Version der Dienstanbieterschnittstelle (Service Provider Interface, SPI) verwenden, die mit der von MAPI verwendeten Version kompatibel ist. Diese Funktionen geben auch Zeiger auf neu erstellte Anbieterobjekte zurück. Weitere Informationen zum Erstellen einer Einstiegspunktfunktion für Ihren Anbieter finden Sie unter [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).
    
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

