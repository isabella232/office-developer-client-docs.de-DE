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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327398"
---
# <a name="tnef-correlation"></a>TNEF-Korrelation

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einige Messagingsysteme führen eine Korrelations Prüfung für einen TNEF-Stream (Transport Neutral Encapsulation Format) aus, der an eine eingehende Nachricht angefügt ist, um zu überprüfen, ob der TNEF-Stream tatsächlich zu dieser Nachricht gehört. Hierzu wird der Wert eines Felds in der Kopfzeile der eingehenden Nachricht mit einer Kopie dieses Werts abgeglichen, die in einer Eigenschaft im TNEF-Stream gespeichert ist. Werte, die vermutlich für jede Nachricht eindeutig sind, wie etwa Nachrichtennummern, werden normalerweise dafür verwendet. Der Transport oder das Gateway, mit dem der TNEF-Stream erstellt wurde, ist dafür verantwortlich, einen geeigneten Wert aus dem Nachrichtenkopf auszuwählen und eine Kopie in einer entsprechenden Eigenschaft zu platzieren, bevor die Eigenschaften der ausgehenden Nachricht in den TNEF-Stream codiert werden. Gateways oder Transports, die die Nachricht empfangen, können diese Eigenschaft dann aus dem TNEF-Stream extrahieren und sicherstellen, dass ihr Wert mit dem Wert des entsprechenden Kopfzeilenfelds in der eingehenden Nachricht übereinstimmt.
  
Wenn die Werte nicht übereinstimmen, sollte das Gateway oder der Transport den TNEF-Datenstrom verwerfen und nur den systemeigenen Nachrichtenumschlag verarbeiten. Solche Überprüfungen sind ratsam, da nicht-MAPI-basierte e-Mail-Clients möglicherweise eine Datei anfügen, die einen TNEF-Datenstrom aus einer alten Nachricht an eine Weiterleitung oder sogar eine nicht verbundene Nachricht enthält. Wenn dies nicht der Fall ist, kann ein solcher Fehler den Verlust des Nachrichtentexts verursachen.
  
Der ausgewählte Header Feldwert muss für die Nachricht eindeutig sein. Es gibt kein festes Kopfzeilenfeld für alle Messagingsysteme, da unterschiedliche Messagingsysteme unterschiedliche Kopfzeilenfelder verwenden, aber in der Regel weist das Messagingsystem der Nachricht, die für diesen Zweck geeignet ist, einen eindeutigen Bezeichner zu. SMTP-Systeme verwenden beispielsweise in der Regel den MessageID-Header, während X. 400-Systeme normalerweise das IM_THIS_IPM-Attribut verwenden.
  

