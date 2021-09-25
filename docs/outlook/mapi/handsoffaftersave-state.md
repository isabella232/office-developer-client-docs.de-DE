---
title: HandsOffAfterSave-Zustand
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e9027ab37fe5183847ee8181530f9adb1a8cddde
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551464"
---
# <a name="handsoffaftersave-state"></a>HandsOffAfterSave-Zustand

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der HandsOffAfterSave-Zustand ist Teil des Speicherns des Inhalts eines Formulars im permanenten Speicher. In diesem Zustand sollte das Formularobjekt keine Änderungen an den speicherinternen Kopien der Werte der Nachrichteneigenschaften vornehmen, da es möglicherweise keine andere Möglichkeit zum Speichern dieser Änderungen gibt. In der folgenden Tabelle werden zulässige Übergänge aus dem HandsOffAfterSave-Zustand beschrieben.
  
|**IPersistMessage-Methode**|**Aktion**|**Neuer Zustand**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)  <br/> |Öffnen Sie alle eingebetteten Objekte. Die Daten in der in _pMessage gespeicherten_ Nachricht sind garantiert identisch mit der Nachricht im vorherigen [IPersistMessage::Save-Aufruf.](ipersistmessage-save.md) Wenn der **SaveCompleted-Aufruf** erfolgreich ist, geben Sie den Status "Normal" ein. Legen Sie andernfalls den letzten Fehler auf E_OUTOFMEMORY fest, und bleiben Sie im HandsOffAfterSave-Zustand.  <br/> |[Normal](normal-state.md) oder HandsOffAfterSave  <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)  <br/> |Legen Sie den letzten Fehler auf E_INVALIDARG oder E_UNEXPECTED fest.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save** oder [IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Legen Sie den letzten Fehler fest, und geben Sie E_UNEXPECTED zurück.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Laden Sie das Formularobjekt mit Daten aus der Zielnachricht. Dieser Aufruf kann auftreten, wenn das Formularobjekt zur nächsten oder vorherigen Nachricht in einem Ordner übergeht.  <br/> |Standard  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Gibt den letzten Fehler zurück.  <br/> |HandsOffAfterSave  <br/> |
|Andere [IPersistMessage: IUnknown-Methoden](ipersistmessageiunknown.md) oder -Methoden aus anderen Schnittstellen  <br/> |Legen Sie den letzten Fehler fest, und geben Sie E_UNEXPECTED zurück.  <br/> |HandsOffAfterSave  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Formularstatus](form-states.md)

