---
title: IMAPIProviderShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProviderShutdown
api_type:
- COM
ms.assetid: fd86c8a5-f251-46c3-ace9-515e94e504ac
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5fa47b972be4ed58de052757545d505381e78cbd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625537"
---
# <a name="imapiprovidershutdown--iunknown"></a>IMAPIProviderShutdown : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht es dem MAPI-Subsystem, einen MAPI-Anbieter über das schnelle Herunterfahren eines MAPI-Clients zu informieren, damit der MAPI-Anbieter auf das Herunterfahren reagieren kann.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Provider-Objekte: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md)oder [IMSProvider](imsprovideriunknown.md) <br/> |
|Implementiert von:  <br/> |MAPI-Anbieter  <br/> |
|Aufgerufen von:  <br/> |MAPI-Subsystem  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIProviderShutdown  <br/> |
|Zeigertyp:  <br/> |LPMAPIPROVIDERSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) <br/> |Fragt den MAPI-Anbieter auf Unterstützung für schnelles Herunterfahren ab.  <br/> |
|[NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |Gibt dem MAPI-Anbieter an, dass ein MAPI-Client ein schnelles Herunterfahren durchführen wird, damit der Anbieter Maßnahmen ergreifen kann, um Datenverluste zu verhindern.  <br/> |
|[DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) <br/> |Gibt dem MAPI-Anbieter an, dass der MAPI-Client sofort beendet wird, sodass der MAPI-Anbieter Änderungen beibehalten wird, um Datenverluste zu verhindern.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Schnelles Herunterfahren ermöglicht es einem MAPI-Client, seinen Prozess innerhalb kurzer Zeit zu beenden, hoffentlich nachdem der Client und geladene MAPI-Anbieter MAPI-Einstellungen und -Daten gespeichert haben. Der MAPI-Client initiiert immer ein schnelles Herunterfahren und sollte das MAPI-Subsystem abfragen, um unterstützung für schnelles Herunterfahren von den geladenen MAPI-Anbietern zu erhalten. Ein Administrator kann die Windows Registrierung auf Benutzerebene festlegen, um die Ebene der Anbieterunterstützung anzugeben, die erforderlich ist, um das schnelle Herunterfahren aller MAPI-Clients zu ermöglichen. Weitere Informationen zu den Registrierungseinstellungen finden Sie unter ["Benutzeroptionen für schnelles Herunterfahren".](fast-shutdown-user-options.md) Damit das schnelle Herunterfahren jedoch ohne Datenverlust erfolgreich ausgeführt werden kann, sollten MAPI-Anbieter die **IMAPIProviderShutdown-Schnittstelle** implementieren. 
  
Ein MAPI-Anbieter, der schnelles Herunterfahren des Clients unterstützen muss, sollte S_OK an das MAPI-Subsystem in der **IMAPIProviderShutdown::QueryFastShutdown-Methode** zurückgeben. Wenn das MAPI-Subsystem anschließend die **METHODEN IMAPIProviderShutdown::NotifyProcessShutdown** und **IMAPIProviderShutdown::D oFastShutdown** aufruft, sollte der MAPI-Anbieter die erforderlichen Maßnahmen ergreifen, um MAPI-Einstellungen und -Daten zu speichern und sich auf das Beenden des Clients vorzubereiten. 
  
MAPI-Anbieter, die das schnelle Herunterfahren des Clients nicht unterstützen müssen, sollten weiterhin die **IMAPIProviderShutdown-Schnittstelle** implementieren und die **IMAPIProviderShutdown::QueryFastShutdown-Methode** MAPI_E_NO_SUPPORT zurückgeben lassen. Für Outlook als MAPI-Client führt dies dazu, dass Outlook warten, bis alle externen Verweise freigegeben werden, bevor sie beendet werden. 
  
Abhängig von der Windows Registrierungseinstellung des Benutzers für schnelles Herunterfahren verhindert die Nichtimplierung der **IMAPIProviderShutdown-Schnittstelle** nicht notwendigerweise ein schnelles Herunterfahren des Clients. 
  
Weitere Informationen zum Prozess des schnellen Herunterfahrens finden Sie unter ["Übersicht über schnelles Herunterfahren".](fast-shutdown-overview.md) Informationen zum erfolgreichen Schnellen Herunterfahren finden Sie unter ["Bewährte Methoden für schnelles Herunterfahren".](best-practices-for-fast-shutdown.md)
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)
  
[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

