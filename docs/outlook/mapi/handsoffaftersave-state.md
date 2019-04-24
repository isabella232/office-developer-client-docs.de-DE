---
title: HandsOffAfterSave-Status
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 85630965c7e78e6fa76e348bfe98cc9060665057
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299524"
---
# <a name="handsoffaftersave-state"></a>HandsOffAfterSave-Status

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der HandsOffAfterSave-Zustand ist Teil des Prozesses zum Speichern des Inhalts eines Formulars in einem permanenten Speicher. Wenn Sie in diesem Zustand sind, sollte das Form-Objekt keine Änderungen an den in-Memory-Kopien von Werten der Eigenschaften der Nachricht vornehmen, da es möglicherweise keine weitere Möglichkeit gibt, diese Änderungen zu speichern. In der folgenden Tabelle werden zulässige Übergänge vom HandsOffAfterSave-Status beschrieben.
  
|**IPersistMessage-Methode**|**Aktion**|**Neuer Status**|
|:-----|:-----|:-----|
|[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ null)  <br/> |Öffnen Sie eingebettete Objekte. Die Daten in der in _pMessage_ gespeicherten Nachricht werden mit der Nachricht im vorherigen [IPersistMessage:: Save](ipersistmessage-save.md) -Aufruf identisch sein. Wenn der **SaveCompleted** -Aufruf erfolgreich ist, geben Sie den normalen Status ein. Andernfalls legen Sie den letzten Fehler auf E_OUTOFMEMORY und bleiben im HandsOffAfterSave-Zustand.  <br/> |[Normal](normal-state.md) oder HandsOffAfterSave  <br/> |
|**IPersistMessage:: SaveCompleted** (_pMessage = =_ null)  <br/> |Legen Sie den letzten Fehler auf E_INVALIDARG oder E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save**oder [IPersistMessage:: InitNew](ipersistmessage-initnew.md) <br/> |Legen Sie den letzten Fehler an und geben Sie E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Laden Sie das Form-Objekt mit Daten aus der Zielnachricht. Dieser Aufruf kann auftreten, wenn das Form-Objekt zur nächsten oder vorherigen Nachricht in einem Ordner geht.  <br/> |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Zurückgeben des letzten Fehlers.  <br/> |HandsOffAfterSave  <br/> |
|Andere [IPersistMessage: IUnknown](ipersistmessageiunknown.md) -Methoden oder Methoden von anderen Schnittstellen  <br/> |Legen Sie den letzten Fehler an und geben Sie E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Formular Status](form-states.md)

