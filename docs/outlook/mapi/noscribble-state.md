---
title: Status „NoScribble“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0246138f-c55e-4353-8e53-e973f524d52c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 239f11cf27cdebff3d51645319d7ada3b9bb9ff6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392567"
---
# <a name="noscribble-state"></a>Status „NoScribble“

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der NoScribble Zustand zeigt an, dass Änderungen an einer Nachricht gespeichert werden. Das tatsächliche Speichern von Werten in der Benutzeroberfläche für das Form-Objekt gespeichert tritt auf, wenn von der Clientanwendung das Formularobjekt [IPersistMessage::Save](ipersistmessage-save.md) -Methode aufgerufen wird. In der folgenden Tabelle werden die zulässigen Übergänge aus dem Status NoScribble beschrieben. 
  
|IPersistMessage **-Methode **|**Aktion**|**Neue Zustand**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage ==_ NULL)  <br/> |Wenn _fSameAsLoad_ -Flag auf true festgelegt wurde der [IPersistMessage::Save](ipersistmessage-save.md) -Aufruf, der das Formular, um den Status NoScribble und die Nachricht eingeben verursachte geändert wurde, intern die Änderungen, die als gespeichert zu markieren, und rufen die [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) -Methode.  <br/> |[Normal](normal-state.md) <br/> |
|**IPersistMessage::SaveCompleted** (_pMessage! =_ NULL)  <br/> |Rufen Sie die [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) -Methode (vergleichbar mit der OLE- [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) -Methode) gefolgt von der normalen **SaveCompleted** Aktionen. Wenn **SaveCompleted** erfolgreich war, geben Sie den normalen Zustand. Geben Sie andernfalls den [HandsOffAfterSave](handsoffaftersave-state.md) Zustand.  <br/> |Normal oder HandsOffAfterSave  <br/> |
|**HandsOffMessage** <br/> |Rekursiv Aufrufen der **HandsOffMessage** -Methode auf eingebettete Nachrichten oder das OLE- **IPersistStorage::HandsOffStorage** -Methode auf eingebettete OLE-Objekte. Das Objekt "Message" und alle eingebettete Nachrichten oder Objekte frei.  <br/> |HandsOffAfterSave  <br/> |
|**Speichern**, [IPersistMessage::InitNew](ipersistmessage-initnew.md)oder [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Legen Sie den letzten Fehler auf und zurückgeben Sie E_UNEXPECTED.  <br/> |NoScribble  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Geben Sie den letzten Fehler zurück.  <br/> |NoScribble  <br/> |
|Andere [IPersistMessage: IUnknown](ipersistmessageiunknown.md) Methoden oder Methoden aus anderen Schnittstellen  <br/> |Legen Sie den letzten Fehler auf und zurückgeben Sie E_UNEXPECTED.  <br/> |NoScribble  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Formularstatus](form-states.md)

