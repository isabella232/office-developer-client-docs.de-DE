---
title: NoScribble-Zustand
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 0246138f-c55e-4353-8e53-e973f524d52c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ab70ef11a68b601729138e2ae92adc37cc89266c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592011"
---
# <a name="noscribble-state"></a>NoScribble-Zustand

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der NoScribble-Zustand gibt an, dass Änderungen an einer Nachricht gespeichert werden. Das tatsächliche Speichern von Werten, die auf der Benutzeroberfläche des Formularobjekts gespeichert sind, erfolgt, wenn die [IPersistMessage::Save-Methode](ipersistmessage-save.md) des Formularobjekts von der Clientanwendung aufgerufen wird. In der folgenden Tabelle werden zulässige Übergänge aus dem NoScribble-Zustand beschrieben. 
  
|IPersistMessage**-Methode**|**Aktion**|**Neuer Zustand**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage ==_ NULL)  <br/> |Wenn _das Flag "fSameAsLoad"_ für den [IPersistMessage::Save-Aufruf](ipersistmessage-save.md) true war, der bewirkt hat, dass das Formular in den NoScribble-Zustand wechselt und die Nachricht geändert wurde, markieren Sie die Änderungen intern als gespeichert, und rufen Sie die [IMAPIViewAdviseSink::OnSaved-Methode auf.](imapiviewadvisesink-onsaved.md)  <br/> |[Normal](normal-state.md) <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage !=_ NULL)  <br/> |Rufen Sie die [IPersistMessage::HandsOffMessage-Methode](ipersistmessage-handsoffmessage.md) auf (ähnlich der OLE [IPersistStorage::HandsOffStorage-Methode),](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) gefolgt von den normalen **SaveCompleted-Aktionen.** Wenn **SaveCompleted** erfolgreich war, geben Sie den Status "Normal" ein. Andernfalls geben Sie den [HandsOffAfterSave-Zustand](handsoffaftersave-state.md) ein.  <br/> |Normal oder HandsOffAfterSave  <br/> |
|**HandsOffMessage** <br/> |Rufen Sie rekursiv die **HandsOffMessage-Methode** für eingebettete Nachrichten oder die OLE **IPersistStorage::HandsOffStorage-Methode** für eingebettete OLE-Objekte auf. Geben Sie das Nachrichtenobjekt und alle eingebetteten Nachrichten oder Objekte frei.  <br/> |HandsOffAfterSave  <br/> |
|**Save**, [IPersistMessage::InitNew](ipersistmessage-initnew.md), or [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Legen Sie den letzten Fehler fest, und geben Sie E_UNEXPECTED zurück.  <br/> |NoScribble  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Gibt den letzten Fehler zurück.  <br/> |NoScribble  <br/> |
|Andere [IPersistMessage: IUnknown-Methoden](ipersistmessageiunknown.md) oder -Methoden aus anderen Schnittstellen  <br/> |Legen Sie den letzten Fehler fest, und geben Sie E_UNEXPECTED zurück.  <br/> |NoScribble  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Formularstatus](form-states.md)

