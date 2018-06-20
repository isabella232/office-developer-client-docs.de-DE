---
title: HandsOffAfterSave Zustand
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4bc4d680903d81b51a39ed39db3861597443d116
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791823"
---
# <a name="handsoffaftersave-state"></a>HandsOffAfterSave Zustand

  
  
**Betrifft**: Outlook 
  
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



[Formular Staaten](form-states.md)

