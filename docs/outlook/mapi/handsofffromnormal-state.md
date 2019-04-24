---
title: Status "handsofffromnormal-Status
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 17fa0f3d4e74ce7d717a94378880f2cc46150fc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299468"
---
# <a name="handsofffromnormal-state"></a>Status "handsofffromnormal-Status

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Status "handsofffromnormal-Zustand ist dem [HandsOffAfterSave](handsoffaftersave-state.md) -Status sehr ähnlich. Sie ist Teil des Prozesses zum Speichern des Inhalts eines Formulars in einem permanenten Speicher. Wenn Sie in diesem Zustand sind, sollte das Form-Objekt keine Änderungen an den in-Memory-Kopien von Werten der Eigenschaften der Nachricht vornehmen, da es möglicherweise keine weitere Möglichkeit gibt, diese Änderungen zu speichern. In der folgenden Tabelle werden zulässige Übergänge vom Status "handsofffromnormal-Status beschrieben. 
  
|IPersistMessage * *-Methode * *|**Aktion**|**Neuer Status**|
|:-----|:-----|:-----|
|[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ null)  <br/> |Ersetzen Sie die Nachricht des Nachrichtenobjekts durch _pMessage_, wobei es sich um die Ersetzung der Nachricht handelt, die durch den vorherigen Aufruf von [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md)widerrufen wurde. Die Daten in der neuen Nachricht sind mit Sicherheit identisch mit der Nachricht. Die Nachricht sollte nicht als sauber gekennzeichnet werden, noch sollte [IMAPIViewAdviseSink::](imapiviewadvisesink-onsaved.md) onsaved nach diesem Aufruf aufgerufen werden. Wenn der **SaveCompleted** -Aufruf erfolgreich ist, geben Sie den [normalen](normal-state.md) Status ein. Andernfalls bleiben Sie im Status "handsofffromnormal-Zustand.  <br/> |Normal oder Status "handsofffromnormal  <br/> |
|**IPersistMessage:: SaveCompleted** (_pMessage = =_ null)  <br/> |Legen Sie den letzten Fehler auf E_UNEXPECTED.  <br/> |Status "handsofffromnormal  <br/> |
|**HandsOffMessage**, [IPersistMessage:: Save](ipersistmessage-save.md), [IPersistMessage:: InitNew](ipersistmessage-initnew.md)oder [IPersistMessage:: Laden](ipersistmessage-load.md) <br/> |Legen Sie den letzten Fehler auf E_UNEXPECTED.  <br/> |Status "handsofffromnormal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Zurückgeben des letzten Fehlers.  <br/> |Status "handsofffromnormal  <br/> |
|Andere [IPersistMessage: IUnknown](ipersistmessageiunknown.md) -Methoden oder Methoden von anderen Schnittstellen  <br/> |Legen Sie den letzten Fehler auf E_UNEXPECTED.  <br/> |Status "handsofffromnormal  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Formular Status](form-states.md)

