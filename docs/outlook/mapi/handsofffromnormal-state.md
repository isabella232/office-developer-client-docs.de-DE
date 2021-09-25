---
title: HandsOffFromNormal-Zustand
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 45374bfbead9f8f94967149c1f418cf77aa9ebd3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561726"
---
# <a name="handsofffromnormal-state"></a>HandsOffFromNormal-Zustand

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der HandsOffFromNormal-Zustand ist dem [HandsOffAfterSave-Zustand](handsoffaftersave-state.md) sehr ähnlich. Es ist Teil des Prozesses zum Speichern des Inhalts eines Formulars in einem dauerhaften Speicher. In diesem Zustand sollte das Formularobjekt keine Änderungen an den speicherinternen Kopien der Werte der Nachrichteneigenschaften vornehmen, da es möglicherweise keine andere Möglichkeit zum Speichern dieser Änderungen gibt. In der folgenden Tabelle werden zulässige Übergänge aus dem HandsOffFromNormal-Zustand beschrieben. 
  
|IPersistMessage**-Methode**|**Aktion**|**Neuer Zustand**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)  <br/> |Ersetzen Sie die Nachricht des Nachrichtenobjekts durch  _pMessage_. Dies ist der Ersatz für die Nachricht, die durch den vorherigen Aufruf von [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)widerrufen wurde. Die Daten in der neuen Nachricht sind garantiert die gleichen wie in der widerrufenen Nachricht. Die Nachricht sollte weder als sauber gekennzeichnet werden, noch sollte [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) nach diesem Aufruf aufgerufen werden. Wenn der **SaveCompleted-Aufruf** erfolgreich ist, geben Sie den Status ["Normal"](normal-state.md) ein. Andernfalls verbleiben Sie im HandsOffFromNormal-Zustand.  <br/> |Normal oder HandsOffFromNormal  <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)  <br/> |Legen Sie den letzten Fehler auf E_UNEXPECTED fest.  <br/> |HandsOffFromNormal  <br/> |
|**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md)oder [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Legen Sie den letzten Fehler auf E_UNEXPECTED fest.  <br/> |HandsOffFromNormal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Gibt den letzten Fehler zurück.  <br/> |HandsOffFromNormal  <br/> |
|Andere [IPersistMessage: IUnknown-Methoden](ipersistmessageiunknown.md) oder -Methoden aus anderen Schnittstellen  <br/> |Legen Sie den letzten Fehler auf E_UNEXPECTED fest.  <br/> |HandsOffFromNormal  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Formularstatus](form-states.md)

