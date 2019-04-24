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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341713"
---
# <a name="starting-a-service-provider"></a>Starten eines Dienstanbieters

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sobald ein Client eine Sitzung mit MAPI startet, wird der Dienstanbieter gestartet. Transport Anbieter werden gestartet, wenn ein Client eine Anforderung für ihre Dienste stellt. Adressbuch-und Nachrichtenspeicher Anbieter werden während des Anmeldevorgangs des Clients gestartet.
  
Ein Client ruft [IMAPISession:: openaddressbook](imapisession-openaddressbook.md) auf, um alle im Profil enthaltenen Adressbuchanbieter und [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) zu laden, um einen bestimmten Nachrichtenspeicher Anbieter zu laden. Adressbuchanbieter, die Teil eines Nachrichtendiensts sind, werden vor einem der anderen Anbieter im Dienst gestartet. 
  
MAPI startet jeden Dienstanbieter im aktiven Profil wie folgt:
  
- Suchen des Namens der DLL im Profil. Sie müssen den Namen der Anbieter-DLL in der Konfigurationsdatei MAPISVC. inf registrieren, um sicherzustellen, dass Sie im Profil angezeigt wird. Wenn Ihr Dienstanbieter einem Profil einzeln oder als Teil eines Nachrichtendiensts hinzugefügt wird, werden alle **[Dienstanbieter]** Abschnitte aus MAPISVC. inf, die für Ihren Anbieter gelten, in das Profil kopiert. Weitere Informationen zur Struktur von MAPISVC. inf finden Sie unter [Datei Format von MAPISVC. inf](file-format-of-mapisvc-inf.md).
    
- Aufrufen der Windows-API-Funktion **LoadLibrary** zum Laden der dll. Da MAPI bei jeder Verwendung einer Dienstanbieter-DLL (unabhängig davon, ob Sie bereits geladen wurde) oder nur zum ersten Mal **LoadLibrary** aufruft, darf der Dienstanbieter keine Annahmen darüber treffen, wie oft er geladen wird. Bei jedem Aufruf von **LoadLibrary**führt MAPI einen Aufruf der Windows-API-Funktion **FreeLibrary** aus, wenn keine Dienstanbieter-dll mehr benötigt wird. 
    
- Aufrufen der Einstiegspunktfunktion für den Anbieter. MAPI Ruft die Einstiegspunktfunktion Ihres Anbieters auf, um den Anmeldevorgang zu initiieren. Einstiegspunktfunktionen stellen Sie sicher, dass Sie eine Version der Dienstanbieterschnittstelle (Service Provider Interface, SPI) verwenden, die mit der von MAPI verwendeten Version kompatibel ist. Diese Funktionen geben auch Zeiger auf neu erstellte Anbieterobjekte zurück. Weitere Informationen zum Erstellen einer Einstiegspunktfunktion für Ihren Anbieter finden Sie unter [Implementieren einer Dienstanbieter-Einstiegspunktfunktion](implementing-a-service-provider-entry-point-function.md).
    
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

