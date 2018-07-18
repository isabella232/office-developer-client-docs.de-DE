---
title: MAPI-Benachrichtigungsereignisse
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ef082d7b-9b2d-4267-beb5-d3ed1d9c7bbf
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 76974c29f1d1efef376e6d23bb0d1f8b3b0d54c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793031"
---
# <a name="mapi-notification-events"></a>MAPI-Benachrichtigungsereignisse

  
  
**Betrifft**: Outlook 
  
Wenn Clientanwendungen für die Benachrichtigung registrieren, müssen sie ein oder mehrere Ereignisse angeben. Die Ereignisse, die sie angeben können, hängt von dem Satz von Ereignissen, die die vorgesehene Advise-Quelle unterstützt. Es gibt zehn Arten von Benachrichtigungen, die Clients und -Dienstanbieter für jedes durch eine Konstante dargestellt registrieren können. Benachrichtigung über den-Objekt ist eine Ausnahme. Benachrichtigung über den-Objekt ist eine interne MAPI-Benachrichtigung an. Clients können nicht für sie registrieren und Dienstanbieter können nicht generiert wurde. Die folgende Tabelle beschreibt die Typen von Ereignissen und der Advise-Objekte, die sie unterstützen können. Die Ereignis-Konstante ist in den Ereignistyp enthalten.
  
|**Ereignistyp**|**Beschreibung**|**Advise-Source-Objekten**|
|:-----|:-----|:-----|
|Schwerwiegender Fehler ( _FnevCriticalError_)  <br/> |Eine globale Fehler oder ein Ereignis, wie etwa eine Sitzung wird heruntergefahren aufgetreten.  <br/> |Alle Typen von Nachrichtenspeicher und Address Book-Objekten, Tabelle, Status-Sitzung  <br/> |
|Objekt geändert ( _FnevObjectModified_)  <br/> |Ein MAPI-Objekt geändert wurde.  <br/> |Ordner, die Nachrichten, die alle Typen von Address Book-Objekten  <br/> |
|Erstellte Objekt ( _FnevObjectCreated_)  <br/> |Ein MAPI-Objekt wurde erstellt.  <br/> |Ordner, die Nachrichten, die alle Typen von Address Book-Objekten  <br/> |
|Objekt verschoben ( _FnevObjectMoved_)  <br/> |Ein MAPI-Objekt wurde verschoben.  <br/> |Ordner, die Nachrichten, die alle Typen von Address Book-Objekten  <br/> |
|Objekt gelöscht ( _FnevObjectDeleted_)  <br/> |Ein MAPI-Objekt wurde gelöscht.  <br/> |Ordner, die Nachrichten, die alle Typen von Address Book-Objekten  <br/> |
|Objekt kopiert ( _FnevObjectCopied_)  <br/> |Ein MAPI-Objekt wurde kopiert.  <br/> |Ordner, die Nachrichten, die alle Typen von Address Book-Objekten  <br/> |
|Erweiterte Ereignis ( _FnevExtended_)  <br/> |Ein internes Ereignis von einem bestimmten Dienstanbieter definierten ist aufgetreten.  <br/> |Alle Advise-Source-Objekt  <br/> |
|Suche abgeschlossen ( _FnevSearchComplete_)  <br/> |Suchvorgang beendet wurde, und die Ergebnisse der Suche zur Verfügung stehen.  <br/> |Ordner  <br/> |
|Tabelle geändert ( _FnevTableModified_)  <br/> |Informationen in einem MAPI-Table-Objekt geändert wurde.  <br/> |Tabellen  <br/> |
|Neue e-Mail-Nachrichten ( _FnevNewMail_)  <br/> |Eine Nachricht übermittelt wurde und wartet auf Verarbeitung.  <br/> |Nachrichtenspeicher, Ordner  <br/> |
   
Das erweiterte Ereignis wird definiert, von einem Dienstanbieter zur Darstellung eines Ereignisses mithilfe eines der anderen vordefinierten Ereignisse abgedeckt werden kann. Für dieses Ereignis können nur Clients, die wissen, bevor sie registrieren, dass es sich bei ein Dienstanbieter ein erweiterte Ereignis unterstützt registrieren. Es ist nicht möglich, damit die Clients ohne Vorauswissen zu ermitteln, ob es sich bei ein Dienstanbieter ein erweiterte Ereignis unterstützt und wenn Ja, wie Sie ein Ereignis beim Empfang zu behandeln.
  

