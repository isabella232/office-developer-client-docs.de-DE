---
title: Nicht initialisierter Status
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: be35c9d3f8fc7badf83086e63e4c94e0efa4d5bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425561"
---
# <a name="uninitialized-state"></a>Nicht initialisierter Status

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der nicht initialisierte Status ist der anfängliche Zustand, in dem Formularobjekte bei der ersten Erstellung vorliegen sollen. Formularobjekte werden mit Nachrichtendaten initialisiert, wenn eine Clientanwendung die [IPersistMessage:: InitNew](ipersistmessage-initnew.md) -oder [IPersistMessage:: Laden](ipersistmessage-load.md) -Methode für das Form-Objekt aufruft. In der folgenden Tabelle werden zulässige Übergänge vom initialisierten-Status beschrieben. 
  
|**IPersistMessage-Methode**|**Aktion**|**Neuer Status**|
|:-----|:-----|:-----|
|[IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Laden Sie das Form-Objekt mit Standarddaten.  <br/> |[Normal](normal-state.md) <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Laden Sie das Form-Objekt mit Daten aus der Zielnachricht.  <br/> |Normal  <br/> |
|[IPersistMessage::GetClassID](ipersistmessage-getclassid.md) <br/> |Zurückgeben des Erfolgs oder Festlegen des letzten Fehlers auf und Zurückgeben von E_UNEXPECTED.  <br/> |Initialisierten  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Zurückgeben des letzten Fehlers.  <br/> |Initialisierten  <br/> |
|Andere [IPersistMessage: IUnknown](ipersistmessageiunknown.md) -Methoden oder Methoden von anderen Schnittstellen  <br/> |Legen Sie den letzten Fehler an und geben Sie E_UNEXPECTED.  <br/> |Initialisierten  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Normaler Status](normal-state.md)
  
[Formular Status](form-states.md)

