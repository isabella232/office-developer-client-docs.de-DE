---
title: Status „HandsOffFromNormal“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 92c604c621e2837b76e9e49fd182524ad17fbcac
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588342"
---
# <a name="handsofffromnormal-state"></a>Status „HandsOffFromNormal“

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Der Zustand HandsOffFromNormal ist auf den Status [HandsOffAfterSave](handsoffaftersave-state.md) sehr ähnlich. Es ist Teil des Prozesses zum Speichern des Inhalts eines Formulars dauerhaft. In diesem Status sollte das Form-Objekt sehen davon ab, die speicherinterne Kopien der Werte der Eigenschaften für die Nachricht, ändern, da es möglicherweise nicht eine weitere Möglichkeit, um die Änderungen zu speichern. In der folgenden Tabelle werden die zulässigen Übergänge aus dem Status HandsOffFromNormal beschrieben. 
  
|IPersistMessage **-Methode **|**Aktion**|**Neue Zustand**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ NULL)  <br/> |Ersetzen Sie das Meldungsobjekt Nachricht durch _pMessage_, der Ersatz für die Nachricht durch den vorherigen Aufruf [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)gesperrt ist. Die Daten in die neue Nachricht ist dieselbe wie die gesperrten Nachricht garantiert. Die Nachricht nicht als clean gekennzeichnet werden soll, und sollte nach diesem Aufruf [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) aufgerufen werden. Wenn der **SaveCompleted** Aufruf erfolgreich ist, geben Sie den [normalen](normal-state.md) Zustand. Bleiben Sie andernfalls den Status HandsOffFromNormal.  <br/> |Normal oder HandsOffFromNormal  <br/> |
|**IPersistMessage::SaveCompleted** (_pMessage ==_ NULL)  <br/> |Legen Sie den letzten Fehler auf E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
|**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md)oder [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Legen Sie den letzten Fehler auf E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Geben Sie den letzten Fehler zurück.  <br/> |HandsOffFromNormal  <br/> |
|Andere [IPersistMessage: IUnknown](ipersistmessageiunknown.md) Methoden oder Methoden aus anderen Schnittstellen  <br/> |Legen Sie den letzten Fehler auf E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Formularstatus](form-states.md)

