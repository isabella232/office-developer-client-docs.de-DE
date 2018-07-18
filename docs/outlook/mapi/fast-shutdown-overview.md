---
title: Übersicht über das schnelle Herunterfahren
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a7830d73-427c-4f8b-86f4-51e040c142c3
description: 'Zuletzt geändert: 26 Juni 2012'
ms.openlocfilehash: 17b1307427af2c35fe9ba8ee40dc78958e6b4a21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791651"
---
# <a name="fast-shutdown-overview"></a>Übersicht über das schnelle Herunterfahren

**Betrifft**: Outlook 
  
Schnelles Herunterfahren ist ein Mechanismus für einen MAPI-Client initiiert ein Schnelles Herunterfahren des Clientprozesses benachrichtigen alle Anbieter mit dem der Client verfügt über eine aktive MAPI-Sitzung auf Daten und Einstellungen zu speichern, bevor der Clientprozess beendet wird. In diesem Thema werden den grundlegenden Mechanismus für Schnelles Herunterfahren. 

Ab Microsoft Outlook 2010 und jetzt mit Microsoft Outlook 2013 MAPI-Subsystems bietet die [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md) Schnittstelle. Outlook und andere MAPI-Clients können Schnelles Herunterfahren als Standardmechanismus für den Client zu beenden einführen. Eine Einstellung auf Benutzerebene in der Windows-Registrierung des Clientcomputers steuert die Akzeptanz Schnelles Herunterfahren für alle MAPI-Clients für diesen Benutzer auf diesem Computer. Ausführliche Informationen zu den Einstellungen in der Registrierung finden Sie unter [Fast Herunterfahren Benutzeroptionen](fast-shutdown-user-options.md).
  
Wenn ein MAPI-Client Schnelles Herunterfahren einführen muss, verwenden sie die **IMAPIClientShutdown: IUnknown** Schnittstelle. Dies ist der typische Kurs der Ereignisse aus, wenn der Client versucht, fahren Sie: 
  
1. Der MAPI-Client initiiert das Herunterfahren durch Aufrufen der [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) -Methode, um festzustellen, ob das MAPI-Subsystem Schnelles Herunterfahren unterstützt. 
    
2. MAPI-Subsystems antwortet mit der die verfügbaren Schnelles Herunterfahren Unterstützung an den Client **IMAPIClientShutdown::QueryFastShutdown** Aufruf mithilfe des folgenden Verfahrens: 
    
    1. MAPI-Subsystems die [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) -Methode für jeden MAPI-Anbieter, mit dem der MAPI-Client-Prozess eine aktive MAPI-Sitzung hat, aufgerufen, wenn der Anbieter implementiert hat die [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) Schnittstelle. 
        
       > [!NOTE]
       >  MAPI-Subsystems fragt immer und benachrichtigt MAPI-Anbieter über die **IMAPIProviderShutdown: IUnknown** Schnittstelle innerhalb jedes MAPI-Sitzung in der folgenden Reihenfolge:
       > 1. Transportanbieter
       > 2. Von adressbuchanbietern implementierte
       > 3. Speicheranbieter 
    
    2. Abhängig von der Einstellung der Schnelles Herunterfahren Registrierung für diesen Benutzer auf dem Clientcomputer gibt an, dass die entsprechenden Code an **IMAPIClientShutdown::QueryFastShutdown**Zurückgeben des MAPI-Subsystems. Der Rückgabecode wird S_OK oder MAPI_E_NO_SUPPORT.
        
    3. Der MAPI-Client Ruft die [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) -Methode, um die Absicht Herunterfahren des MAPI-Subsystems anzuzeigen. 
        
    4. MAPI-Subsystems gibt an, aller geladenen MAPI-Dienstanbieter, die der MAPI-Client beendet wird. Für diesen Anbieter, die implementiert haben die **IMAPIProviderShutdown: IUnknown** -Schnittstelle des MAPI-Subsystems Ruft die entsprechende [IMAPIProviderShutdown::NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) -Methode. 
        
    5. Der MAPI-Client Ruft die [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) -Methode, um für die MAPI-Subsystems anzugeben, dass der Clientprozess sofort beendet wird. 
        
    6. MAPI-Subsystems gibt jeden geladenen MAPI-Anbieter an, dass der MAPI-Client-Prozess beendet wird. Für diesen Anbieter, die implementiert haben die **IMAPIProviderShutdown: IUnknown** -Schnittstelle des MAPI-Subsystems Ruft die entsprechende [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) -Methode. Zu diesem Zeitpunkt sollte diese MAPI-Anbieter überprüfen, ob alle erforderliche Aktionen wie das Speichern von Daten und Einstellungen für die Vorbereitung der MAPI-Client sofort alle Verweise zu trennen und Anwendung beenden abgeschlossen sind. 
    
## <a name="see-also"></a>Siehe auch

- [Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)
- [Benutzeroptionen für das schnelle Herunterfahren](fast-shutdown-user-options.md)
- [Bewährte Methoden für das schnelle Herunterfahren](best-practices-for-fast-shutdown.md)

