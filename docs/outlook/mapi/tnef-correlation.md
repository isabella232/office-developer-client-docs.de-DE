---
title: TNEF-Korrelation
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93d1716d-a0be-45aa-85d2-6c9be65f5fd2
description: 'Letzte Änderung: 12. März 2013'
ms.openlocfilehash: 8d601bb2bbc65e21c5bc83179cc29e53ddd33876
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410371"
---
# <a name="tnef-correlation"></a>TNEF-Korrelation

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einige Messagingsysteme führen eine Korrelationsprüfung für jeden Transport-Neutral Encapsulation Format (TNEF)-Stream durch, der an eine eingehende Nachricht angefügt ist, um sicherzustellen, dass der TNEF-Stream tatsächlich zu dieser Nachricht gehört. Dazu muss der Wert eines Felds in der Kopfzeile der eingehenden Nachricht mit einer Kopie dieses Werts übereinstimmen, die in einer Eigenschaft im TNEF-Stream gespeichert ist. Werte, die für jede Nachricht wahrscheinlich eindeutig sind, z. B. Nachrichten-ID-Nummern, werden in der Regel dafür verwendet. Der Transport oder das Gateway, mit dem der TNEF-Stream erstellt wurde, ist dafür verantwortlich, einen geeigneten Wert aus dem Nachrichtenkopf zu wählen und eine Kopie in eine entsprechende Eigenschaft zu platzieren, bevor die Eigenschaften der ausgehenden Nachricht in den TNEF-Stream codiert werden. Gateways oder Transporte, die die Nachricht empfangen, können diese Eigenschaft dann aus dem TNEF-Stream extrahieren und überprüfen, ob ihr Wert dem Wert des entsprechenden Kopfzeilenfelds für die eingehende Nachricht entspricht.
  
Wenn die Werte nicht übereinstimmen, sollte das Gateway oder der Transport den TNEF-Stream verwerfen und nur den systemeigenen Nachrichtenumschlag verarbeiten. Solche Prüfungen sind sinnvoll, da nicht MAPI-basierte E-Mail-Clients eine Datei anfügen können, die einen #A0 aus einer alten Nachricht an eine Weiterleitung oder gar eine nicht zusammenhängende Nachricht enthält. Wenn diese Option nicht aktiviert ist, kann ein solcher Fehler den Nachrichtentextverlust verursachen.
  
Der ausgewählte Kopfzeilenfeldwert muss für die Nachricht eindeutig sein. Es gibt kein festes Kopfzeilenfeld für alle Messagingsysteme, da unterschiedliche Messagingsysteme unterschiedliche Kopfzeilenfelder verwenden, aber in der Regel weist das Messagingsystem der Nachricht einen eindeutigen Bezeichner zu, der für diesen Zweck geeignet ist. Beispielsweise verwenden SMTP-Systeme in der Regel den MessageID-Header, während X.400-Systeme in der Regel das IM_THIS_IPM verwenden.
  

