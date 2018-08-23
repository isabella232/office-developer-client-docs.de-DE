---
title: Zurückstellen der Verarbeitung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a791b95f-56ad-493a-9ba5-fb4c7dd80e89
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2c4577a35315c9df0055e97de26dd0baf1a2b489
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580586"
---
# <a name="deferring-processing"></a>Zurückstellen der Verarbeitung

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Übergeben Sie das MAPI_DEFERRED_ERRORS-Flag für die Methode anrufen so weit wie möglich. Viele der MAPI-Methodenaufrufe wurden optimiert Annahme dieses Flag, verursacht des Anbieters, das die angeforderte Aufgabe entweder zu verschieben, bis mehrere Aufgaben gleichzeitig ausgeführt werden können oder nicht mehr für die Ergebnisse warten können.
  
Angenommen, wenn Sie [IMsgStore::OpenEntry](imsgstore-openentry.md) , einen Ordner öffnen MAPI_DEFERRED_ERRORS übergeben, kann das Öffnen des Ordners und einen möglichen Remoteaufruf verschoben werden, bis Sie einen weiteren Anruf wie einen Anruf an des Ordners **GetHierarchyTable** oder **vornehmen GetProps** Methoden. **GetHierarchyTable** und **GetProps** erfordern die Rückgabe von Daten vom Dienstanbieter, eine Aufgabe, die sofort ausgeführt werden muss. 
  
Eine andere Möglichkeit, Verarbeitung zurückstellen ist einfach nicht um einen Anruf zu tätigen. Bewusst des Benutzers und der Benutzer eine Belastung Ressourcen oder Verarbeitungszeit erkennen kann, können Sie ermitteln, wenn es sinnvoll, Anrufe tätigen. Möglichkeit zur Verbesserung der Leistung durch Aufrufe entweder jeweils Wenn der Benutzer nicht bemerken oder durch nicht in allen besteht.
  
Betrachten Sie beispielsweise die Situation, wenn Sie mehr als eine Benachrichtigung pro Sekunde von einem Nachrichtenspeicher erhalten, die eine große Anzahl von Nachrichten verschoben wird. Eine Statusanzeige wird angezeigt, um den Prozentsatz der Abschluss des Vorgangs angeben. Benutzer werden in der Regel nicht schätzen diesen Vorgang, um langsame werden erst nach einige Sekunden vergangen sind. Aus diesem Grund, wenn Sie die Statusanzeige aktualisieren, führen Sie nehmen Sie keine Änderungen erst nach dem Initiieren des Verschiebevorgangs mindestens vier Sekunden. Dadurch wird im Allgemeinen Zeit sparen, wenn der Vorgang fast ist und Benutzer in kurzer Zeit zu informieren, wenn der Vorgang langsam ist.
  

