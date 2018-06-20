---
title: IMAPIClientShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown
api_type:
- COM
ms.assetid: b6a5096f-ad27-48b3-b569-f33efc20fa72
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e68211049bc0f958ae24975f4ab4063953eef567
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792087"
---
# <a name="imapiclientshutdown--iunknown"></a>IMAPIClientShutdown: IUnknown

  
  
**Betrifft**: Outlook 
  
Ermöglicht einen MAPI-Client, um das schnelle Herunterfahren des Clientprozesses auszuführen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |[IMAPISession](imapisessioniunknown.md) -Objekt  <br/> |
|Implementiert von:  <br/> |MAPI-Subsystems  <br/> |
|Aufgerufen von:  <br/> |MAPI-client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIClientShutdown  <br/> |
|Zeigertyp:  <br/> |LPMAPICLIENTSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) <br/> |Abfragen des MAPI-Subsystems für Schnelles Herunterfahren unterstützt, die von geladenen MAPI-Anbieter bereitgestellt wird.  <br/> |
|[NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) <br/> |Gibt an, fahren Sie der Zweck der MAPI-Client, fortsetzen.  <br/> |
|[DoFastShutdown](imapiclientshutdown-dofastshutdown.md) <br/> |Gibt an, dass der MAPI-Client der Client sofort zu beenden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Schnelles Herunterfahren dient, dass ein MAPI-Client und alle geladenen MAPI-Anbieter mit dem der MAPI-Client eine aktive MAPI-Sitzung MAPI-Einstellungen und Daten gespeichert wurde. Auf diese Weise können den MAPI-Client, trennen alle externen Verweise und zu beenden, ohne Datenverlust verursacht. Ein MAPI-Client, der muss Schnelles Herunterfahren ausführen, muss die **IMAPIClientShutdown** -Schnittstelle verwenden. Der MAPI-Client kann einen Zeiger auf diese Schnittstelle abrufen, durch die QueryInterface-Methode für jedes Objekt [IMAPISession](imapisessioniunknown.md) aufrufen. 
  
Ein MAPI-Client wird stets ein Schnelles Herunterfahren durch Aufrufen der Methode **IMAPIClientShutdown::QueryFastShutdown** initiiert. MAPI-Subsystems reagiert auf die MAPI-Client-Abfrage, indem Sie überprüfen, ob die geladene MAPI-Anbieter Schnelles Herunterfahren des Clients unterstützen. Der Administrator kann Einstellungen der Windows-Registrierung verwenden, um die Ebene der anbieterunterstützung zu ermitteln, die für MAPI-Clients zu Schnelles Herunterfahren fortsetzen erforderlich ist. Weitere Informationen finden Sie unter [Fast Herunterfahren Benutzeroptionen](fast-shutdown-user-options.md).
  
Um Schnelles Herunterfahren fortzusetzen, ruft der Client die **IMAPIClientShutdown::NotifyProcessShutdown** -Methode, um die Absicht Herunterfahren des MAPI-Subsystems anzuzeigen. Der Client ruft dann die **IMAPIClientShutdown::DoFastShutdown** -Methode, um darauf hinzuweisen, dass der Clientprozess sofort beendet wird. 
  
Weitere Informationen zu Schnelles Herunterfahren finden Sie unter [Übersicht über die schnelle Herunterfahren](fast-shutdown-overview.md). Informationen über das Schnelles Herunterfahren erfolgreich ausführen finden Sie unter [Bewährte Methoden für das schnelle Herunterfahren](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)
  
[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

