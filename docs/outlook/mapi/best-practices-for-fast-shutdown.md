---
title: Bewährte Methoden für das schnelle Herunterfahren
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
# <a name="best-practices-for-fast-shutdown"></a>Bewährte Methoden für das schnelle Herunterfahren

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Thema werden bewährte Methoden für Administratoren, MAPI-Clients und MAPI-Anbieter empfohlen, die die Windows-Registrierungseinstellungen und die schnell heruntergefahrenen Schnittstellen verwenden, um Datenverluste beim Herunterfahren des Clients zu minimieren.
  
- Damit ein MAPI-Client das schnelle Herunterfahren erfolgreich ausführen kann, sodass Anbieter Prozesse keinen Datenverlust verursachen, sollte der MAPI-Client zunächst die [IMAPIClientShutdown:: QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) -Methode aufrufen. Der Client sollte dann mit den Methoden [IMAPIClientShutdown:: NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) und [IMAPIClientShutdown::D ofastshutdown](imapiclientshutdown-dofastshutdown.md) basierend auf der Unterstützung des MAPI-Subsystems für schnelles Herunterfahren Vorgehen, wie durch den Rückgabewert von ** IMAPIClientShutdown:: QueryFastShutdown**. Als MAPI-Client ruft Microsoft Outlook nicht **IMAPIClientShutdown:: NotifyProcessShutdown** oder **IMAPIClientShutdown::D ofastshutdown** auf, wenn **IMAPIClientShutdown:: QueryFastShutdown** einen Fehler zurückgibt. Wenn der Administrator das schnelle Herunterfahren in der Windows-Registrierung deaktiviert hat, würde das MAPI-Subsystem MAPI_E_NO_SUPPORT an **IMAPIClientShutdown:: QueryFastShutdown**zurückgeben. In diesem Fall informiert das MAPI-Subsystem MAPI-Anbieter nicht über einen sofortigen Clientprozess-Exit. Wenn also ein MAPI-Client diesen Fehler zurückgibt, wird der Rückgabewert des Fehlers beendet, und alle externen Verweise werden getrennt, alle geladenen MAPI-Anbieter haben Datenverlust. 
    
- MAPI-Anbieter sollten die [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) -Schnittstelle implementieren, um rechtzeitige und erforderliche Schritte auszuführen, um Datenverluste zu vermeiden, da externe Verweise vom Client getrennt werden, bevor der Client beendet wird. Ein Anbieter sollte alles andere verschieben, was nicht unbedingt erforderlich ist, um Daten in seinem primären Datenspeicher zu speichern. Ein Transportanbieter sollte beispielsweise unnötige Hintergrundvorgänge verschieben, die auf neue e-Mails prüfen, ein Adressbuchanbieter sollte das Herunterladen der letzten Änderungen von seinem Server hinausschieben, und ein Speicheranbieter sollte Wartungsaufgaben wie komprimieren oder indizieren. 
    
- Benutzer, die MAPI-Clients beenden sollen, sobald Sie Sie schließen, sollten die Standard Registrierungseinstellung verwenden, die das schnelle Herunterfahren ermöglicht, es sei denn, ein Anbieter wählt aus.
    
- Wenn ein MAPI-Client **IMAPIClientShutdown::D ofastshutdown**aufruft, dürfen keine weiteren Aufrufe an MAPI vorgenommen werden, einschließlich der [MAPIUninitialize](mapiuninitialize.md) -Funktion. Der Client sollte MAPI für die restliche Lebensdauer des Clientprozesses nicht verwenden. 
    
- Ein MAPI-Client sollte niemals die **IMAPIProviderShutdown** -Schnittstelle eines Anbieters direkt aufrufen. MAPI-Clients sollten immer die [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md) -Schnittstelle verwenden. 
    
- Wenn ein MAPI-Anbieter sicherstellen muss, dass das schnelle Herunterfahren beim Laden nicht verwendet wird, sollte er die **IMAPIProviderShutdown** -Schnittstelle implementieren und MAPI_E_NO_SUPPORT für die **IMAPIProviderShutdown:: QueryFastShutdown** -Methode zurückgeben. Für MAPI-Clients wie Outlook führt dies jedoch dazu, dass der Client das schnelle Herunterfahren aufgibt und das Herunterfahren länger dauert. 
    
## <a name="see-also"></a>Siehe auch



[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)
  
[Übersicht über das schnelle Herunterfahren](fast-shutdown-overview.md)
  
[Benutzeroptionen für das schnelle Herunterfahren](fast-shutdown-user-options.md)

