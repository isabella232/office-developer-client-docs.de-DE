---
title: Senden über Messagingdomänen hinweg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 65594253-66cd-486a-aa5b-0bc719f761f0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ddbaa4aeacf17f2c266ccc0ff963d005f9e403ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410112"
---
# <a name="sending-across-messaging-domains"></a>Senden über Messagingdomänen hinweg

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Messagingdomäne stellt ein oder mehrere Messagingsysteme dar, die ein gemeinsames Adressformat verwenden. Die Kommunikation über mehrere Messagingdomänen umfasst das Übersetzen einer Nachricht im Format der ursprünglichen Messagingdomäne in das Format der Zielnachrichtendomäne. Da nicht alle Adressformate kompatibel sind, ist ein Gateway erforderlich, um die Adressierungsinformationen aus dem Quellformat in das Zielformat zu übersetzen. Um die Gültigkeit in allen Messagingdomänen sicherzustellen, speichern Clientanwendungen wichtige Adressierungsinformationen in MAPI-Eigenschaften. Darüber hinaus führen Gateways die Übersetzung aus, untersuchen die Eigenschaften, die für die Übersetzung bekannt sind, und ändern sie in ein Format, das von der Zielnachrichtendomäne verwendet werden kann.
  
Zuvor hat MAPI zugelassen, dass diese Adressierungsinformationen nur den Benutzern zugeordnet werden, die aus der aktuellen Empfängerliste einer Nachricht bestehen. Die Eigenschaften, die die einzelnen Mitglieder der Empfängerliste beschreiben, haben die erforderliche Übersetzung durch das Gateway erhalten, um die Gültigkeit in allen Messagingdomänen sicherzustellen. Einige Anwendungen erfordern jedoch, dass ihre Nachrichten Informationen über Benutzer adressieren, die in der Vergangenheit möglicherweise Empfänger waren, künftig Empfänger sind oder niemals Empfänger sein werden. Beispielsweise betten Routinganwendungen, die Nachrichten in einer bestimmten Reihenfolge an eine Gruppe von Benutzern senden, Adressierungsinformationen zu diesen Benutzern in die Nachrichten ein. Die eingebetteten Informationen umfassen in der Regel die Adresse und den Adresstyp der zukünftigen Empfänger sowie möglicherweise auch ihre Rollen und Positionen in der Routingreihenfolge, ihre Namen und einen oder mehrere binäre Bezeichner pro Empfänger.
  
Damit Nachrichten Informationen zu diesen unergienten Benutzern enthalten können, enthält MAPI nun eine Strategie, um sicherzustellen, dass diese nicht-hilfsden Informationen auch korrekt über Messagingdomänen hinweg übersetzt werden. Diese Strategie basiert auf dem Konzept von Gateway-mappable-Eigenschaften.
  

