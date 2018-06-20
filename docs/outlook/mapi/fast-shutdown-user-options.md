---
title: Schnelles Herunterfahren Benutzeroptionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 220aeab5-20f6-4520-96c9-8aaa0e8ea15b
description: 'Zuletzt geändert: 26 Juni 2012'
ms.openlocfilehash: a58f8b98ab2f5a5c1028440676a561427272d028
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791654"
---
# <a name="fast-shutdown-user-options"></a>Schnelles Herunterfahren Benutzeroptionen

**Betrifft**: Outlook 
  
In diesem Thema werden die drei Windows-registrierungseinstellungen, die verfügbar sind, beginnend in Microsoft Outlook 2010 und jetzt einschließlich Microsoft Outlook 2013 für Schnelles Herunterfahren von MAPI-Clients des Benutzers. Administratoren können diese Registrierungseinträge verwenden, um das bevorzugte Client Herunterfahren Verhalten je nach der MAPI-Anbieter Unterstützung für schnelle Herunterfahren von Clients anzugeben. Des Administrators festlegen, wiederum bestimmt, wie das MAPI-Subsystem Aufruf [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) im Hinblick auf die verfügbaren Schnelles Herunterfahren Unterstützung der MAPI-Client reagiert. 
  
Obwohl eine Einstellung in der Registrierung des Administrators Voreinstellung auf Benutzerebene für Schnelles Herunterfahren für alle MAPI-Clients wiedergibt, kann ein MAPI-Client-Entwickler entscheiden Sie, ob der Client Schnelles Herunterfahren unabhängig von anderen MAPI-Clients unterstützt und die registrierungseinstellung des Administrators. Dennoch für Schnelles Herunterfahren erfolgreich, stattfinden muss der Benutzer die Einstellung der erforderlichen Registrierung verfügen, die ein MAPI-Client muss das schnelle Herunterfahren initiiert werden mithilfe der [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md) Schnittstelle und MAPI-Anbieter, die Arbeit mit der Client sollte Implementieren der [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) -Schnittstelle für das schnelle Herunterfahren von Clients unterstützen. 
  
In der folgenden Liste werden die drei Optionen auf Benutzerebene beschrieben.
  
### <a name="option-1-the-mapi-subsystem-enables-fast-shutdown-unless-mapi-providers-explicitly-opt-out"></a>Option 1: Ermöglicht das MAPI-Subsystem Schnelles Herunterfahren, wenn MAPI-Anbieter explizit Aufheben der Bestätigung 
    
Starten in Outlook 2010, ist dies das Standardverhalten, wenn Outlook MAPI-Client ist; Es ist nicht unbedingt das Standardverhalten für andere MAPI-Clients. Wenn Sie diese Option für Outlook explizit angeben, können Administratoren auch den folgenden Registrierungsschlüssel und den Wert festzulegen.
    
Registrierungsschlüssel:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Wert:
  
>  `"FastShutdownBehavior"=dword:00000000`
    
Wenn ein MAPI-Client ein Schnelles Herunterfahren initiiert und **IMAPIClientShutdown::QueryFastShutdown** Abfrage für Schnelles Herunterfahren Support Ruft, antwortet des MAPI-Subsystems auf die Abfrage durch Rückgabe S\_solange keine MAPI-Anbieter, der eine aktive MAPI wurde auf OK Sitzung mit der MAPI-Client wurde nicht mehr unterstützt Schnelles Herunterfahren explizit bestätigt. 

Ein MAPI-Anbieter nicht genügend Schnelles Herunterfahren entscheidet, durch die Implementierung der [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) -Methode, um einen Fehler zurück (MAPI\_E\_NO\_Unterstützung). Wenn eine oder mehrere MAPI-Anbieter in **IMAPIProviderShutdown::QueryFastShutdown**einen Fehler zurück, gibt MAPI-Subsystems MAPI_\E_\NO\_SUPPORT zur **IMAPIClientShutdown::QueryFastShutdown**. 

Es sei denn, ein MAPI-Anbieter, die MAPI-Subsystems gibt S entscheidet\_auf OK, auch wenn eine oder mehrere Anbieter nicht implementiert haben die **IMAPIProviderShutdown: IUnknown** Schnittstelle. 
    
### <a name="option-2-the-mapi-subsystem-enables-fast-shutdown-only-if-every-mapi-provider-explicitly-opts-in"></a>Option 2: MAPI-Subsystems ermöglicht Schnelles Herunterfahren nur, wenn alle MAPI-Anbieter explizit in entscheidet 
    
Administratoren müssen die folgenden Registrierungsschlüssel und den Wert an, diese Einstellung für das schnelle Herunterfahren von Client explizit festlegen.
    
Registrierungsschlüssel:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Wert:
  
>  `"FastShutdownBehavior"=dword:00000001`
    
Wenn ein MAPI-Client ein Schnelles Herunterfahren initiiert und **IMAPIClientShutdown::QueryFastShutdown** Abfrage für Schnelles Herunterfahren Support Ruft, antwortet des MAPI-Subsystems auf die Abfrage durch Rückgabe S\_OK, wenn alle MAPI-Anbieter mit aktiver Sitzungen mit die MAPI-Client-Unterstützung Schnelles Herunterfahren. Ein MAPI-Anbieter veranschaulicht die Unterstützung durch die Implementierung von **IMAPIProviderShutdown::QueryFastShutdown** , um einen Fehlercode zurück (S\_OK). 

Wenn solche MAPI-Anbieter einen oder mehrere MAPI zurückgeben\_E\_NO\_SUPPORT, oder **IMAPIProviderShutdown::QueryFastShutdown**, nicht zu implementieren des MAPI-Subsystems gibt einen Fehlercode an **IMAPIClientShutdown::QueryFastShutdown** zurück. .
    
### <a name="option-3-an-administrator-disables-support-for-client-fast-shutdown"></a>Option 3: Administrator deaktiviert die Unterstützung für schnelle Herunterfahren von Clients
    
Administratoren müssen die folgenden Registrierungsschlüssel und Deaktivieren der Unterstützung für das schnelle Herunterfahren von Client-Wert explizit festlegen.
    
Registrierungsschlüssel:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Wert:
  
>  `"FastShutdownBehavior"=dword:00000002`
    
Wenn ein MAPI-Client ein Schnelles Herunterfahren initiiert und **IMAPIClientShutdown::QueryFastShutdown** Abfrage für Schnelles Herunterfahren Support Ruft, antwortet des MAPI-Subsystems auf die Abfrage durch Rückgabe MAPI_E_NO_SUPPORT, unabhängig davon, ob ein MAPI-Anbieter unterstützt die schnelle Herunterfahren. Bei dieser registrierungseinstellung ruft des MAPI-Subsystems nie die **IMAPIProviderShutdown::QueryFastShutdown** oder [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) -Methode der Anbieter. 
    
## <a name="see-also"></a>Siehe auch

- [Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)
- [Schnelles Herunterfahren (Übersicht)](fast-shutdown-overview.md)
- [Bewährte Methoden für das schnelle Herunterfahren](best-practices-for-fast-shutdown.md)

