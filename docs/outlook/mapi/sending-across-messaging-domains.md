---
title: Senden über Messaging-Domänen hinweg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 65594253-66cd-486a-aa5b-0bc719f761f0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ddbaa4aeacf17f2c266ccc0ff963d005f9e403ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339718"
---
# <a name="sending-across-messaging-domains"></a>Senden über Messaging-Domänen hinweg

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Messaging Domäne stellt ein oder mehrere Messagingsysteme dar, die ein gemeinsames Adressformat aufweisen. Die Kommunikation über mehrere Messaging Domänen umfasst die Übersetzung einer Nachricht, die im Format der ursprünglichen Messaging Domäne gesendet wurde, in das Format der Ziel Messaging Domäne. Da nicht alle Adressformate kompatibel sind, ist ein Gateway erforderlich, um die Adressierungsinformationen aus dem Quellformat in das Zielformat zu übersetzen. Um die Gültigkeit über Messaging-Domänen hinweg sicherzustellen, speichern Clientanwendungen wichtige Adressinformationen in MAPI-Eigenschaften. Darüber hinaus führen Gateways die Übersetzung aus, untersuchen die Eigenschaften, die Übersetzung benötigt werden, und ändern Sie in ein Format, das von der Ziel Messaging Domäne verwendet werden kann.
  
Zuvor erlaubte MAPI, dass diese Adressinformationen nur den Benutzern zugeordnet werden, die die aktuelle Empfängerliste einer Nachricht enthalten. Die Eigenschaften, die jedes Mitglied der Empfängerliste beschreiben, wurden der erforderlichen Übersetzung durch das Gateway unterzogen, um die Gültigkeit zwischen Messaging Domänen sicherzustellen. Einige Anwendungen erfordern jedoch, dass Ihre Nachrichten Adressinformationen zu Benutzern aufweisen, die möglicherweise in der Vergangenheit Empfänger waren, die Empfänger in der Zukunft oder nie Empfänger sind. Routing Anwendungen, die Nachrichten in einer bestimmten Reihenfolge an eine Gruppe von Benutzern senden, können beispielsweise Adressinformationen zu diesen Benutzern in die Nachrichten einbetten. Die eingebetteten Informationen enthalten in der Regel den Adress-und Adresstyp der zukünftigen Empfänger, und möglicherweise auch Ihre Rollen und Positionen in der Routing Reihenfolge, deren Namen und mindestens einen binären Bezeichner pro Empfänger.
  
Damit Nachrichten Informationen zu diesen nicht Empfänger Benutzern enthalten, enthält MAPI jetzt eine Strategie, um sicherzustellen, dass diese nicht Empfängerinformationen auch über Messaging Domänen korrekt übersetzt werden. Diese Strategie basiert auf dem Konzept der Gateway-zuzuordnende-Eigenschaften.
  

