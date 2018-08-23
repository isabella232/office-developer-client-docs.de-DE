---
title: Status „HandsOffAfterSave“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 274e7206171e1874e3625896952f861d25f3b382
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564535"
---
# <a name="handsoffaftersave-state"></a>Status „HandsOffAfterSave“

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Der Zustand HandsOffAfterSave ist Teil des Prozesses zum Speichern des Inhalts eines Formulars dauerhaft. In diesem Status sollte das Form-Objekt sehen davon ab, die speicherinterne Kopien der Werte der Eigenschaften für die Nachricht, ändern, da es möglicherweise nicht eine weitere Möglichkeit, um die Änderungen zu speichern. In der folgenden Tabelle werden die zulässigen Übergänge aus dem Status HandsOffAfterSave beschrieben.
  
|**IPersistMessage-Methode**|**Aktion**|**Neue Zustand**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ NULL)  <br/> |Eingebettete Objekte zu öffnen. Die Daten in der Nachricht in _pMessage_ gespeichert werden unbedingt die Nachricht in der vorherigen Aufruf der [IPersistMessage::Save](ipersistmessage-save.md) identisch sein. Wenn der Anruf **SaveCompleted** erfolgreich ist, geben Sie die normalen Zustand. Andernfalls legen Sie den letzten Fehler auf E_OUTOFMEMORY und bleiben Sie in der HandsOffAfterSave Zustand.  <br/> |[Normal](normal-state.md) oder HandsOffAfterSave  <br/> |
|**IPersistMessage::SaveCompleted** (_pMessage ==_ NULL)  <br/> |Legen Sie den letzten Fehler auf E_INVALIDARG oder E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Speichern**oder [IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Legen Sie den letzten Fehler auf und zurückgeben Sie E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Laden Sie das Form-Objekt mit Daten aus der Zielnachricht. Dieses Anrufs kann auftreten, wenn das Form-Objekt an der nächsten oder der vorherigen Nachricht in einem Ordner geht.  <br/> |Standard  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Geben Sie den letzten Fehler zurück.  <br/> |HandsOffAfterSave  <br/> |
|Andere [IPersistMessage: IUnknown](ipersistmessageiunknown.md) Methoden oder Methoden aus anderen Schnittstellen  <br/> |Legen Sie den letzten Fehler auf und zurückgeben Sie E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Formularstatus](form-states.md)

