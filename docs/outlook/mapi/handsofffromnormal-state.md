---
title: HandsOffFromNormal Zustand
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d0b7baf4ab17d12145170961a43ca4be252146a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791831"
---
# <a name="handsofffromnormal-state"></a>HandsOffFromNormal Zustand

  
  
**Betrifft**: Outlook 
  
Der Zustand HandsOffFromNormal ist auf den Status [HandsOffAfterSave](handsoffaftersave-state.md) sehr ähnlich. Es ist Teil des Prozesses zum Speichern des Inhalts eines Formulars dauerhaft. In diesem Status sollte das Form-Objekt sehen davon ab, die speicherinterne Kopien der Werte der Eigenschaften für die Nachricht, ändern, da es möglicherweise nicht eine weitere Möglichkeit, um die Änderungen zu speichern. In der folgenden Tabelle werden die zulässigen Übergänge aus dem Status HandsOffFromNormal beschrieben. 
  
|IPersistMessage **-Methode **|**Aktion**|**Neue Zustand**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ NULL)  <br/> |Ersetzen Sie das Meldungsobjekt Nachricht durch _pMessage_, der Ersatz für die Nachricht durch den vorherigen Aufruf [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)gesperrt ist. Die Daten in die neue Nachricht ist dieselbe wie die gesperrten Nachricht garantiert. Die Nachricht nicht als clean gekennzeichnet werden soll, und sollte nach diesem Aufruf [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) aufgerufen werden. Wenn der **SaveCompleted** Aufruf erfolgreich ist, geben Sie den [normalen](normal-state.md) Zustand. Bleiben Sie andernfalls den Status HandsOffFromNormal.  <br/> |Normal oder HandsOffFromNormal  <br/> |
|**IPersistMessage::SaveCompleted** (_pMessage ==_ NULL)  <br/> |Legen Sie den letzten Fehler auf E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
|**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md)oder [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Legen Sie den letzten Fehler auf E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Geben Sie den letzten Fehler zurück.  <br/> |HandsOffFromNormal  <br/> |
|Andere [IPersistMessage: IUnknown](ipersistmessageiunknown.md) Methoden oder Methoden aus anderen Schnittstellen  <br/> |Legen Sie den letzten Fehler auf E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Formular Staaten](form-states.md)

