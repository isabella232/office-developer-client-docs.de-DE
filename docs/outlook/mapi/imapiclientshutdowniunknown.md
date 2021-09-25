---
title: IMAPIClientShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIClientShutdown
api_type:
- COM
ms.assetid: b6a5096f-ad27-48b3-b569-f33efc20fa72
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8243ab5a342c402946812a61ca199af0d17803b5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567613"
---
# <a name="imapiclientshutdown--iunknown"></a>IMAPIClientShutdown : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht einem MAPI-Client das schnelle Herunterfahren des Clientprozesses. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |[IMAPISession-Objekt](imapisessioniunknown.md)  <br/> |
|Implementiert von:  <br/> |MAPI-Subsystem  <br/> |
|Aufgerufen von:  <br/> |MAPI-Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIClientShutdown  <br/> |
|Zeigertyp:  <br/> |LPMAPICLIENTSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) <br/> |Fragt das MAPI-Subsystem auf Unterstützung für schnelles Herunterfahren ab, die von geladenen MAPI-Anbietern bereitgestellt wird.  <br/> |
|[NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) <br/> |Gibt die Absicht des MAPI-Clients an, mit dem Herunterfahren fortzufahren.  <br/> |
|[DoFastShutdown](imapiclientshutdown-dofastshutdown.md) <br/> |Gibt die Absicht des MAPI-Clients an, den Clientprozess sofort zu beenden.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Zweck des schnellen Herunterfahrens besteht darin, einem MAPI-Client und jedem geladenen MAPI-Anbieter, mit dem der MAPI-Client über eine aktive MAPI-Sitzung verfügt, das Speichern von MAPI-Einstellungen und -Daten zu ermöglichen. Dadurch kann der MAPI-Client alle externen Verweise trennen und beenden, ohne datenverlust zu verursachen. Ein MAPI-Client, der schnelles Herunterfahren ausführen muss, muss die **IMAPIClientShutdown-Schnittstelle** verwenden. Der MAPI-Client kann einen Zeiger auf diese Schnittstelle abrufen, indem er die IUnknown::QueryInterface-Methode für jedes [IMAPISession-Objekt aufruft.](imapisessioniunknown.md) 
  
Ein MAPI-Client initiiert immer ein schnelles Herunterfahren, indem die **IMAPIClientShutdown::QueryFastShutdown-Methode** aufgerufen wird. Das MAPI-Subsystem antwortet auf die Abfrage des MAPI-Clients, indem überprüft wird, ob geladene MAPI-Anbieter das schnelle Herunterfahren des Clients unterstützen. Der Administrator kann Windows Registrierungseinstellungen verwenden, um die Ebene der Anbieterunterstützung zu ermitteln, die erforderlich ist, damit MAPI-Clients mit schnellem Herunterfahren fortfahren können. Weitere Informationen finden Sie unter ["Benutzeroptionen für schnelles Herunterfahren".](fast-shutdown-user-options.md)
  
Um mit dem schnellen Herunterfahren fortzufahren, ruft der Client die **IMAPIClientShutdown::NotifyProcessShutdown-Methode** auf, um dem MAPI-Subsystem anzugeben, dass heruntergefahren werden soll. Der Client ruft dann die **IMAPIClientShutdown::D oFastShutdown-Methode** auf, um anzugeben, dass der Clientprozess sofort beendet wird. 
  
Weitere Informationen zum schnellen Herunterfahren finden Sie unter ["Übersicht über schnelles Herunterfahren".](fast-shutdown-overview.md) Informationen zum erfolgreichen schnellen Herunterfahren finden Sie unter ["Bewährte Methoden für schnelles Herunterfahren".](best-practices-for-fast-shutdown.md)
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)
  
[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

