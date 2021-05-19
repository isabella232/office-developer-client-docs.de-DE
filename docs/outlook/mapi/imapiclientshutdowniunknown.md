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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 279d6109e8c29de204c4fb58da51de84b4fbe183
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435334"
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
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) <br/> |Fragt das MAPI-Subsystem nach Unterstützung für schnelles Herunterfahren ab, die von geladenen MAPI-Anbietern bereitgestellt wird.  <br/> |
|[NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) <br/> |Gibt die Absicht des MAPI-Clients an, mit dem Herunterfahren fortzufahren.  <br/> |
|[DoFastShutdown](imapiclientshutdown-dofastshutdown.md) <br/> |Gibt die Absicht des MAPI-Clients an, den Clientprozess sofort zu beenden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Zweck des schnellen Herunterfahrens besteht im Zulassen eines MAPI-Clients und eines beliebigen geladenen MAPI-Anbieters, mit dem der MAPI-Client über eine aktive MAPI-Sitzung zum Speichern von MAPI-Einstellungen und -Daten verfügt. Dadurch kann der MAPI-Client alle externen Verweise trennen und beenden, ohne Datenverlust zu verursachen. Ein MAPI-Client, der schnelles Herunterfahren ausführen muss, muss die **IMAPIClientShutdown-Schnittstelle** verwenden. Der MAPI-Client kann einen Zeiger auf diese Schnittstelle abrufen, indem er die IUnknown::QueryInterface-Methode für jedes [IMAPISession-Objekt](imapisessioniunknown.md) aufruft. 
  
Ein MAPI-Client initiiert immer ein schnelles Herunterfahren, indem die **IMAPIClientShutdown::QueryFastShutdown-Methode aufgerufen** wird. Das MAPI-Subsystem antwortet auf die Abfrage des MAPI-Clients, indem es überprüft, ob geladene MAPI-Anbieter das schnelle Herunterfahren des Clients unterstützen. Der Administrator kann mithilfe Windows Registrierungseinstellungen bestimmen, welche Stufe der Anbieterunterstützung erforderlich ist, damit MAPI-Clients mit dem schnellen Herunterfahren fortfahren können. Weitere Informationen finden Sie unter [Fast Shutdown User Options](fast-shutdown-user-options.md).
  
Um mit dem schnellen Herunterfahren fortzufahren, ruft der Client die **IMAPIClientShutdown::NotifyProcessShutdown-Methode** auf, um dem MAPI-Subsystem die Absicht zum Herunterfahren anzuzeigen. Der Client ruft dann die **IMAPIClientShutdown::D oFastShutdown-Methode** auf, um anzugeben, dass der Clientprozess sofort beendet wird. 
  
Weitere Informationen zum schnellen Herunterfahren finden Sie unter [Fast Shutdown Overview](fast-shutdown-overview.md). Informationen zum erfolgreichen Schnellen Herunterfahren finden Sie unter [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)
  
[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

