---
title: Übersicht über schnelles Herunterfahren
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
# <a name="fast-shutdown-overview"></a>Übersicht über schnelles Herunterfahren

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Schnelles Herunterfahren ist ein Mechanismus für einen MAPI-Client, um ein schnelles Herunterfahren des Clientprozesses zu initiieren und alle Anbieter zu benachrichtigen, mit denen der Client über eine aktive MAPI-Sitzung verfügt, um Daten und Einstellungen zu speichern, bevor der Clientprozess beendet wird. In diesem Thema wird der grundlegende Mechanismus für schnelles Herunterfahren beschrieben. 

Ab Microsoft Outlook 2010 und jetzt einschließlich Microsoft Outlook 2013 bietet das MAPI-Subsystem die [IMAPIClientShutdown : IUnknown-Schnittstelle.](imapiclientshutdowniunknown.md) Outlook und andere MAPI-Clients können das schnelle Herunterfahren als Standardmechanismus zum Beenden des Clientprozesses verwenden. Eine Einstellung auf Benutzerebene in der Windows des Clientcomputers steuert die Einführung des schnellen Herunterfahrens für alle MAPI-Clients für den Benutzer auf diesem Computer. Weitere Informationen zu den Registrierungseinstellungen finden Sie unter [Fast Shutdown User Options](fast-shutdown-user-options.md).
  
Wenn ein MAPI-Client das schnelle Herunterfahren übernehmen muss, muss er die **IMAPIClientShutdown : IUnknown-Schnittstelle** verwenden. Im Folgenden finden Sie den typischen Verlauf von Ereignissen, wenn der Client versucht, das System heruntergefahren zu werden: 
  
1. Der MAPI-Client initiiert das Herunterfahren, indem die [IMAPIClientShutdown::QueryFastShutdown-Methode](imapiclientshutdown-queryfastshutdown.md) aufgerufen wird, um zu ermitteln, ob das MAPI-Subsystem das schnelle Herunterfahren unterstützt. 
    
2. Das MAPI-Subsystem antwortet mit der verfügbaren Unterstützung für schnelles Herunterfahren auf den **IMAPIClientShutdown::QueryFastShutdown-Aufruf** des Clients mithilfe des folgenden Verfahrens: 
    
    1. Das MAPI-Subsystem ruft die [IMAPIProviderShutdown::QueryFastShutdown-Methode](imapiprovidershutdown-queryfastshutdown.md) für jeden MAPI-Anbieter auf, mit dem der MAPI-Clientprozess über eine aktive MAPI-Sitzung verfügt, wenn der Anbieter die [IMAPIProviderShutdown : IUnknown-Schnittstelle](imapiprovidershutdowniunknown.md) implementiert hat. 
        
       > [!NOTE]
       >  Das MAPI-Subsystem fragt und benachrichtigt MAPI-Anbieter immer über die **IMAPIProviderShutdown : IUnknown-Schnittstelle** innerhalb jeder MAPI-Sitzung in der folgenden Reihenfolge:
       > 1. Transportanbieter
       > 2. Adressbuchanbieter
       > 3. Store Anbieter 
    
    2. Abhängig von der Registrierungseinstellung für das schnelle Herunterfahren für diesen Benutzer auf dem Clientcomputer gibt das MAPI-Subsystem den entsprechenden Rückgabecode an **IMAPIClientShutdown::QueryFastShutdown an.** Der Rückgabecode wird entweder S_OK oder MAPI_E_NO_SUPPORT.
        
    3. Der MAPI-Client ruft die [IMAPIClientShutdown::NotifyProcessShutdown-Methode](imapiclientshutdown-notifyprocessshutdown.md) auf, um dem MAPI-Subsystem die Absicht zum Herunterfahren anzuzeigen. 
        
    4. Das MAPI-Subsystem gibt jedem geladenen MAPI-Anbieter an, dass der MAPI-Client heruntergefahren wird. Für anbieter, die die **IMAPIProviderShutdown : IUnknown-Schnittstelle** implementiert haben, ruft das MAPI-Subsystem die entsprechende [IMAPIProviderShutdown::NotifyProcessShutdown-Methode](imapiprovidershutdown-notifyprocessshutdown.md) auf. 
        
    5. Der MAPI-Client ruft die [IMAPIClientShutdown::D oFastShutdown-Methode](imapiclientshutdown-dofastshutdown.md) auf, um dem MAPI-Subsystem anzugeben, dass der Clientprozess sofort beendet wird. 
        
    6. Das MAPI-Subsystem gibt jedem geladenen MAPI-Anbieter an, dass der MAPI-Clientprozess beendet wird. Für anbieter, die die **IMAPIProviderShutdown : IUnknown-Schnittstelle** implementiert haben, ruft das MAPI-Subsystem die entsprechende [IMAPIProviderShutdown::D oFastShutdown-Methode](imapiprovidershutdown-dofastshutdown.md) auf. An diesem Punkt sollten diese MAPI-Anbieter überprüfen, ob alle erforderlichen Aktionen, z. B. das Speichern von Daten und Einstellungen, abgeschlossen sind, damit der MAPI-Client sofort alle Verweise trennen und beenden kann. 
    
## <a name="see-also"></a>Siehe auch

- [Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)
- [Benutzeroptionen für schnelles Herunterfahren](fast-shutdown-user-options.md)
- [Bewährte Methoden für das schnelle Herunterfahren](best-practices-for-fast-shutdown.md)

