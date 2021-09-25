---
title: Normalzustand
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8b2acad7-5ef8-44db-911f-3bd2a7ca2778
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5dcd536ef7781d00869be30324f58ee7f4ed9d5f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575365"
---
# <a name="normal-state"></a>Normalzustand

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Im Normalzustand verbringt das Formularobjekt den größten Teil seiner Zeit und wartet darauf, dass Clientanwendungen eine Aktion wie das Speichern von Änderungen oder das Schließen des Formulars initiieren. In der folgenden Tabelle werden die zulässigen Übergänge aus dem Normalzustand beschrieben.
  
|**IPersistMessage-Methode**|**Aktion**|**Neuer Zustand**|
|:-----|:-----|:-----|
|[IPersistMessage::Save](ipersistmessage-save.md)(_pMessage ==_ NULL,  _fSameAsLoad ==_ TRUE)  <br/> -oder-  <br/> **IPersistMessage::Save**(_pMessage !=_ NULL,  _fSameAsLoad ==_ FALSE)  <br/> |Speichern Sie rekursiv alle eingebetteten OLE-Objekte, die geändert wurden. Speichern Sie Nachrichtendaten wieder im Nachrichtenobjekt. Store das _Flag "fSameAsLoad"_ für die spätere Verwendung im [NoScribble-Zustand.](noscribble-state.md)  <br/> |NoScribble  <br/> |
|**IPersistMessage::Save**(_pMessage !=_ NULL,  _fSameAsLoad ==_ TRUE)  <br/> |Dies ist identisch mit dem vorherigen Fall, mit der Ausnahme, dass dieser **Save-Aufruf** in Situationen mit wenig Arbeitsspeicher verwendet wird und aus Speichergründen nicht fehlschlagen darf.  <br/> |NoScribble  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Rufen Sie rekursiv die **HandsOffMessage-Methode** für eingebettete Nachrichten oder die OLE [IPersistStorage::HandsOffStorage-Methode](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) für eingebettete OLE-Objekte auf. Geben Sie das Nachrichtenobjekt und alle eingebetteten Nachrichten oder Objekte frei.  <br/> |[HandsOffFromNormal](handsofffromnormal-state.md) <br/> |
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md) oder [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Legen Sie den letzten Fehler fest, und geben Sie E_UNEXPECTED zurück.  <br/> |Standard  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Gibt den letzten Fehler zurück.  <br/> |Standard  <br/> |
|Andere [IPersistMessage: IUnknown-Methoden](ipersistmessageiunknown.md) oder -Methoden aus anderen Schnittstellen  <br/> |Implementieren Sie wie in der Dokumentation für die [IPersistMessage : IUnknown-Schnittstelle](ipersistmessageiunknown.md) beschrieben.  <br/> |Standard  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Formularstatus](form-states.md)

