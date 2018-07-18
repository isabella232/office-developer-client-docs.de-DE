---
title: IMAPIProviderShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown
api_type:
- COM
ms.assetid: fd86c8a5-f251-46c3-ace9-515e94e504ac
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a679d04f7697abbe0172105febf87082c0cd9946
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792327"
---
# <a name="imapiprovidershutdown--iunknown"></a>IMAPIProviderShutdown : IUnknown

  
  
**Betrifft**: Outlook 
  
Ermöglicht das MAPI-Subsystem, um einen MAPI-Anbieter für das schnelle Herunterfahren von einem MAPI-Client zu informieren, damit der MAPI-Anbieter auf das Herunterfahren reagieren kann.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Provider-Objekte: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md)oder [IMSProvider](imsprovideriunknown.md) <br/> |
|Implementiert von:  <br/> |MAPI-Anbieter  <br/> |
|Aufgerufen von:  <br/> |MAPI-Subsystems  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIProviderShutdown  <br/> |
|Zeigertyp:  <br/> |LPMAPIPROVIDERSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) <br/> |Abfragen der MAPI-Anbieter für Schnelles Herunterfahren unterstützen.  <br/> |
|[NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |Zeigt den MAPI-Anbieter, dass ein MAPI-Client ausführt, ein Schnelles Herunterfahren, so dass der Anbieter Aktionen, um Datenverlust zu vermeiden nutzen kann.  <br/> |
|[DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) <br/> |Gibt an, an den MAPI-Anbieter, dass der MAPI-Client sofort beendet wird, damit der MAPI-Anbieter ändert sich, um Datenverlust zu vermeiden beibehalten wird.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Schnelles Herunterfahren kann ein MAPI-Client seine in kurzer Zeit zu beenden, hoffentlich geladen, nachdem sich der Client und MAPI-Anbieter haben gespeichert MAPI-Einstellungen und Daten. Der MAPI-Client initiiert ein Schnelles Herunterfahren immer und sollte Abfragen des MAPI-Subsystems für Schnelles Herunterfahren Unterstützung von MAPI-Anbieter geladen. Ein Administrator kann die Windows-Registrierung können Sie die anbieterunterstützung angeben, die erforderlich sind, um das Schnelles Herunterfahren aller MAPI-Clients zulassen wird auf Benutzerebene festgelegt. Weitere Informationen zu den Einstellungen in der Registrierung finden Sie unter [Fast Herunterfahren Benutzeroptionen](fast-shutdown-user-options.md). Für schnelle Herunterfahren ohne Datenverlust erfolgreich ausgeführt wurde, sollte MAPI-Anbieter jedoch die **IMAPIProviderShutdown** -Schnittstelle implementieren. 
  
Ein MAPI-Anbieter, der schnelle Herunterfahren von Clients unterstützen muss, sollte zu MAPI-Subsystems in der **IMAPIProviderShutdown::QueryFastShutdown** -Methode S_OK zurück. Wenn MAPI-Subsystems anschließend die Methoden **IMAPIProviderShutdown::NotifyProcessShutdown** und **IMAPIProviderShutdown::DoFastShutdown** aufruft, dauert der MAPI-Anbieter erforderliche Aktionen für das MAPI-Einstellungen und Daten zu speichern und Vorbereiten der Client beenden. 
  
MAPI-Anbieter, die keine schnelle Herunterfahren von Clients unterstützen müssen sollten weiterhin die **IMAPIProviderShutdown** -Schnittstelle implementieren, und haben die **IMAPIProviderShutdown::QueryFastShutdown** -Methode MAPI_E_NO_SUPPORT zurückgeben. Für Outlook als MAPI-Client bewirkt, dass dieser Outlook warten, dass alle externen Verweise freigegeben werden muss, bevor sie beendet wird. 
  
Je nach Windows-Registrierung des Benutzers verhindert Einstellung für das schnelle Herunterfahren nicht implementieren der **IMAPIProviderShutdown** -Schnittstelle nicht unbedingt ein schnelle Herunterfahren von Clients. 
  
Weitere Informationen über den Prozess der Schnelles Herunterfahren finden Sie unter [Übersicht über die schnelle Herunterfahren](fast-shutdown-overview.md). Informationen dazu, wie Sie das schnelle Herunterfahren erfolgreich durchzuführen finden Sie unter [Bewährte Methoden für das schnelle Herunterfahren](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)
  
[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

