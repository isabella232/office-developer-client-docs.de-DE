---
title: MAPI-Benachrichtigungsereignisse
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ef082d7b-9b2d-4267-beb5-d3ed1d9c7bbf
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0d05672a0b136520216357cc85a6b7a125415759
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427955"
---
# <a name="mapi-notification-events"></a>MAPI-Benachrichtigungsereignisse

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn sich Clientanwendungen für ereignisbenachrichtigungen registrieren, müssen sie ein oder mehrere Ereignisse angeben. Die Ereignisse, die sie angeben können, hängen von der Gruppe von Ereignissen ab, die von der beabsichtigten Ratschlagquelle unterstützt werden. Es gibt zehn Arten von Benachrichtigungen, für die Sich Clients und Dienstanbieter registrieren können, die jeweils durch eine Konstante dargestellt werden. Die Statusobjektbenachrichtigung ist eine Ausnahme. Status-Objektbenachrichtigung ist eine interne #A0 clients cannot register for it and service providers cannot generate it. In der folgenden Tabelle werden die Ereignistypen und die beratende Quellobjekte beschrieben, die sie unterstützen können. Die Ereigniskonstante ist im Ereignistyp enthalten.
  
|**Ereignistyp**|**Beschreibung**|**Beraten von Quellobjekten**|
|:-----|:-----|:-----|
|Kritischer Fehler ( _fnevCriticalError_)  <br/> |Es ist ein globaler Fehler oder ein Ereignis aufgetreten, z. B. ein während des Herunterfahrens der Sitzung ausgeführtes Ereignis.  <br/> |Sitzung, alle Arten von Nachrichtenspeicher- und Adressbuchobjekten, Tabelle, Status  <br/> |
|Objekt geändert ( _fnevObjectModified_)  <br/> |Ein MAPI-Objekt wurde geändert.  <br/> |Ordner, Nachrichten, alle Arten von Adressbuchobjekten  <br/> |
|Objekt erstellt ( _fnevObjectCreated_)  <br/> |Ein MAPI-Objekt wurde erstellt.  <br/> |Ordner, Nachrichten, alle Arten von Adressbuchobjekten  <br/> |
|Objekt verschoben ( _fnevObjectMoved_)  <br/> |Ein MAPI-Objekt wurde verschoben.  <br/> |Ordner, Nachrichten, alle Arten von Adressbuchobjekten  <br/> |
|Objekt gelöscht ( _fnevObjectDeleted_)  <br/> |Ein MAPI-Objekt wurde gelöscht.  <br/> |Ordner, Nachrichten, alle Arten von Adressbuchobjekten  <br/> |
|Objekt kopiert ( _fnevObjectCopied_)  <br/> |Ein MAPI-Objekt wurde kopiert.  <br/> |Ordner, Nachrichten, alle Arten von Adressbuchobjekten  <br/> |
|Erweitertes Ereignis ( _fnevExtended_)  <br/> |Ein internes Ereignis, das von einem bestimmten Dienstanbieter definiert wurde, ist aufgetreten.  <br/> |Beliebiges Advise-Quellobjekt  <br/> |
|Suche abgeschlossen ( _fnevSearchComplete_)  <br/> |Ein Suchvorgang ist abgeschlossen, und die Ergebnisse der Suche sind verfügbar.  <br/> |Ordner  <br/> |
|Tabelle geändert ( _fnevTableModified_)  <br/> |Die Informationen in einem MAPI-Tabellenobjekt wurden geändert.  <br/> |Tabellen  <br/> |
|Neue _E-Mails ( fnevNewMail_)  <br/> |Eine Nachricht wurde zugestellt und wartet auf die Verarbeitung.  <br/> |Nachrichtenspeicher, Ordner  <br/> |
   
Das erweiterte Ereignis wird von einem Dienstanbieter definiert, um ein Ereignis zu repräsentieren, das von keinem der anderen vordefinierten Ereignisse abgedeckt werden kann. Nur Clients, die vor der Registrierung wissen, dass ein Dienstanbieter ein erweitertes Ereignis unterstützt, können sich für dieses Ereignis registrieren. Clients können ohne vorherige Kenntnisse nicht ermitteln, ob ein Dienstanbieter ein erweitertes Ereignis unterstützt und, falls ja, wie ein solches Ereignis beim Empfangen zu behandeln ist.
  

