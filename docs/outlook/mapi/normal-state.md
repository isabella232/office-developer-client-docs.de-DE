---
title: Normaler Status
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b2acad7-5ef8-44db-911f-3bd2a7ca2778
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d7b50a92c58dd7ab1f03cb4cf84acc2d4a2b404b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335742"
---
# <a name="normal-state"></a>Normaler Status

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Normal Zustand ist der Ort, an dem das Formularobjekt den größten Teil seiner Zeit aufwendet, und wartet darauf, dass Clientanwendungen eine Aktion wie das Speichern von Änderungen oder das Schließen des Formulars initiieren. In der folgenden Tabelle werden zulässige Übergänge vom normalen Status beschrieben.
  
|**IPersistMessage-Methode**|**Aktion**|**Neuer Status**|
|:-----|:-----|:-----|
|[IPersistMessage:: Save](ipersistmessage-save.md) (_pMessage = =_ NULL, _fSameAsLoad = =_ true)  <br/> - oder -  <br/> **IPersistMessage:: Save** (_pMessage! =_ NULL, _fSameAsLoad = =_ false)  <br/> |Speichern Sie alle eingebetteten OLE-Objekte, die geändert wurden, rekursiv. Speichern Sie die Nachrichtendaten zurück in das Nachrichtenobjekt. Speichern Sie das _fSameAsLoad_ -Flag zur späteren Verwendung [](noscribble-state.md) im noscribble-Zustand.  <br/> |NoScribble  <br/> |
|**IPersistMessage:: Save** (_pMessage! =_ NULL, _fSameAsLoad = =_ true)  <br/> |Dies ist identisch mit dem vorherigen Fall, außer dass dieser Speicher **** Aufruf in Situationen mit niedrigem Arbeitsspeicher verwendet wird und nicht aus Mangel an Arbeitsspeicher fehlschlagen darf.  <br/> |NoScribble  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Rufen Sie die **HandsOffMessage** -Methode rekursiv für eingebettete Nachrichten oder die OLE [IPersistStorage:: HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) -Methode für eingebettete OLE-Objekte auf. Geben Sie das Message-Objekt und alle eingebetteten Nachrichten oder Objekte frei.  <br/> |[Status "handsofffromnormal](handsofffromnormal-state.md) <br/> |
|[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md), [IPersistMessage:: InitNew](ipersistmessage-initnew.md) oder [IPersistMessage:: Laden](ipersistmessage-load.md) <br/> |Legen Sie den letzten Fehler an und geben Sie E_UNEXPECTED.  <br/> |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Zurückgeben des letzten Fehlers.  <br/> |Normal  <br/> |
|Andere [IPersistMessage: IUnknown](ipersistmessageiunknown.md) -Methoden oder Methoden von anderen Schnittstellen  <br/> |Implementieren Sie, wie in der Dokumentation für die [IPersistMessage: IUnknown](ipersistmessageiunknown.md) -Schnittstelle beschrieben.  <br/> |Normal  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Formular Status](form-states.md)

