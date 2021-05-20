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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429166"
---
# <a name="form-states"></a>Formularstatus

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Formularobjekte können sich in einem von fünf unterschiedlichen Zuständen unterscheiden, je nachdem, welche Methoden in ihnen aufgerufen wurden und ob Fehler bei der Ausführung dieser Methoden aufgetreten sind. Die Zustände werden in den folgenden Themen beschrieben:
  
- [Nicht initialisierter Status](uninitialized-state.md)
    
- [Normalzustand](normal-state.md)
    
- [NoScribble State](noscribble-state.md)
    
- [HandsOffAfterSave-Status](handsoffaftersave-state.md)
    
- [HandsOffFromNormal-Status](handsofffromnormal-state.md)
    
Die Zustände beziehen sich in erster Linie auf den Status der Daten im Formularobjekt. Die verschiedenen Zustände geben an, ob die Daten gespeichert werden müssen, ob das Formularobjekt Änderungen an den Daten zulassen soll und welchen Punkt das Speichern der Daten im Formular hat. Daher haben die Formularzustände und -übergänge zwischen ihnen mehr mit der Implementierung von [IPersistMessage : IUnknown-Schnittstellenmethoden](ipersistmessageiunknown.md) zu tun als alle anderen. Die Kenntnis dieser Zustände ist sehr nützlich für die ordnungsgemäße Implementierung der MAPI-Formularschnittstellen, die ihr Formularserver implementieren muss. 
  
In den Themen in diesem Abschnitt werden die verschiedenen Zustände sowie die zulässigen Aktionen beschrieben, die Übergänge in andere Zustände verursachen. Übergänge, die in den Themen nicht aufgeführt sind, sind nicht zulässig. Wenn Ihre Formularobjekte nicht zulässige Übergänge zwischen Zuständen erstellen, verhalten sie sich nicht wie von Messagingclients erwartet und können unvorhersehbares Client- oder Formularobjektverhalten verursachen.
  
> [!NOTE]
> Einige Zustandsübergänge hängen von Informationen aus früheren Zuzuständen ab. Der Formularserver muss höchstwahrscheinlich ein Kennzeichen in seinen Formularobjekten implementieren, um anzugeben, ob die Werte der Eigenschaften der Nachricht geändert wurden, um spätere Statusänderungen zu erleichtern. 
  
## <a name="see-also"></a>Siehe auch

- [Entwickeln von MAPI-Formularservern](developing-mapi-form-servers.md)

