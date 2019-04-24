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
ms.openlocfilehash: 92067b5badfb2aab40f3b3735a164bc09321702c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322406"
---
# <a name="imapiprovidershutdown--iunknown"></a>IMAPIProviderShutdown : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht dem MAPI-Subsystem, einen MAPI-Anbieter über das schnelle Herunterfahren eines MAPI-Clients zu informieren, damit der MAPI-Anbieter auf das Herunterfahren reagieren kann.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Verf�gbar gemacht von:  <br/> |Anbieterobjekte: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md)oder [IMSProvider](imsprovideriunknown.md) <br/> |
|Implementiert von:  <br/> |MAPI-Anbieter  <br/> |
|Aufgerufen von:  <br/> |MAPI-Subsystem  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIProviderShutdown  <br/> |
|Zeigertyp:  <br/> |LPMAPIPROVIDERSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) <br/> |Fragt den MAPI-Anbieter ab, um das schnelle Herunterfahren zu unterstützen.  <br/> |
|[NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |Gibt dem MAPI-Anbieter an, dass ein MAPI-Client ein schnelles Herunterfahren durchführen soll, damit der Anbieter Maßnahmen ergreifen kann, um Datenverluste zu verhindern.  <br/> |
|[DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) <br/> |Gibt dem MAPI-Anbieter an, dass der MAPI-Client sofort beendet wird, sodass der MAPI-Anbieter Änderungen anhält, um Datenverluste zu vermeiden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das schnelle Herunterfahren ermöglicht es einem MAPI-Client, seinen Prozess innerhalb kurzer Zeit zu beenden, hoffentlich nachdem der Client und die geladenen MAPI-Anbieter MAPI-Einstellungen und-Daten gespeichert haben. Der MAPI-Client initiiert immer ein schnelles Herunterfahren und sollte das MAPI-Subsystem Abfragen, um die Unterstützung für das schnelle Herunterfahren von den geladenen MAPI-Anbietern zu erhalten. Ein Administrator kann die Windows-Registrierung auf Benutzerebene festlegen, um die Ebene der Anbieterunterstützung anzugeben, die erforderlich ist, um das schnelle Herunterfahren aller MAPI-Clients zu ermöglichen. Weitere Informationen zu den Registrierungseinstellungen finden Sie unter [Benutzeroptionen für das schnelle Herunterfahren](fast-shutdown-user-options.md). Damit jedoch das schnelle Herunterfahren ohne Datenverlust erfolgreich ausgeführt werden kann, sollten MAPI-Anbieter die **IMAPIProviderShutdown** -Schnittstelle implementieren. 
  
Ein MAPI-Anbieter, der das schnelle Herunterfahren des Clients unterstützen muss, sollte S_OK in der **IMAPIProviderShutdown:: QueryFastShutdown** -Methode an das MAPI-Subsystem zurückgeben. Wenn das MAPI-Subsystem anschließend die Methoden **IMAPIProviderShutdown:: NotifyProcessShutdown** und **IMAPIProviderShutdown::D ofastshutdown** aufruft, sollte der MAPI-Anbieter die erforderlichen Aktionen zum Speichern von MAPI-Einstellungen und-Daten ergreifen und bereiten Sie den Exit des Clients vor. 
  
MAPI-Anbieter, die das schnelle Herunterfahren des Clients nicht unterstützen müssen, sollten weiterhin die **IMAPIProviderShutdown** -Schnittstelle implementieren und die **IMAPIProviderShutdown:: QUERYFASTSHUTDOWN** -Methode MAPI_E_NO_SUPPORT zurückgeben. Für Outlook als MAPI-Client bewirkt dies, dass Outlook auf alle externen Verweise wartet, bevor es beendet wird. 
  
Abhängig von der Windows-Registrierungseinstellung des Benutzers für das schnelle Herunterfahren verhindert die Implementierung der **IMAPIProviderShutdown** -Schnittstelle nicht unbedingt, dass ein Client schnell heruntergefahren wird. 
  
Weitere Informationen zum Prozess des schnellen Herunterfahrens finden Sie unter [Übersicht über Schnelles Herunterfahren](fast-shutdown-overview.md). Weitere Informationen dazu, wie Sie das schnelle Herunterfahren erfolgreich ausführen können, finden Sie unter [bewährte Methoden für das schnelle Herunterfahren](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)
  
[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

