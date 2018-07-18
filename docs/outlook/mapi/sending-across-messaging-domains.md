---
title: Senden über Nachrichtendomänen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 65594253-66cd-486a-aa5b-0bc719f761f0
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1fc5e4de63815c2cbfcb4818a9f6454af8c4d93b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795467"
---
# <a name="sending-across-messaging-domains"></a>Senden über Nachrichtendomänen

  
  
**Betrifft**: Outlook 
  
Eine messaging Domäne stellt eine oder mehrere messaging-Systemen, die ein gemeinsames Adresse Format dar. Die Kommunikation über mehrere Domänen messaging umfasst eine Nachricht in das Format der ursprünglichen messaging-Domäne in das Format des der Zieldomäne messaging übersetzen. Da nicht alle Adressformate kompatibel sind, ist ein Gateway erforderlich, um die Adressinformationen sowie das Format der Quelle in das Zielformat übersetzt wird. Um die Gültigkeit messaging domänenübergreifend sicherzustellen, speichern Clientanwendungen wichtige Adressinformationen in MAPI-Eigenschaften. Führen Sie darüber hinaus Gateways die Übersetzung, überprüft die Eigenschaften bekanntermaßen benötigen Übersetzung und ändern Sie diese in ein Format, die die Zieldomäne messaging verwenden können.
  
Bisher zulässig MAPI diese Adressinformationen, nur die Benutzer zugeordnet werden soll, die aktuelle Empfängerliste eine Nachricht umfassen. Die Beschreibung jedes Mitglied die Empfängerliste Eigenschaften vorgenommen wurden die erforderliche Übersetzung vom Gateway messaging domänenübergreifend Gültigkeit sicherzustellen. Einige Anwendungen erfordern jedoch, dass ihre Nachrichten enthalten Informationen zu Benutzern, die möglicherweise Empfänger in der Vergangenheit wurden Adressierung, Empfänger in der Zukunft werden oder nie Empfänger werden. Beispielsweise einbetten routing bereit, mit die Senden von Nachrichten an eine Gruppe von Benutzern in einer bestimmten Reihenfolge reagieren auf Informationen über diese Benutzer in den Nachrichten. Die eingebettete Informationen umfasst in der Regel die Adresse und den Adresstyp zukünftige Empfänger, und möglicherweise auch ihre Rollen und Positionen in der Reihenfolge der Weiterleitung, deren Namen und eine oder mehrere binäre Kennungen pro Empfänger.
  
Um Nachrichten mit Informationen zu diesen nonrecipient Benutzer aktivieren möchten, enthält die MAPI nun eine Strategie zum sicherstellen, dass diese nonrecipient Informationen auch ordnungsgemäß über messaging Domänen übersetzt wird. Diese Strategie basiert auf das Konzept der Gateway sämtliche Eigenschaften.
  

