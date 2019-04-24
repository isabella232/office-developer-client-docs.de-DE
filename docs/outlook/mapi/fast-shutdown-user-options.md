---
title: Benutzeroptionen für das schnelle Herunterfahren
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 220aeab5-20f6-4520-96c9-8aaa0e8ea15b
description: 'Letzte Änderung: 26. Juni 2012'
localization_priority: Priority
ms.openlocfilehash: 3c60862733c6b38e60650ae9daba9bba578fcd58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341076"
---
# <a name="fast-shutdown-user-options"></a>Benutzeroptionen für das schnelle Herunterfahren

**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Thema werden die drei Windows-Registrierungseinstellungen beschrieben, die ab Microsoft Outlook 2010 und jetzt bis einschließlich Microsoft Outlook 2013 für das schnelle Herunterfahren von MAPI-Clients eines Benutzers verfügbar sind. Administratoren können mithilfe dieser Registrierungseinstellungen das bevorzugte Clientverhalten beim Herunterfahren abhängig von der vom MAPI-Anbieter angebotenen Unterstützung für das schnelle Herunterfahren des Clients angeben. Die Einstellung des Administrators bestimmt wiederum, wie das MAPI-Subsystem auf den Aufruf des MAPI-Clients von [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) in Bezug auf die verfügbare Unterstützung für schnelles Herunterfahren reagiert. 
  
Eine Registrierungseinstellung spiegelt zwar die bevorzugte Einstellung des Administrators für das schnelle Herunterfahren aller MAPI-Clients auf Benutzerebene wider, ein MAPI-Cliententwickler kann jedoch entscheiden, ob der Client schnelles Herunterfahren unabhängig von anderen MAPI-Clients und der Registrierungseinstellung des Administrators unterstützen soll. Aber damit das schnelle Herunterfahren erfolgreich ausgeführt wird, muss der Benutzer die erforderliche Registrierungseinstellung festgelegt haben, ein MAPI-Client muss das schnelle Herunterfahren mithilfe der Schnittstelle [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) initiieren, und MAPI-Anbieter, die mit dem Client arbeiten, müssen die Schnittstelle [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) implementieren, um das schnelle Herunterfahren des Clients zu unterstützen. 
  
In der folgenden Liste sind diese drei Optionen auf Benutzerebene beschrieben.
  
### <a name="option-1-the-mapi-subsystem-enables-fast-shutdown-unless-mapi-providers-explicitly-opt-out"></a>Option 1: Das MAPI-Subsystem ermöglicht schnelles Herunterfahren, sofern die MAPI-Anbieter dies nicht explizit deaktivieren 
    
Ab Outlook 2010 handelt es sich dabei um das Standardverhalten, wenn Outlook der MAPI-Client ist. Bei anderen MAPI-Clients stellt das nicht unbedingt das Standardverhalten dar. Um diese Option für Outlook explizit anzugeben, können Administratoren den folgenden Registrierungsschlüssel und -wert festlegen.
    
Registrierungsschlüssel:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Wert:
  
>  `"FastShutdownBehavior"=dword:00000000`
    
Wenn ein MAPI-Client schnelles Herunterfahren initiiert und **IMAPIClientShutdown::QueryFastShutdown** aufruft, um Unterstützung für schnelles Herunterfahren abzufragen, antwortet das MAPI-Subsystem auf die Abfrage mit der Rückgabe von S\_OK, sofern kein MAPI-Anbieter, der über eine aktive MAPI-Sitzung mit dem MAPI-Client verfügt, die Unterstützung für schnelles Herunterfahren explizit deaktiviert hat. 

Ein MAPI-Anbieter deaktiviert schnelles Herunterfahren, indem er die Methode [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) zur Rückgabe eines Fehlers (MAPI\_E\_NO\_SUPPORT) implementiert. Wenn ein oder mehrere MAPI-Anbieter einen Fehler in **IMAPIProviderShutdown::QueryFastShutdown** zurückgeben, gibt das MAPI-Subsystem MAPI_\E_\NO\_SUPPORT an **IMAPIClientShutdown::QueryFastShutdown** zurück. 

Sofern ein MAPI-Anbieter die Option nicht deaktiviert, gibt das MAPI-Subsystem S\_OK zurück, auch wenn ein oder mehrere Anbieter die Schnittstelle **IMAPIProviderShutdown : IUnknown** nicht implementiert haben. 
    
### <a name="option-2-the-mapi-subsystem-enables-fast-shutdown-only-if-every-mapi-provider-explicitly-opts-in"></a>Option 2: Das MAPI-Subsystem ermöglicht schnelles Herunterfahren nur, wenn jeder MAPI-Anbieter dies explizit aktiviert 
    
Administratoren müssen den folgenden Registrierungsschlüssel und -wert explizit festlegen, um diese Einstellung für das schnelle Herunterfahren des Clients anzugeben.
    
Registrierungsschlüssel:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Wert:
  
>  `"FastShutdownBehavior"=dword:00000001`
    
Wenn ein MAPI-Client schnelles Herunterfahren initiiert und **IMAPIClientShutdown::QueryFastShutdown** aufruft, um Unterstützung für schnelles Herunterfahren abzufragen, antwortet das MAPI-Subsystem auf die Abfrage mit der Rückgabe von S\_OK, wenn alle MAPI-Anbieter, die über aktive Sitzungen mit dem MAPI-Client verfügen, schnelles Herunterfahren unterstützen. Ein MAPI-Anbieter demonstriert seine Unterstützung, indem er **IMAPIProviderShutdown::QueryFastShutdown** zur Rückgabe eines Nicht-Fehlercodes (S\_OK) implementiert. 

Wenn ein oder mehrere MAPI-Anbieter MAPI\_E\_NO\_SUPPORT zurückgeben oder **IMAPIProviderShutdown::QueryFastShutdown** nicht implementieren, gibt das MAPI-Subsystem einen Fehlercode an **IMAPIClientShutdown::QueryFastShutdown** zurück.
    
### <a name="option-3-an-administrator-disables-support-for-client-fast-shutdown"></a>Option 3: Ein Administrator deaktiviert die Unterstützung für das schnelle Herunterfahren des Clients
    
Administratoren müssen den folgenden Registrierungsschlüssel und -wert explizit festlegen, um die Unterstützung für das schnelle Herunterfahren des Clients zu deaktivieren.
    
Registrierungsschlüssel:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
Wert:
  
>  `"FastShutdownBehavior"=dword:00000002`
    
Wenn ein MAPI-Client schnelles Herunterfahren initiiert und **IMAPIClientShutdown::QueryFastShutdown** aufruft, um Unterstützung für schnelles Herunterfahren abzufragen, antwortet das MAPI-Subsystem auf die Abfrage mit der Rückgabe von MAPI_E_NO_SUPPORT, und zwar unabhängig davon, ob die MAPI-Anbieter schnelles Herunterfahren unterstützen. Bei dieser Registrierungseinstellung ruft das MAPI-Subsystem niemals die Methode **IMAPIProviderShutdown::QueryFastShutdown** oder [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) eines Anbieters auf. 
    
## <a name="see-also"></a>Siehe auch

- [Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)
- [Übersicht über das schnelle Herunterfahren](fast-shutdown-overview.md)
- [Bewährte Methoden für das schnelle Herunterfahren](best-practices-for-fast-shutdown.md)

