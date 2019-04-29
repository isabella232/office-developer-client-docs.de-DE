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
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Verf�gbar gemacht von:  <br/> |[IMAPISession](imapisessioniunknown.md) -Objekt  <br/> |
|Implementiert von:  <br/> |MAPI-Subsystem  <br/> |
|Aufgerufen von:  <br/> |MAPI-Client  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIClientShutdown  <br/> |
|Zeigertyp:  <br/> |LPMAPICLIENTSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) <br/> |Fragt das MAPI-Subsystem zur Unterstützung des schnellen Herunterfahrens ab, das von geladenen MAPI-Anbietern bereitgestellt wird.  <br/> |
|[NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) <br/> |Gibt an, dass der MAPI-Client mit dem Herunterfahren fortfahren soll.  <br/> |
|[DoFastShutdown](imapiclientshutdown-dofastshutdown.md) <br/> |Gibt an, dass der MAPI-Client sofort den Clientprozess beenden soll.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Zweck des schnellen Herunterfahrens besteht darin, einem MAPI-Client und einem beliebigen geladenen MAPI-Anbieter, mit dem der MAPI-Client über eine aktive MAPI-Sitzung verfügt, die MAPI-Einstellungen und-Daten zu speichern. Dadurch kann der MAPI-Client alle externen Verweise trennen und beenden, ohne Datenverluste zu verursachen. Ein MAPI-Client, der Schnelles Herunterfahren durchführen muss, muss die **IMAPIClientShutdown** -Schnittstelle verwenden. Der MAPI-Client kann einen Zeiger auf diese Schnittstelle abrufen, indem er die IUnknown:: QueryInterface-Methode für ein beliebiges [IMAPISession](imapisessioniunknown.md) -Objekt aufruft. 
  
Ein MAPI-Client initiiert immer ein schnelles Herunterfahren durch Aufrufen der **IMAPIClientShutdown:: QueryFastShutdown** -Methode. Das MAPI-Subsystem antwortet auf die Abfrage des MAPI-Clients, indem überprüft wird, ob geladene MAPI-Anbieter das schnelle Herunterfahren des Clients unterstützen. Der Administrator kann mithilfe der Windows-Registrierungseinstellungen die Ebene der Anbieterunterstützung ermitteln, die für MAPI-Clients erforderlich ist, um das schnelle Herunterfahren zu ermöglichen. Weitere Informationen finden Sie unter [Benutzeroptionen für das schnelle Herunterfahren](fast-shutdown-user-options.md).
  
Um mit dem schnellen Herunterfahren fortzufahren, ruft der Client die **IMAPIClientShutdown:: NotifyProcessShutdown** -Methode auf, um dem MAPI-Subsystem anzuzeigen, dass das Herunterfahren beabsichtigt ist. Der Client ruft dann die **IMAPIClientShutdown::D ofastshutdown** -Methode auf, um anzugeben, dass der Clientprozess sofort beendet wird. 
  
Weitere Informationen zum schnellen Herunterfahren finden Sie unter [Übersicht über Schnelles Herunterfahren](fast-shutdown-overview.md). Informationen dazu, wie Sie das schnelle Herunterfahren erfolgreich durchführen können, finden Sie unter [bewährte Methoden für das schnelle Herunterfahren](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)
  
[Herunterfahren von Clients in MAPI](client-shutdown-in-mapi.md)

