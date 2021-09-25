---
title: Nicht initialisierter Zustand
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f2c2d31033ee77e1de581045012be632f15c5dc4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609236"
---
# <a name="uninitialized-state"></a>Nicht initialisierter Zustand

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der nicht initialisierte Zustand ist der Anfangszustand, in dem sich Formularobjekte befinden sollten, wenn sie zum ersten Mal erstellt werden. Formularobjekte werden mit Nachrichtendaten initialisiert, wenn eine Clientanwendung die [IPersistMessage::InitNew-](ipersistmessage-initnew.md) oder [IPersistMessage::Load-Methode](ipersistmessage-load.md) für das Formularobjekt aufruft. In der folgenden Tabelle werden zulässige Übergänge aus dem Zustand "Unitialisiert" beschrieben. 
  
|**IPersistMessage-Methode**|**Aktion**|**Neuer Zustand**|
|:-----|:-----|:-----|
|[IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Laden Sie das Formularobjekt mit Standarddaten.  <br/> |[Normal](normal-state.md) <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Laden Sie das Formularobjekt mit Daten aus der Zielnachricht.  <br/> |Standard  <br/> |
|[IPersistMessage::GetClassID](ipersistmessage-getclassid.md) <br/> |Zurückgeben des Erfolgs oder Festlegen des letzten Fehlers auf und Zurückgeben E_UNEXPECTED.  <br/> |Nicht initialisiert  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Gibt den letzten Fehler zurück.  <br/> |Nicht initialisiert  <br/> |
|Andere [IPersistMessage: IUnknown-Methoden](ipersistmessageiunknown.md) oder -Methoden aus anderen Schnittstellen  <br/> |Legen Sie den letzten Fehler fest, und geben Sie E_UNEXPECTED zurück.  <br/> |Nicht initialisiert  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Normalzustand](normal-state.md)
  
[Formularstatus](form-states.md)

