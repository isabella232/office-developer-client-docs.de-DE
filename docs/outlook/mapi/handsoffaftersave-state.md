---
title: HandsOffAfterSave-Status
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 85630965c7e78e6fa76e348bfe98cc9060665057
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406605"
---
# <a name="handsoffaftersave-state"></a>HandsOffAfterSave-Status

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Status HandsOffAfterSave ist Teil des Prozesses zum Speichern des Inhalts eines Formulars im permanenten Speicher. In diesem Zustand sollte das Formularobjekt keine Änderungen an den Speicherkopien der Werte der Eigenschaften der Nachricht vornehmen, da es möglicherweise keine weitere Möglichkeit gibt, diese Änderungen zu speichern. In der folgenden Tabelle werden zulässige Übergänge vom Status HandsOffAfterSave beschrieben.
  
|**IPersistMessage-Methode**|**Action**|**Neuer Status**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)  <br/> |Öffnen Sie alle eingebetteten Objekte. Die Daten in der in _pMessage_ gespeicherten Nachricht sind garantiert identisch mit der Nachricht im vorherigen [IPersistMessage::Save-Aufruf.](ipersistmessage-save.md) Wenn der **SaveCompleted-Aufruf** erfolgreich ist, geben Sie den Status Normal ein. Legen Sie andernfalls den letzten Fehler auf E_OUTOFMEMORY und bleiben Sie im Status HandsOffAfterSave.  <br/> |[Normal](normal-state.md) oder HandsOffAfterSave  <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)  <br/> |Legen Sie den letzten Fehler auf E_INVALIDARG oder E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save** oder [IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Legen Sie den letzten Fehler auf und geben E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Laden Sie das Formularobjekt mit Daten aus der Zielnachricht. Dieser Aufruf kann auftreten, wenn das Formularobjekt zur nächsten oder vorherigen Nachricht in einem Ordner geht.  <br/> |Standard  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Gibt den letzten Fehler zurück.  <br/> |HandsOffAfterSave  <br/> |
|Andere [IPersistMessage : IUnknown-Methoden](ipersistmessageiunknown.md) oder -Methoden aus anderen Schnittstellen  <br/> |Legen Sie den letzten Fehler auf und geben E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Formularzustände](form-states.md)

