---
title: NoScribble State
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0246138f-c55e-4353-8e53-e973f524d52c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 239f11cf27cdebff3d51645319d7ada3b9bb9ff6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326201"
---
# <a name="noscribble-state"></a>NoScribble State

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der NoScribble-Zustand gibt an, dass Änderungen an einer Nachricht gespeichert werden. Das tatsächliche Speichern von Werten, die auf der Benutzeroberfläche des Formularobjekts gespeichert sind, tritt auf, wenn die [IPersistMessage::Save-Methode](ipersistmessage-save.md) des Formularobjekts von der Clientanwendung aufgerufen wird. In der folgenden Tabelle werden zulässige Übergänge vom Status NoScribble beschrieben. 
  
|IPersistMessage**-Methode**|**Action**|**Neuer Status**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage ==_ NULL)  <br/> |Wenn  _das fSameAsLoad-Flag_ für den [IPersistMessage::Save-Aufruf](ipersistmessage-save.md) TRUE war, der dazu führte, dass das Formular in den Status NoScribble eint, und die Nachricht geändert wurde, markieren Sie die Änderungen intern als gespeichert, und rufen Sie die [IMAPIViewAdviseSink::OnSaved-Methode](imapiviewadvisesink-onsaved.md) auf.  <br/> |[Normal](normal-state.md) <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage !=_ NULL)  <br/> |Rufen Sie die [IPersistMessage::HandsOffMessage-Methode](ipersistmessage-handsoffmessage.md) auf (ähnlich der OLE [IPersistStorage::HandsOffStorage-Methode),](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) gefolgt von den normalen **SaveCompleted-Aktionen.** Wenn **SaveCompleted** erfolgreich war, geben Sie den Status Normal ein. Geben Sie andernfalls den [Status HandsOffAfterSave](handsoffaftersave-state.md) ein.  <br/> |Normal oder HandsOffAfterSave  <br/> |
|**HandsOffMessage** <br/> |Rufen Sie rekursiv die **HandsOffMessage-Methode** für eingebettete Nachrichten oder die OLE **IPersistStorage::HandsOffStorage-Methode** für eingebettete OLE-Objekte auf. Geben Sie das Nachrichtenobjekt und alle eingebetteten Nachrichten oder Objekte frei.  <br/> |HandsOffAfterSave  <br/> |
|**Speichern**, [IPersistMessage::InitNew](ipersistmessage-initnew.md)oder [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Legen Sie den letzten Fehler auf und geben E_UNEXPECTED.  <br/> |NoScribble  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Gibt den letzten Fehler zurück.  <br/> |NoScribble  <br/> |
|Andere [IPersistMessage : IUnknown-Methoden](ipersistmessageiunknown.md) oder -Methoden aus anderen Schnittstellen  <br/> |Legen Sie den letzten Fehler auf und geben E_UNEXPECTED.  <br/> |NoScribble  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Formularzustände](form-states.md)

