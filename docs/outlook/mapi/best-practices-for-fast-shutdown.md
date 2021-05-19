---
title: Bewährte Methoden für schnelles Herunterfahren
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ae8a9214-e53f-4c57-8dbe-aa7cc6903aa8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8c7225427b80d89c6dd8adfa85f7d91885850365
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426968"
---
# <a name="best-practices-for-fast-shutdown"></a>Bewährte Methoden für schnelles Herunterfahren

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Thema werden bewährte Methoden für Administratoren, MAPI-Clients und MAPI-Anbieter empfohlen, Windows Registrierungseinstellungen und die Schnittstellen zum schnellen Herunterfahren zu verwenden, um Datenverluste beim Herunterfahren des Clients zu minimieren.
  
- Damit ein MAPI-Client das schnelle Herunterfahren erfolgreich ausführen kann, damit anbieterprozesse keinen Datenverlust entstehen, sollte der MAPI-Client zuerst die [IMAPIClientShutdown::QueryFastShutdown-Methode](imapiclientshutdown-queryfastshutdown.md) aufrufen. Der Client sollte dann mit den [Methoden IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) und [IMAPIClientShutdown::D oFastShutdown](imapiclientshutdown-dofastshutdown.md) basierend auf der Unterstützung des MAPI-Subsystems für schnelles Herunterfahren fortfahren, wie durch den Rückgabewert von **IMAPIClientShutdown::QueryFastShutdown angegeben.** Als MAPI-Client wird von Microsoft Outlook **nicht IMAPIClientShutdown::NotifyProcessShutdown** oder **IMAPIClientShutdown::D oFastShutdown aufgerufen,** wenn **IMAPIClientShutdown::QueryFastShutdown** einen Fehler zurückgibt. Wenn der Administrator das schnelle Herunterfahren in der Windows deaktiviert hat, würde das MAPI-Subsystem MAPI_E_NO_SUPPORT **IMAPIClientShutdown::QueryFastShutdown zurückgeben.** In diesem Fall informiert das MAPI-Subsystem die MAPI-Anbieter nicht über einen sofortigen Clientprozessabgang. Wenn daher ein MAPI-Client diesen Fehlerrücklaufcode ignoriert, mit dem schnellen Herunterfahren fortschreitet und alle externen Verweise getrennt werden, haben alle geladenen MAPI-Anbieter Datenverlust. 
    
- MAPI-Anbieter sollten die [IMAPIProviderShutdown : IUnknown-Schnittstelle](imapiprovidershutdowniunknown.md) implementieren, um rechtzeitige und erforderliche Schritte zur Vermeidung von Datenverlusten zu ergreifen, da der Client externe Verweise trennt, bevor der Client beendet wird. Ein Anbieter sollte alles andere verschieben, was für das Speichern von Daten in seinem primären Datenspeicher nicht von Bedenklich ist. Beispielsweise sollte ein Transportanbieter unnötige Hintergrundvorgänge verschieben, die nach neuen E-Mails suchen, ein Adressbuchanbieter sollte das Herunterladen der letzten Änderungen von seinem Server verschieben, und ein Speicheranbieter sollte Wartungsaufgaben wie die Komprimiertheit oder Indizierung verschieben. 
    
- Benutzer, für die MAPI-Clients beendet werden sollen, sobald sie sie schließen, sollten die Standardregistrierungseinstellung verwenden, die ein schnelles Herunterfahren ermöglicht, sofern sich ein Anbieter nicht abmeldet.
    
- Sobald ein MAPI-Client **IMAPIClientShutdown::D oFastShutdown** aufruft, sollte er keine weiteren Aufrufe von MAPI, einschließlich der [MAPIUninitialize-Funktion,](mapiuninitialize.md) machen. Der Client sollte MAPI für die restliche Lebensdauer des Clientprozesses nicht verwenden. 
    
- Ein MAPI-Client sollte niemals die **IMAPIProviderShutdown-Schnittstelle** eines Anbieters direkt aufrufen. MAPI-Clients sollten immer die [IMAPIClientShutdown : IUnknown-Schnittstelle](imapiclientshutdowniunknown.md) verwenden. 
    
- Wenn ein MAPI-Anbieter sicherstellen muss, dass beim Laden kein schnelles Herunterfahren verwendet wird, sollte er die **IMAPIProviderShutdown-Schnittstelle** implementieren und MAPI_E_NO_SUPPORT für die **IMAPIProviderShutdown::QueryFastShutdown-Methode** zurückgeben. Für MAPI-Clients wie Outlook verursacht dies jedoch, dass der Client das schnelle Herunterfahren auf sich nimmt und längere Zeit zum Herunterfahren benötigt. 
    
## <a name="see-also"></a>Siehe auch



[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)
  
[Übersicht über das schnelle Herunterfahren](fast-shutdown-overview.md)
  
[Benutzeroptionen für schnelles Herunterfahren](fast-shutdown-user-options.md)

