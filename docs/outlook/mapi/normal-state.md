---
title: Normalzustand
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b2acad7-5ef8-44db-911f-3bd2a7ca2778
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d7b50a92c58dd7ab1f03cb4cf84acc2d4a2b404b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335742"
---
# <a name="normal-state"></a>Normalzustand

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Im Normalzustand verbringt das Formularobjekt die meiste Zeit und wartet auf Clientanwendungen, um eine Aktion wie das Speichern von Änderungen oder schließen des Formulars zu initiieren. In der folgenden Tabelle werden zulässige Übergänge vom Normalzustand beschrieben.
  
|**IPersistMessage-Methode**|**Action**|**Neuer Status**|
|:-----|:-----|:-----|
|[IPersistMessage::Save](ipersistmessage-save.md)(_pMessage ==_ NULL,  _fSameAsLoad ==_ TRUE)  <br/> - oder -  <br/> **IPersistMessage::Save**(_pMessage !=_ NULL,  _fSameAsLoad ==_ FALSE)  <br/> |Speichern Sie rekursiv alle eingebetteten OLE-Objekte, die geändert wurden. Speichern Sie Nachrichtendaten zurück in das Message-Objekt. Store das _fSameAsLoad-Flag_ für die spätere Verwendung im [NoScribble-Zustand.](noscribble-state.md)  <br/> |NoScribble  <br/> |
|**IPersistMessage::Save**(_pMessage !=_ NULL,  _fSameAsLoad ==_ TRUE)  <br/> |Dies ist mit dem vorherigen Fall identisch, mit der Ausnahme, dass dieser **Save-Aufruf** in Situationen mit wenig Arbeitsspeicher verwendet wird und aus Mangel an Arbeitsspeicher nicht fehlschlagen darf.  <br/> |NoScribble  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Rufen Sie rekursiv die **HandsOffMessage-Methode** für eingebettete Nachrichten oder die OLE [IPersistStorage::HandsOffStorage-Methode](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) für eingebettete OLE-Objekte auf. Geben Sie das Nachrichtenobjekt und alle eingebetteten Nachrichten oder Objekte frei.  <br/> |[HandsOffFromNormal](handsofffromnormal-state.md) <br/> |
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md) oder [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Legen Sie den letzten Fehler auf und geben E_UNEXPECTED.  <br/> |Standard  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Gibt den letzten Fehler zurück.  <br/> |Standard  <br/> |
|Andere [IPersistMessage : IUnknown-Methoden](ipersistmessageiunknown.md) oder -Methoden aus anderen Schnittstellen  <br/> |Implementieren Sie wie in der Dokumentation für die [IPersistMessage : IUnknown-Schnittstelle](ipersistmessageiunknown.md) beschrieben.  <br/> |Standard  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Formularzustände](form-states.md)

