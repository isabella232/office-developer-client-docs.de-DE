---
title: Übersicht über das schnelle Herunterfahren
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a7830d73-427c-4f8b-86f4-51e040c142c3
description: 'Letzte Änderung: 26. Juni 2012'
ms.openlocfilehash: 8c33214b04e7c41eab173196c09f145c20ddf219
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427206"
---
# <a name="fast-shutdown-overview"></a>Übersicht über das schnelle Herunterfahren

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das schnelle Herunterfahren ist ein Mechanismus für einen MAPI-Client, um ein schnelles Herunterfahren des Clientprozesses zu initiieren, wobei alle Anbieter benachrichtigt werden, mit denen der Client über eine aktive MAPI-Sitzung verfügt, um Daten und Einstellungen zu speichern, bevor der Clientprozess beendet wird. In diesem Thema wird der grundlegende Mechanismus für schnelles Herunterfahren beschrieben. 

Beginnend mit Microsoft Outlook 2010 und jetzt einschließlich Microsoft Outlook 2013, stellt das MAPI-Subsystem die [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md) -Schnittstelle bereit. Outlook und andere MAPI-Clients können das schnelle Herunterfahren als Standardmechanismus zum Beenden des Clientprozesses festlegen. Eine Einstellung auf Benutzerebene in der Windows-Registrierung des Clientcomputers steuert das schnelle Herunterfahren für alle MAPI-Clients für diesen Benutzer auf diesem Computer. Ausführliche Informationen zu den Registrierungseinstellungen finden Sie unter [Benutzeroptionen für das schnelle Herunterfahren](fast-shutdown-user-options.md).
  
Wenn ein MAPI-Client Schnelles Herunterfahren übernehmen muss, muss die **IMAPIClientShutdown: IUnknown** -Schnittstelle verwendet werden. Es folgt ein typischer Verlauf von Ereignissen, wenn der Client versucht, das Herunterfahren zu beenden: 
  
1. Der MAPI-Client initiiert das Herunterfahren durch Aufrufen der [IMAPIClientShutdown:: QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) -Methode, um zu bestimmen, ob das MAPI-Subsystem das schnelle Herunterfahren unterstützt. 
    
2. Das MAPI-Subsystem antwortet mit der verfügbaren Unterstützung für das schnelle Herunterfahren auf den **IMAPIClientShutdown:: QueryFastShutdown** -Aufruf des Clients, indem Sie das folgende Verfahren ausführen: 
    
    1. Das MAPI-Subsystem Ruft die [IMAPIProviderShutdown:: QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) -Methode für jeden MAPI-Anbieter auf, mit dem der MAPI-Clientprozess eine aktive MAPI-Sitzung hat, wenn der Anbieter das IMAPIProviderShutdown implementiert hat [: IUnknown](imapiprovidershutdowniunknown.md) Oberfläche. 
        
       > [!NOTE]
       >  Das MAPI-Subsystem fragt MAPI-Anbieter immer über die **IMAPIProviderShutdown: IUnknown** -Schnittstelle innerhalb jeder MAPI-Sitzung ab und benachrichtigt Sie in der folgenden Reihenfolge:
       > 1. Transport Anbieter
       > 2. Adressbuchanbieter
       > 3. Speicheranbieter 
    
    2. Abhängig von der Registrierungseinstellung für das schnelle Herunterfahren für diesen Benutzer auf dem Clientcomputer gibt das MAPI-Subsystem den entsprechenden Rückgabecode für **IMAPIClientShutdown:: QueryFastShutdown**an. Der Rückgabecode ist entweder S_OK oder MAPI_E_NO_SUPPORT.
        
    3. Der MAPI-Client ruft die [IMAPIClientShutdown:: NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) -Methode auf, um dem MAPI-Subsystem anzuzeigen, dass das Herunterfahren beabsichtigt ist. 
        
    4. Das MAPI-Subsystem gibt jedem geladenen MAPI-Anbieter an, dass der MAPI-Client heruntergefahren wird. Für die Anbieter, die die **IMAPIProviderShutdown: IUnknown** -Schnittstelle implementiert haben, ruft das MAPI-Subsystem die entsprechende [IMAPIProviderShutdown:: NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) -Methode auf. 
        
    5. Der MAPI-Client ruft die [IMAPIClientShutdown::D ofastshutdown](imapiclientshutdown-dofastshutdown.md) -Methode auf, um dem MAPI-Subsystem anzuzeigen, dass der Clientprozess sofort beendet wird. 
        
    6. Das MAPI-Subsystem gibt jedem geladenen MAPI-Anbieter an, dass der MAPI-Clientprozess beendet wird. Für die Anbieter, die die **IMAPIProviderShutdown: IUnknown** -Schnittstelle implementiert haben, ruft das MAPI-Subsystem die entsprechende [IMAPIProviderShutdown::D Ofastshutdown](imapiprovidershutdown-dofastshutdown.md) -Methode auf. An diesem Punkt sollten diese MAPI-Anbieter überprüfen, ob alle erforderlichen Aktionen, wie das Speichern von Daten und Einstellungen, abgeschlossen sind, damit der MAPI-Client sofort alle Verweise und die Beendigung der Verbindung trennen kann. 
    
## <a name="see-also"></a>Siehe auch

- [Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)
- [Benutzeroptionen für das schnelle Herunterfahren](fast-shutdown-user-options.md)
- [Bewährte Methoden für das schnelle Herunterfahren](best-practices-for-fast-shutdown.md)

