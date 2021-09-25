---
title: Senden über Messagingdomänen hinweg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 65594253-66cd-486a-aa5b-0bc719f761f0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2161b4d28c668c1a294dff8b666df8afa6eaedef
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578683"
---
# <a name="sending-across-messaging-domains"></a>Senden über Messagingdomänen hinweg

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Messagingdomäne stellt ein oder mehrere Messagingsysteme dar, die ein gemeinsames Adressformat verwenden. Bei der Kommunikation über mehrere Messagingdomänen hinweg muss eine Nachricht, die im Format der ursprünglichen Messagingdomäne gesendet wurde, in das Format der Zielmessagingdomäne übersetzt werden. Da nicht alle Adressformate kompatibel sind, ist ein Gateway erforderlich, um die Adressierungsinformationen aus dem Quellformat in das Zielformat zu übersetzen. Um die Gültigkeit über Messagingdomänen hinweg sicherzustellen, speichern Clientanwendungen wichtige Adressierungsinformationen in MAPI-Eigenschaften. Darüber hinaus führen Gateways die Übersetzung durch, untersuchen die Eigenschaften, die für die Übersetzung erforderlich sind, und ändern sie in ein Format, das die Zielmessagingdomäne verwenden kann.
  
Zuvor war es mapi möglich, diese Adressinformationen nur den Benutzern zuzuordnen, die die aktuelle Empfängerliste einer Nachricht bilden. Die Eigenschaften, die jedes Mitglied der Empfängerliste beschreiben, deklarieren die erforderliche Übersetzung durch das Gateway, um die Gültigkeit über Messagingdomänen hinweg sicherzustellen. Einige Anwendungen erfordern jedoch, dass ihre Nachrichten Informationen zu Benutzern enthalten, die möglicherweise in der Vergangenheit Empfänger waren, in der Zukunft Empfänger sind oder nie Empfänger sein werden. Beispielsweise betten Routinganwendungen, die Nachrichten in einer bestimmten Reihenfolge an eine Gruppe von Benutzern senden, Adressierungsinformationen zu diesen Benutzern in die Nachrichten ein. Die eingebetteten Informationen umfassen in der Regel die Adresse und den Adresstyp der zukünftigen Empfänger und möglicherweise auch deren Rollen und Positionen in der Routingreihenfolge, deren Namen und einen oder mehrere binäre Bezeichner pro Empfänger.
  
Damit Nachrichten Informationen zu diesen nicht ezipienten Benutzern enthalten können, enthält die MAPI jetzt eine Strategie, mit der sichergestellt wird, dass diese nicht ezipienten Informationen auch ordnungsgemäß über Messagingdomänen hinweg übersetzt werden. Diese Strategie basiert auf dem Konzept der gatewayzuordnungsfähigen Eigenschaften.
  

