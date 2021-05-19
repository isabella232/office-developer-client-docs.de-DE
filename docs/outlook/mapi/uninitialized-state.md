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
  
Der Status "Nicht initialisiert" ist der Anfangszustand, in dem sich Formularobjekte befinden sollten, wenn sie zum ersten Mal erstellt werden. Formularobjekte werden mit Nachrichtendaten initialisiert, wenn eine Clientanwendung die [IPersistMessage::InitNew-](ipersistmessage-initnew.md) oder [IPersistMessage::Load-Methode](ipersistmessage-load.md) für das Formularobjekt aufruft. In der folgenden Tabelle werden zulässige Übergänge vom Unitialized-Zustand beschrieben. 
  
|**IPersistMessage-Methode**|**Action**|**Neuer Status**|
|:-----|:-----|:-----|
|[IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Laden Sie das Formularobjekt mit Standarddaten.  <br/> |[Normal](normal-state.md) <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Laden Sie das Formularobjekt mit Daten aus der Zielnachricht.  <br/> |Standard  <br/> |
|[IPersistMessage::GetClassID](ipersistmessage-getclassid.md) <br/> |Zurückgeben des Erfolgs oder Festlegen des letzten Fehlers auf und Zurückgeben E_UNEXPECTED.  <br/> |Nicht initialisiert  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Gibt den letzten Fehler zurück.  <br/> |Nicht initialisiert  <br/> |
|Andere [IPersistMessage : IUnknown-Methoden](ipersistmessageiunknown.md) oder -Methoden aus anderen Schnittstellen  <br/> |Legen Sie den letzten Fehler auf und geben E_UNEXPECTED.  <br/> |Nicht initialisiert  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Normalzustand](normal-state.md)
  
[Formularzustände](form-states.md)

