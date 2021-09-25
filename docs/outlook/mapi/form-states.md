---
title: Formularstatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: dfc9fbf1-90d4-4756-92d9-032ac56a9c50
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 96d4b3dc53a71027d64b8ae60291f80bc9f3fe13
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614213"
---
# <a name="form-states"></a>Formularstatus

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Formularobjekte können sich in einem von fünf unterschiedlichen Zuständen befinden, je nachdem, welche Methoden in ihnen aufgerufen wurden und ob Fehler beim Ausführen dieser Methoden aufgetreten sind. Die Zustände werden in den folgenden Themen beschrieben:
  
- [Nicht initialisierter Zustand](uninitialized-state.md)
    
- [Normalzustand](normal-state.md)
    
- [NoScribble-Zustand](noscribble-state.md)
    
- [HandsOffAfterSave-Zustand](handsoffaftersave-state.md)
    
- [HandsOffFromNormal-Zustand](handsofffromnormal-state.md)
    
Die Zustände beziehen sich in erster Linie auf den Status der Daten im Formularobjekt. Die verschiedenen Zustände geben an, ob die Daten gespeichert werden müssen, ob das Formularobjekt Änderungen an den Daten zulassen soll und an welchem Punkt sich das Speichern der Daten im Formular befindet. Daher haben die Formularzustände und Übergänge zwischen ihnen mehr mit der Implementierung von [IPersistMessage durch](ipersistmessageiunknown.md) den Formularserver zu tun: IUnknown-Schnittstellenmethoden als alle anderen. Die Kenntnis dieser Zustände ist sehr nützlich für die ordnungsgemäße Implementierung der MAPI-Formularschnittstellen, die der Formularserver implementieren muss. 
  
In den Themen in diesem Abschnitt werden die verschiedenen Zustände sowie die zulässigen Aktionen beschrieben, die Übergänge zu anderen Zuständen verursachen. Alle Übergänge, die nicht in den Themen aufgeführt sind, sind nicht zulässig. Wenn Ihre Formularobjekte unzulässige Übergänge zwischen Zuständen vornehmen, verhalten sie sich nicht so, wie dies von Messagingclients erwartet wird, und kann zu unvorhersehbaren Client- oder Formularobjektverhalten führen.
  
> [!NOTE]
> Einige Statusübergänge hängen von Informationen aus vorherigen Zuständen ab. Der Formularserver muss wahrscheinlich ein Flag in seinen Formularobjekten implementieren, um anzugeben, ob die Werte der Nachrichteneigenschaften geändert wurden, um spätere Statusänderungen zu vereinfachen. 
  
## <a name="see-also"></a>Siehe auch

- [Entwickeln von MAPI-Formularservern](developing-mapi-form-servers.md)

