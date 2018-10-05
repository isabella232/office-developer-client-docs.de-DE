---
title: Status „Normal“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b2acad7-5ef8-44db-911f-3bd2a7ca2778
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d7b50a92c58dd7ab1f03cb4cf84acc2d4a2b404b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395791"
---
# <a name="normal-state"></a>Status „Normal“

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Normale Zustand ist, das Form-Objekt für die meisten der Wartezeit für Clientanwendungen zum Initiieren einer Aktion zum Speichern von Änderungen oder zum Schließen des Formulars benötigt. In der folgenden Tabelle werden die zulässigen Übergänge von Normalzustand beschrieben.
  
|**IPersistMessage-Methode**|**Aktion**|**Neue Zustand**|
|:-----|:-----|:-----|
|[IPersistMessage::Save](ipersistmessage-save.md) (_pMessage ==_ NULL _fSameAsLoad ==_ TRUE)  <br/> -oder-  <br/> **IPersistMessage::Save** (_pMessage! =_ NULL _fSameAsLoad ==_ "false")  <br/> |Rekursiv speichern alle eingebetteten OLE-Objekte, die geändert wurden. Meldungsdaten wieder auf das Objekt "Message" speichern. Speichern Sie die Kennzeichen _fSameAsLoad_ zur späteren Verwendung im [NoScribble](noscribble-state.md) Zustand.  <br/> |NoScribble  <br/> |
|**IPersistMessage::Save** (_pMessage! =_ NULL _fSameAsLoad ==_ TRUE)  <br/> |Dies ist im vorherigen Fall identisch, außer dass dieses Anrufs **Speichern** in Speichermangel verwendet wird und muss nicht fehlendem Speicher fehl.  <br/> |NoScribble  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Rekursiv Aufrufen der **HandsOffMessage** -Methode auf eingebettete Nachrichten oder das OLE- [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) -Methode auf eingebettete OLE-Objekte. Das Objekt "Message" und alle eingebettete Nachrichten oder Objekte frei.  <br/> |[HandsOffFromNormal](handsofffromnormal-state.md) <br/> |
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md) oder [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Legen Sie den letzten Fehler auf und zurückgeben Sie E_UNEXPECTED.  <br/> |Standard  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Geben Sie den letzten Fehler zurück.  <br/> |Standard  <br/> |
|Andere [IPersistMessage: IUnknown](ipersistmessageiunknown.md) Methoden oder Methoden aus anderen Schnittstellen  <br/> |Implementieren Sie wie in der Dokumentation für die [IPersistMessage: IUnknown](ipersistmessageiunknown.md) Schnittstelle.  <br/> |Standard  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Formularstatus](form-states.md)

