---
title: Starten von einem Dienstanbieter
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4b61cc3-d9fe-4616-a05c-d1e4096b5abd
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 99f47ee4fe990b0e77fcf868977b72d83bfdbac7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795628"
---
# <a name="starting-a-service-provider"></a>Starten von einem Dienstanbieter

 
  
**Betrifft**: Outlook 
  
Zu einem bestimmten Zeitpunkt nach dem Starten eines Clients einer Sitzung mit MAPI, wird Ihr Dienstanbieter gestartet werden. Transportanbieter gestartet wurden, wenn ein Client für ihre Dienste anfordert. Address Book und Message-Anbieter werden während der Client Anmeldevorgang gestartet.
  
Ein Client ruft [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) , um die im Profil und [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) zum Laden der Anbieter eine bestimmte Nachricht enthalten adressbuchanbietern implementierte zu laden. Von adressbuchanbietern implementierte, die Teil eines Diensts Nachricht sind wurden vor allen anderen Anbieter im Dienst gestartet. 
  
MAPI startet jeder Dienstanbieter in das aktive Profil, indem Sie wie folgt vorgehen:
  
- Suchen den Namen der entsprechenden DLL im Profil. Sie müssen den Namen Ihres Anbieters DLL registrieren, in der Konfigurationsdatei Mapisvc.inf, um sicherzustellen, dass es im Profil angezeigt wird. Wenn Ihr Dienstanbieter zu einem Profil einzeln oder als Teil eines Diensts Nachricht hinzugefügt wird, werden alle Abschnitte **[Service Provider]** aus Mapisvc.inf, die vom Dienstanbieter liegen, in das Profil kopiert. Weitere Informationen zur Struktur von Mapisvc.inf finden Sie unter [File Format der MapiSvc.inf](file-format-of-mapisvc-inf.md).
    
- Aufrufen der Windows-API-Funktion **LoadLibrary** zum Laden der DLL. Da MAPI **LoadLibrary** entweder jedes Mal, wenn es verwendet einen Dienstanbieter DLL (unabhängig davon, ob es bereits geladen wurde) oder nur beim ersten Mal aufruft, muss Ihren Dienstanbieter nicht Annahmen über die Anzahl der Male vornehmen, die sie geladen wird. Für jeden Aufruf von **LoadLibrary**führt MAPI einen Aufruf an die Windows-API-Funktion **FreeLibrary** bei einem Dienstanbieter, die, den DLL nicht mehr benötigt wird. 
    
- Aufrufen der Eintrag Point-Funktion für den Anbieter. MAPI-Aufrufen des Anbieters Eintrag Point-Funktion zum Initiieren des Anmeldevorgangs. Entry Point Funktionen stellen Sie sicher, dass Sie eine Version der der Dienstanbieter-Schnittstelle (SPI) verwenden, die mit der Version von MAPI verwendet wird, kompatibel ist. Diese Funktionen geben auch Zeiger auf neu erstellten Anbieterobjekte. Zeigen Sie die Funktion für Weitere Informationen zum Erstellen eines Eintrags für den Anbieter, finden Sie unter [Implementieren einer Service Provider Eintrag zeigen-Funktion](implementing-a-service-provider-entry-point-function.md).
    
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

