---
title: TNEF-Korrelation
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 93d1716d-a0be-45aa-85d2-6c9be65f5fd2
description: 'Letzte Änderung: 12. März 2013'
ms.openlocfilehash: 6f7c9403990a7950bb2e2c88528477e5a9b90501
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590908"
---
# <a name="tnef-correlation"></a>TNEF-Korrelation

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einige Messagingsysteme führen eine Korrelationsprüfung für jeden Transport-Neutral TNEF-Datenstrom (Encapsulation Format) durch, der an eine eingehende Nachricht angefügt ist, um zu überprüfen, ob der TNEF-Datenstrom tatsächlich zu dieser Nachricht gehört. Dies umfasst das Abgleichen des Werts eines Felds in der Kopfzeile der eingehenden Nachricht mit einer Kopie dieses Werts, die in einer Eigenschaft im TNEF-Stream gespeichert ist. Werte, die vermutlich für jede Nachricht eindeutig sind, z. B. Nachrichten-ID-Nummern, werden in der Regel dafür verwendet. Der Transport oder das Gateway, das den TNEF-Datenstrom erstellt hat, ist dafür verantwortlich, einen geeigneten Wert aus dem Nachrichtenheader auszuwählen und eine Kopie in eine entsprechende Eigenschaft zu platzieren, bevor die Eigenschaften der ausgehenden Nachricht im TNEF-Stream codiert werden. Gateways oder Transporte, die die Nachricht empfangen, können diese Eigenschaft dann aus dem TNEF-Stream extrahieren und überprüfen, ob ihr Wert mit dem Wert des entsprechenden Kopfzeilenfelds für die eingehende Nachricht übereinstimmt.
  
Wenn die Werte nicht übereinstimmen, sollte das Gateway oder der Transport den TNEF-Datenstrom verwerfen und nur den systemeigenen Nachrichtenumschlag verarbeiten. Solche Überprüfungen sind vorsichtig, da nicht MAPI-basierte E-Mail-Clients eine Datei anfügen können, die einen TNEF-Stream von einer alten Nachricht an eine Weiterleitung oder sogar eine nachricht ohne Bezug enthält. Wenn dieser Fehler nicht überprüft wird, kann ein solcher Fehler zu einem Verlust des Nachrichtentexts führen.
  
Der ausgewählte Headerfeldwert muss für die Nachricht eindeutig sein. Es gibt kein festes Kopfzeilenfeld für alle Messagingsysteme, da unterschiedliche Messagingsysteme unterschiedliche Kopfzeilenfelder verwenden, aber in der Regel weist das Messagingsystem der Nachricht einen eindeutigen Bezeichner zu, der für diesen Zweck geeignet ist. SMTP-Systeme verwenden z. B. in der Regel den MessageID-Header, während X.400-Systeme in der Regel das attribut IM_THIS_IPM verwenden.
  

