---
title: Nicht initialisierten Zustand
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c00d5bb2e5da02b007579c7a8206baa98f64143f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795787"
---
# <a name="uninitialized-state"></a>Nicht initialisierten Zustand

  
  
**Betrifft**: Outlook 
  
Initialisierte Zustand ist der Anfangszustand-Formular, die Objekte in werden sollen, wenn sie zuerst erstellt werden. Formular-Objekte werden mit Meldungsdaten initialisiert, wenn eine Clientanwendung für das Form-Objekt die [IPersistMessage::InitNew](ipersistmessage-initnew.md) oder [IPersistMessage::Load](ipersistmessage-load.md) -Methode aufruft. In der folgenden Tabelle werden die zulässigen Übergänge aus dem Status Unitialized beschrieben. 
  
|**IPersistMessage-Methode**|**Aktion**|**Neue Zustand**|
|:-----|:-----|:-----|
|[IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Laden Sie das Form-Objekt mit Standarddaten.  <br/> |[Normal](normal-state.md) <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Laden Sie das Form-Objekt mit Daten aus der Zielnachricht.  <br/> |Standard  <br/> |
|[IPersistMessage::GetClassID](ipersistmessage-getclassid.md) <br/> |Zurückgeben von Erfolg, oder legen Sie den letzten Fehler auf und E_UNEXPECTED zurückgeben.  <br/> |Nicht initialisiert  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Geben Sie den letzten Fehler zurück.  <br/> |Nicht initialisiert  <br/> |
|Andere [IPersistMessage: IUnknown](ipersistmessageiunknown.md) Methoden oder Methoden aus anderen Schnittstellen  <br/> |Legen Sie den letzten Fehler auf und zurückgeben Sie E_UNEXPECTED.  <br/> |Nicht initialisiert  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Normalzustand](normal-state.md)
  
[Formular Staaten](form-states.md)

