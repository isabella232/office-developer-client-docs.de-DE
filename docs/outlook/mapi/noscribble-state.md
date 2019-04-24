---
title: Status "noScribble"
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0246138f-c55e-4353-8e53-e973f524d52c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 239f11cf27cdebff3d51645319d7ada3b9bb9ff6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326201"
---
# <a name="noscribble-state"></a>Status "noScribble"

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Status noScribble gibt an, dass Änderungen an einer Nachricht gespeichert werden. Die tatsächliche Speicherung der in der Benutzeroberfläche des Formularobjekts gespeicherten Werte tritt auf, wenn die [IPersistMessage:: Save](ipersistmessage-save.md) -Methode des Form-Objekts von der Clientanwendung aufgerufen wird. In der folgenden Tabelle werden zulässige Übergänge vom noScribble-Zustand beschrieben. 
  
|IPersistMessage * *-Methode * *|**Aktion**|**Neuer Status**|
|:-----|:-----|:-----|
|[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage = =_ null)  <br/> |Wenn das _fSameAsLoad_ -Flag für den [IPersistMessage:: Save](ipersistmessage-save.md) -Aufruf true war, der dazu geführt hat, dass das Formular den Status "noscribble" eingegeben hat und die Nachricht geändert wurde, kennzeichnen Sie die Änderungen intern als gespeichert, und rufen Sie die [IMAPIViewAdviseSink::](imapiviewadvisesink-onsaved.md) onsaved auf. Methode.  <br/> |[Normal](normal-state.md) <br/> |
|**IPersistMessage:: SaveCompleted** (_pMessage! =_ null)  <br/> |Rufen Sie die [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md) -Methode (ähnlich der OLE- [IPersistStorage:: HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) -Methode) gefolgt von den normalen **SaveCompleted** -Aktionen auf. Wenn **SaveCompleted** erfolgreich war, geben Sie den normalen Status ein. Geben Sie andernfalls den [HandsOffAfterSave](handsoffaftersave-state.md) -Status ein.  <br/> |Normal oder HandsOffAfterSave  <br/> |
|**HandsOffMessage** <br/> |Rufen Sie die **HandsOffMessage** -Methode rekursiv für eingebettete Nachrichten oder die OLE **IPersistStorage:: HandsOffStorage** -Methode für eingebettete OLE-Objekte auf. Geben Sie das Message-Objekt und alle eingebetteten Nachrichten oder Objekte frei.  <br/> |HandsOffAfterSave  <br/> |
|**Save**, [IPersistMessage:: InitNew](ipersistmessage-initnew.md)oder [IPersistMessage:: Laden](ipersistmessage-load.md) <br/> |Legen Sie den letzten Fehler an und geben Sie E_UNEXPECTED.  <br/> |NoScribble  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Zurückgeben des letzten Fehlers.  <br/> |NoScribble  <br/> |
|Andere [IPersistMessage: IUnknown](ipersistmessageiunknown.md) -Methoden oder Methoden von anderen Schnittstellen  <br/> |Legen Sie den letzten Fehler an und geben Sie E_UNEXPECTED.  <br/> |NoScribble  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Formular Status](form-states.md)

