---
title: Übersicht über schnelles Herunterfahren
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a7830d73-427c-4f8b-86f4-51e040c142c3
description: 'Letzte Änderung: 26. Juni 2012'
ms.openlocfilehash: 49b14c6d627ed90f716eaa607b0e9421662c5ab7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567662"
---
# <a name="fast-shutdown-overview"></a>Übersicht über schnelles Herunterfahren

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Schnelles Herunterfahren ist ein Mechanismus für einen MAPI-Client, um ein schnelles Herunterfahren des Clientprozesses zu initiieren und alle Anbieter zu benachrichtigen, bei denen der Client über eine aktive MAPI-Sitzung verfügt, um Daten und Einstellungen zu speichern, bevor der Clientprozess beendet wird. In diesem Thema wird der grundlegende Mechanismus für schnelles Herunterfahren beschrieben. 

Ab Microsoft Outlook 2010 und jetzt einschließlich Microsoft Outlook 2013 stellt das MAPI-Subsystem die [IMAPIClientShutdown : IUnknown-Schnittstelle](imapiclientshutdowniunknown.md) bereit. Outlook und andere MAPI-Clients können schnelles Herunterfahren als Standardmechanismus zum Beenden des Clientprozesses verwenden. Eine Einstellung auf Benutzerebene in der Windows Registrierung des Clientcomputers steuert die Einführung des schnellen Herunterfahrens für alle MAPI-Clients für diesen Benutzer auf diesem Computer. Ausführliche Informationen zu den Registrierungseinstellungen finden Sie unter ["Benutzeroptionen für schnelles Herunterfahren".](fast-shutdown-user-options.md)
  
Wenn ein MAPI-Client schnelles Herunterfahren einführen muss, muss er die **IMAPIClientShutdown : IUnknown-Schnittstelle** verwenden. Es folgt der typische Ereignisverlauf, wenn der Client versucht, das Herunterfahren zu versuchen: 
  
1. Der MAPI-Client initiiert das Herunterfahren, indem er die [IMAPIClientShutdown::QueryFastShutdown-Methode](imapiclientshutdown-queryfastshutdown.md) aufruft, um zu bestimmen, ob das MAPI-Subsystem schnelles Herunterfahren unterstützt. 
    
2. Das MAPI-Subsystem reagiert mit der verfügbaren Unterstützung für schnelles Herunterfahren auf den **IMAPIClientShutdown::QueryFastShutdown-Aufruf** des Clients mithilfe des folgenden Verfahrens: 
    
    1. Das MAPI-Subsystem ruft die [IMAPIProviderShutdown::QueryFastShutdown-Methode](imapiprovidershutdown-queryfastshutdown.md) für jeden MAPI-Anbieter auf, mit dem der MAPI-Clientprozess über eine aktive MAPI-Sitzung verfügt, wenn der Anbieter die [IMAPIProviderShutdown : IUnknown-Schnittstelle](imapiprovidershutdowniunknown.md) implementiert hat. 
        
       > [!NOTE]
       >  Das MAPI-Subsystem fragt MAPI-Anbieter immer ab und benachrichtigt sie über die **IMAPIProviderShutdown : IUnknown-Schnittstelle** innerhalb jeder MAPI-Sitzung in der folgenden Reihenfolge:
       > 1. Transportanbieter
       > 2. Adressbuchanbieter
       > 3. Store Anbieter 
    
    2. Abhängig von der Registrierungseinstellung für schnelles Herunterfahren für diesen Benutzer auf dem Clientcomputer gibt das MAPI-Subsystem den entsprechenden Rückgabecode an **IMAPIClientShutdown::QueryFastShutdown** an. Der Rückgabecode ist entweder S_OK oder MAPI_E_NO_SUPPORT.
        
    3. Der MAPI-Client ruft die [IMAPIClientShutdown::NotifyProcessShutdown-Methode](imapiclientshutdown-notifyprocessshutdown.md) auf, um dem MAPI-Subsystem anzugeben, dass heruntergefahren werden soll. 
        
    4. Das MAPI-Subsystem gibt jedem geladenen MAPI-Anbieter an, dass der MAPI-Client heruntergefahren wird. Für Anbieter, die die **IMAPIProviderShutdown : IUnknown-Schnittstelle** implementiert haben, ruft das MAPI-Subsystem die entsprechende [IMAPIProviderShutdown::NotifyProcessShutdown-Methode](imapiprovidershutdown-notifyprocessshutdown.md) auf. 
        
    5. Der MAPI-Client ruft die [IMAPIClientShutdown::D oFastShutdown-Methode](imapiclientshutdown-dofastshutdown.md) auf, um dem MAPI-Subsystem anzugeben, dass der Clientprozess sofort beendet wird. 
        
    6. Das MAPI-Subsystem gibt jedem geladenen MAPI-Anbieter an, dass der MAPI-Clientprozess beendet wird. Für Anbieter, die die **IMAPIProviderShutdown : IUnknown-Schnittstelle** implementiert haben, ruft das MAPI-Subsystem die entsprechende [IMAPIProviderShutdown::D oFastShutdown-Methode](imapiprovidershutdown-dofastshutdown.md) auf. An diesem Punkt sollten diese MAPI-Anbieter überprüfen, ob alle erforderlichen Aktionen, z. B. das Speichern von Daten und Einstellungen, abgeschlossen sind, damit der MAPI-Client alle Verweise sofort trennt und beendet. 
    
## <a name="see-also"></a>Siehe auch

- [Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)
- [Benutzeroptionen für schnelles Herunterfahren](fast-shutdown-user-options.md)
- [Bewährte Methoden für das schnelle Herunterfahren](best-practices-for-fast-shutdown.md)

