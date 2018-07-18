---
title: Bewährte Methoden für das schnelle Herunterfahren
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ae8a9214-e53f-4c57-8dbe-aa7cc6903aa8
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0d9e7caf43bcee654aa92652e94bc8c2ebba18e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791375"
---
# <a name="best-practices-for-fast-shutdown"></a>Bewährte Methoden für das schnelle Herunterfahren

  
  
**Betrifft**: Outlook 
  
In diesem Thema empfiehlt bewährte Methoden für Administratoren, MAPI-Clients und MAPI-Anbieter, um die Einstellungen der Windows-Registrierung und das schnelle Herunterfahren-Schnittstellen verwenden, um während des Herunterfahrens Client Datenverluste zu minimieren.
  
- Damit ein MAPI-Client, um Schnelles Herunterfahren erfolgreich auszuführen, sodass Anbieter Prozesse nicht ein gewisser Datenverlust auftreten muss der MAPI-Client zunächst die [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) -Methode aufrufen. Der Client sollte mit den Methoden [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) und [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) basierend auf den MAPI-Subsystems Unterstützung für schnelle Herunterfahren, fahren Sie durch den Rückgabewert der ** IMAPIClientShutdown::QueryFastShutdown**. Als MAPI-Client ist Microsoft Outlook nicht **IMAPIClientShutdown::NotifyProcessShutdown** oder **IMAPIClientShutdown::DoFastShutdown** aufrufen, wenn **IMAPIClientShutdown::QueryFastShutdown** einen Fehler zurückgibt. Wenn der Administrator Schnelles Herunterfahren in der Windows-Registrierung deaktiviert wurde, würde der MAPI-Subsystems MAPI_E_NO_SUPPORT an **IMAPIClientShutdown::QueryFastShutdown**zurückgeben. In diesem Fall würde des MAPI-Subsystems nicht darüber informiert, dass es sich bei MAPI-Anbieter über einen sofortigen Clientprozess beenden. Wenn ein MAPI-Client dieser Fehler Rückgabecode ignoriert, geht zum Herunterfahren schnelle und alle externen Verweise trennt, müssen alle geladenen MAPI-Anbieter Datenverlust daher. 
    
- MAPI-Anbieter implementieren sollten die [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) Schnittstelle für die Durchführung rechtzeitig und die erforderlichen Schritte zur Vermeidung Verlust von Daten durch den Client externe Verweise trennen, bevor der Client beendet wird. Ein Anbieter sollte alles verschieben, das zum Speichern von Daten als primären Datenspeicher nicht benötigte ist. Beispiel ein Transportdienstes sollten unnötige Hintergrundvorgängen, die für neue Nachrichten überprüfen einer Adressbuchanbieter verschiebt sollte das Herunterladen von kürzlichen Änderungen vom Server verschieben und sollte ein Anbieter anmelden Wartungsaufgaben wie verschieben Komprimieren oder indizieren. 
    
- Benutzer, die MAPI-Clients zu beenden, sobald sie diese schließen möchten, sollten die Standardeinstellung für die Registrierung verwenden, die Schnelles Herunterfahren aktiviert, es sei denn, ein Anbieter entscheidet.
    
- Nachdem ein MAPI-Client **IMAPIClientShutdown::DoFastShutdown**aufruft, sollte zusätzlichen Anrufe MAPI, einschließlich der [MAPIUninitialize](mapiuninitialize.md) -Funktion nicht ermöglichen. Der Client sollte MAPI für den Rest der Lebensdauer des Clientprozesses nicht verwenden. 
    
- Ein MAPI-Client sollte niemals direkt eine Anbieterschnittstelle **IMAPIProviderShutdown** aufrufen. Verwenden Sie MAPI-Clients sollte immer die [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md) Schnittstelle. 
    
- Wenn ein MAPI-Anbieter muss sicherstellen, dass diese schnelle Herunterfahren nicht verwendet wird, während es geladen wird, muss die **IMAPIProviderShutdown** -Schnittstelle implementieren und MAPI_E_NO_SUPPORT für die **IMAPIProviderShutdown::QueryFastShutdown** -Methode zurückgegeben. MAPI-Clients wie Outlook verursacht dies jedoch den Client Schnelles Herunterfahren abbrechen und zum Herunterfahren längere Zeit in Anspruch nehmen. 
    
## <a name="see-also"></a>Siehe auch



[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)
  
[Übersicht über das schnelle Herunterfahren](fast-shutdown-overview.md)
  
[Benutzeroptionen für das schnelle Herunterfahren](fast-shutdown-user-options.md)

