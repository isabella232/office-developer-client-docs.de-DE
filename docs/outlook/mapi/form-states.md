---
title: Formular Staaten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dfc9fbf1-90d4-4756-92d9-032ac56a9c50
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 969aca6fd37f237a607df36cc58f249828449e27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791749"
---
# <a name="form-states"></a>Formular Staaten

**Betrifft**: Outlook 
  
Formular-Objekte können in eine der fünf verschiedenen Status, je nach welche Methoden werden aufgerufen wurden und ob Fehler aufgetreten sind, in diese Methoden ausgeführt werden. In den folgenden Themen werden die Zustände beschrieben:
  
- [Nicht initialisierten Zustand](uninitialized-state.md)
    
- [Normalzustand](normal-state.md)
    
- [NoScribble Zustand](noscribble-state.md)
    
- [HandsOffAfterSave Zustand](handsoffaftersave-state.md)
    
- [HandsOffFromNormal Zustand](handsofffromnormal-state.md)
    
Die Zustände beziehen sich hauptsächlich auf den Status der Daten in das Form-Objekt. Die unterschiedlichen Zustände anzugeben, ob die Daten gespeichert werden müssen, ob das Form-Objekt Änderungen an welchem Punkt beim Speichern der Daten, die darf, denen in das Formular befindet, und die Daten. Als solche Formular Zustände und Übergänge zwischen diesen stärker mit Ihrem Formular Server Implementierung von [IPersistMessage: IUnknown](ipersistmessageiunknown.md) Schnittstellenmethoden als andere. Kenntnisse in dieser Zustände ist sehr nützlich für eine ordnungsgemäße Implementierung der MAPI-Formulars Schnittstellen, die der Formular Server implementiert werden muss. 
  
In den Themen in diesem Abschnitt beschreiben die verschiedenen Status, zusammen mit den zulässigen Aktionen, die dazu führen, in anderen Zustände wechselt dass. Alle Übergänge, die nicht in den Themen aufgeführt sind nicht zulässig. Wenn Ihr Formularobjekte nicht zulässige Übergänge zwischen Zuständen vornehmen, werden sie nicht Weise Verhalten, messaging-Clients auf Sie zukommt und unvorhersehbares Verhalten der Clients oder Form-Objekt verursachen.
  
> [!NOTE]
> Einige Statusübergänge hängen von Informationen aus der vorherigen Status. Ihr Formular Server muss in den meisten Fällen implementieren Sie ein Flag in Formularobjekte anzugeben, ob die Werte der Eigenschaften der Nachricht ändert sich höher vereinfachen geändert wurden. 
  
## <a name="see-also"></a>Siehe auch

- [Entwickeln von MAPI-Formular-Servern](developing-mapi-form-servers.md)

