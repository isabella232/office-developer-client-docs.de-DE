---
title: Formularstatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dfc9fbf1-90d4-4756-92d9-032ac56a9c50
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 61d20ff7010151a82c53cafc69270e6925796a5c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327517"
---
# <a name="form-states"></a>Formularstatus

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Formularobjekte können sich in einem von fünf unterschiedlichen Status befinden, je nachdem, welche Methoden in diesen aufgerufen wurden und ob beim Ausführen dieser Methoden Fehler aufgetreten sind. Die Zustände werden in den folgenden Themen beschrieben:
  
- [Nicht initialisierter Status](uninitialized-state.md)
    
- [Normaler Status](normal-state.md)
    
- [Status "noScribble"](noscribble-state.md)
    
- [HandsOffAfterSave-Status](handsoffaftersave-state.md)
    
- [Status "handsofffromnormal-Status](handsofffromnormal-state.md)
    
Die Zustände beziehen sich in erster Linie auf den Status der Daten im Form-Objekt. Die verschiedenen Statusangaben geben an, ob die Daten gespeichert werden müssen, ob das Form-Objektänderungen an den Daten zulassen soll und wie die Daten, in denen das Formular gespeichert ist, in den Prozess eingespart werden. Daher haben die Formular Zustände und Übergänge zwischen diesen mehr mit der Implementierung der [IPersistMessage: IUnknown](ipersistmessageiunknown.md) -Schnittstellenmethoden durch den Formularserver als alle anderen. Die Kenntnis dieser Zustände ist sehr nützlich für die ordnungsgemäße Implementierung der MAPI-Formular Schnittstellen, die der Formularserver implementieren muss. 
  
In den Themen in diesem Abschnitt werden die verschiedenen Status zusammen mit den zulässigen Aktionen beschrieben, die Übergänge zu anderen Zuständen verursachen. Alle Übergänge, die nicht in den Themen aufgeführt sind, sind nicht zulässig. Wenn Ihre Formularobjekte nicht zulässige Übergänge zwischen Zuständen vornehmen, Verhalten Sie sich nicht auf die Art und Weise, wie Messaging-Clients erwarten, und können zu unvorhersehbaren Client-oder Formularobjekt Verhalten führen.
  
> [!NOTE]
> Einige Statusübergänge hängen von Informationen aus früheren Status ab. Der Formularserver muss höchstwahrscheinlich ein Flag in seinen Form-Objekten implementieren, um anzugeben, ob die Werte der Eigenschaften der Nachricht geändert wurden, um spätere Statusänderungen zu erleichtern. 
  
## <a name="see-also"></a>Siehe auch

- [Entwickeln von MAPI-Formular Servern](developing-mapi-form-servers.md)

