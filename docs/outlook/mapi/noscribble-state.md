---
title: Noscribble-Zustand
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
# <a name="noscribble-state"></a>Noscribble-Zustand

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Status noscribble gibt an, dass Änderungen an einer Nachricht gespeichert werden. Das tatsächliche Speichern von Werten, die in der Benutzeroberfläche des Form-Objekts gespeichert sind, tritt auf, wenn die [IPersistMessage:: Save](ipersistmessage-save.md) -Methode des Form-Objekts von der Clientanwendung aufgerufen wird. In der folgenden Tabelle werden zulässige Übergänge aus dem Status noscribble beschrieben. 
  
|IPersistMessage * *-Methode * *|**Action**|**Neuer Status**|
|:-----|:-----|:-----|
|[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage = =_ null)  <br/> |Wenn das _fSameAsLoad_ -Flag für den [IPersistMessage:: Save](ipersistmessage-save.md) -Aufruf true war, der dazu führte, dass das Formular den noscribble-Zustand eingibt und die Nachricht geändert wurde, markieren Sie die Änderungen intern als gespeichert, und rufen Sie die [IMAPIViewAdviseSink::](imapiviewadvisesink-onsaved.md) onsaved auf. Methode.  <br/> |[Normal](normal-state.md) <br/> |
|**IPersistMessage:: SaveCompleted** (_pMessage! =_ null)  <br/> |Rufen Sie die [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md) -Methode (ähnlich der OLE- [IPersistStorage:: HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) -Methode) gefolgt von den normalen **SaveCompleted** -Aktionen auf. Wenn **SaveCompleted** erfolgreich war, geben Sie den normalen Status ein. Geben Sie andernfalls den [HandsOffAfterSave](handsoffaftersave-state.md) -Status ein.  <br/> |Normal oder HandsOffAfterSave  <br/> |
|**HandsOffMessage** <br/> |Rekursives Aufrufen der **HandsOffMessage** -Methode für eingebettete Nachrichten oder die OLE- **IPersistStorage:: HandsOffStorage** -Methode für eingebettete OLE-Objekte. Geben Sie das Message-Objekt und alle eingebetteten Nachrichten oder Objekte frei.  <br/> |HandsOffAfterSave  <br/> |
|**Save**, [IPersistMessage:: InitNew](ipersistmessage-initnew.md)oder [IPersistMessage:: Laden](ipersistmessage-load.md) <br/> |Legen Sie den letzten Fehler auf fest, und geben Sie E_UNEXPECTED zurück.  <br/> |NoScribble  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Gibt den letzten Fehler zurück.  <br/> |NoScribble  <br/> |
|Weitere [IPersistMessage: IUnknown](ipersistmessageiunknown.md) -Methoden oder-Methoden aus anderen Schnittstellen  <br/> |Legen Sie den letzten Fehler auf fest, und geben Sie E_UNEXPECTED zurück.  <br/> |NoScribble  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Formular Status](form-states.md)

