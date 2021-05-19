---
title: HandsOffFromNormal-Status
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 17fa0f3d4e74ce7d717a94378880f2cc46150fc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426471"
---
# <a name="handsofffromnormal-state"></a>HandsOffFromNormal-Status

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Status HandsOffFromNormal ist dem Status [HandsOffAfterSave sehr](handsoffaftersave-state.md) ähnlich. Es ist Teil des Prozesses zum Speichern des Inhalts eines Formulars in einem dauerhaften Speicher. In diesem Zustand sollte das Formularobjekt keine Änderungen an den Speicherkopien der Werte der Eigenschaften der Nachricht vornehmen, da es möglicherweise keine weitere Möglichkeit gibt, diese Änderungen zu speichern. In der folgenden Tabelle werden zulässige Übergänge vom Status HandsOffFromNormal beschrieben. 
  
|IPersistMessage**-Methode**|**Action**|**Neuer Status**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)  <br/> |Ersetzen Sie die Nachricht des Nachrichtenobjekts durch  _pMessage_. Dies ist der Ersatz für die Nachricht, die durch den vorherigen Aufruf von [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)widerrufen wurde. Die Daten in der neuen Nachricht sind garantiert dieselben wie in der widerrufenen Nachricht. Die Nachricht sollte nicht als "clean" gekennzeichnet werden, und nach diesem Aufruf sollte [auch nicht IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) aufgerufen werden. Wenn der **SaveCompleted-Aufruf** erfolgreich ist, geben Sie den Status [Normal](normal-state.md) ein. Bleiben Sie andernfalls im Status HandsOffFromNormal.  <br/> |Normal oder HandsOffFromNormal  <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)  <br/> |Legen Sie den letzten Fehler auf E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
|**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md)oder [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Legen Sie den letzten Fehler auf E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Gibt den letzten Fehler zurück.  <br/> |HandsOffFromNormal  <br/> |
|Andere [IPersistMessage : IUnknown-Methoden](ipersistmessageiunknown.md) oder -Methoden aus anderen Schnittstellen  <br/> |Legen Sie den letzten Fehler auf E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Formularzustände](form-states.md)

