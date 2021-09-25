---
title: MAPI-Benachrichtigungsereignisse
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ef082d7b-9b2d-4267-beb5-d3ed1d9c7bbf
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0558668ddfbb7890dbb59175d6902577f208a33e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610265"
---
# <a name="mapi-notification-events"></a>MAPI-Benachrichtigungsereignisse

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn sich Clientanwendungen für die Ereignisbenachrichtigung registrieren, müssen sie ein oder mehrere Ereignisse angeben. Die Ereignisse, die sie angeben können, sind von der Gruppe von Ereignissen abhängig, die die beabsichtigte Empfehlungsquelle unterstützt. Es gibt zehn Arten von Benachrichtigungen, für die sich Clients und Dienstanbieter registrieren können, die jeweils durch eine Konstante dargestellt werden. Statusobjektbenachrichtigung ist eine Ausnahme. Statusobjektbenachrichtigung ist eine interne MAPI-Benachrichtigung; clients cannot register for it and service providers cannot generate it. In der folgenden Tabelle werden die Ereignistypen und die Empfehlungsquellobjekte beschrieben, die diese unterstützen können. Die Ereigniskonstante ist im Ereignistyp enthalten.
  
|**Ereignistyp**|**Beschreibung**|**Raten von Quellobjekten**|
|:-----|:-----|:-----|
|Kritischer Fehler ( _fnevCriticalError_)  <br/> |Ein globaler Fehler oder ein globales Ereignis ist aufgetreten, z. B. das Herunterfahren einer Sitzung.  <br/> |Sitzung, alle Arten von Nachrichtenspeicher- und Adressbuchobjekten, Tabelle, Status  <br/> |
|Objekt geändert ( _fnevObjectModified_)  <br/> |Ein MAPI-Objekt wurde geändert.  <br/> |Ordner, Nachrichten, alle Arten von Adressbuchobjekten  <br/> |
|Objekt erstellt ( _fnevObjectCreated_)  <br/> |Ein MAPI-Objekt wurde erstellt.  <br/> |Ordner, Nachrichten, alle Arten von Adressbuchobjekten  <br/> |
|Objekt verschoben ( _fnevObjectMoved_)  <br/> |Ein MAPI-Objekt wurde verschoben.  <br/> |Ordner, Nachrichten, alle Arten von Adressbuchobjekten  <br/> |
|Objekt gelöscht ( _fnevObjectDeleted_)  <br/> |Ein MAPI-Objekt wurde gelöscht.  <br/> |Ordner, Nachrichten, alle Arten von Adressbuchobjekten  <br/> |
|Objekt kopiert ( _fnevObjectCopied_)  <br/> |Ein MAPI-Objekt wurde kopiert.  <br/> |Ordner, Nachrichten, alle Arten von Adressbuchobjekten  <br/> |
|Extended-Ereignis ( _fnevExtended_)  <br/> |Ein internes Ereignis, das von einem bestimmten Dienstanbieter definiert wurde, ist aufgetreten.  <br/> |Beliebiges Empfehlungsquellobjekt  <br/> |
|Suche abgeschlossen ( _fnevSearchComplete_)  <br/> |Ein Suchvorgang wurde abgeschlossen, und die Ergebnisse der Suche sind verfügbar.  <br/> |Ordner  <br/> |
|Tabelle geändert ( _fnevTableModified_)  <br/> |Informationen in einem MAPI-Tabellenobjekt wurden geändert.  <br/> |Tabellen  <br/> |
|Neue Mail ( _fnevNewMail_)  <br/> |Eine Nachricht wurde zugestellt und wartet auf die Verarbeitung.  <br/> |Nachrichtenspeicher, Ordner  <br/> |
   
Das erweiterte Ereignis wird von einem Dienstanbieter definiert, um ein Ereignis darzustellen, das von keinem der anderen vordefinierten Ereignisse abgedeckt werden kann. Nur Clients, die vor der Registrierung wissen, dass ein Dienstanbieter ein erweitertes Ereignis unterstützt, können sich für dieses Ereignis registrieren. Clients können ohne vorheriges Wissen nicht ermitteln, ob ein Dienstanbieter ein erweitertes Ereignis unterstützt und, falls ja, wie ein solches Ereignis beim Empfang behandelt wird.
  

