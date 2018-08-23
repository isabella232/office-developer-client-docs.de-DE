---
title: MAPI-Spezialordner
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f2aa2376-b293-4d05-9104-218cc1fe1758
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 396a6c01d0b9cd867706a7dd4997bd6ddd7fd147
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578290"
---
# <a name="mapi-special-folders"></a>MAPI-Spezialordner

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
MAPI definiert einige Ordner, die spezielle sind, da sie vordefinierte Rollen als Standardordner f�r bestimmte Arten von Nachrichten dienen. Diesen Spezialordnern k�nnen in der Regel k�nnen nicht gel�scht werden, und spezielle Eintrag Bezeichnereigenschaften vorhanden sind.
  
Es gibt acht Spezialordner, einige, die Teil der Unterstruktur zwischen Personen Nachricht (IPM) sind. MAPI erstellt diese Ordner, bevor ein Client Zugriff auf den Nachrichtenspeicher erh�lt, nach dem der Client die Ordner l�schen bei Bedarf werden kann. Einige Anbieter Nachricht zulassen l�schen, w�hrend andere Benutzer nicht der Fall ist. In der folgenden Tabelle werden diese Ordner beschrieben.
  
**MAPI-Ordner**

|**Ordner**|**Beschreibung**|
|:-----|:-----|
|Postausgang  <br/> |Ausgehende IPM Nachrichten enth�lt.  <br/> |
|Ordner "Gel�schte Elemente"  <br/> |Enth�lt IPM-Nachrichten, die zum L�schen markiert sind.  <br/> |
|Ordner 'Gesendete Elemente'  <br/> |Enth�lt IPM-Nachrichten, die gesendet wurden.  <br/> |
|IPM-Stammordner  <br/> |Ordner f�r die Verwaltung von IPM-Nachrichten enth�lt.  <br/> |
|Ordner empfangen  <br/> |Eingehende Nachrichten f�r eine bestimmte Nachrichtenklasse enth�lt.  <br/> |
|Suchergebnisse Stammordner  <br/> |Ordner f�r die Verwaltung von Suchergebnissen enth�lt.  <br/> |
|Stammordner gemeinsamen-Ansichten  <br/> |Ordner f�r die Verwaltung von Ansichten f�r den Nachrichtenspeicher enth�lt.  <br/> |
|Pers�nliche Ansichten Stammordner  <br/> |Ordner f�r die Verwaltung von Ansichten f�r einen bestimmten Benutzer enth�lt.  <br/> |
   
The first four folders relate to the IPM subtree, a tree of folders that MAPI creates when a message store is initialized. Default message stores for interactive messaging clients always include the IPM folder subtree and the other special folders in their folder hierarchy. Non-default message stores are required only to support the search-results root folder, the IPM subtree root folder, the Deleted Items folder, and the receive folder. To ensure that the IPM subtree folders exist and are valid, clients can call the [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function. **HrValidateIPMSubtree** checks the folders and recreates them if there is a problem. 
  
Die Stammordner f�r Suchergebnisse, allgemeine Ansichten und pers�nliche Ansichten sind nicht Teil der IPM-Unterstruktur; Diese Ordner werden in den Stammordner f�r den Nachrichtenspeicher erstellt. Suchergebnisse Stammordner enth�lt Ordner, die Inhalt Tabellen mit Nachrichten zu unterst�tzen, die eine Reihe von Suchkriterien erf�llen. Obwohl Clients zum Erstellen von Suchergebnissen Ordnern in einem Ordner zul�ssig sind, bestimmen die meisten Clients einen einzelner Stammordner auf das �bergeordnete Objekt des alle Suchergebnisse werden w�hrend der Sitzung erstellten Ordner. 
  
Die Stammordner gemeinsamen- und pers�nliche Ansichten enthalten die Ansichten oder bevorzugten M�glichkeiten f�r die Darstellung von Nachrichten und Ordnern Daten beschrieben. Stammordner gemeinsamen Ansichten enth�lt Ansichten, die mit einem beliebigen Ordner im Nachrichtenspeicher Clients verwenden k�nnen. Ordner Pers�nliche Ansichten enth�lt Ansichten, die von einem bestimmten Benutzer f�r einen bestimmten Ordner oder Ordner definiert wurden.
  
Clients, die mit IPM-Nachrichten arbeiten sollten alle Ordner und Nachrichten unter IPM Unterstruktur Stammordner, statt in den Stammordner des Nachrichtenspeichers erstellen. Dies bietet nicht-IPM-Clients � die Clients, die Nachrichten zwischen Computern oder zwischen Menschen und Computern ausgetauscht verarbeiten � eine einfache M�glichkeit, ihre Nachrichten von Clients IPM ausblenden. 
  
MAPI assigns special entry identifier properties for these special folders. For a list of the special folder entry identifiers, see [�ffnen eines Ordners Nachrichtenspeicher](opening-a-message-store-folder.md).
  
### <a name="outlook-special-folders"></a>Outlook-Spezialordner

Outlook-Spezialordner werden durch die Eintrags-IDs identifiziert, die in den Ordner Posteingang und den Stammordner f�r den Nachrichtenspeicher gespeichert sind.
  
|**Folder**|**Der festzulegenden Eigenschaft**|
|:-----|:-----|
|Calendar  <br/> |**PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md))  <br/> |
|Kontakte  <br/> |**PR_IPM_CONTACT_ENTRYID** ([PidTagIpmContactEntryId](pidtagipmcontactentryid-canonical-property.md))  <br/> |
|Journal  <br/> |**PR_IPM_JOURNAL_ENTRYID** ([PidTagIpmJournalEntryId](pidtagipmjournalentryid-canonical-property.md))  <br/> |
|Hinweise  <br/> |**PR_IPM_NOTE_ENTRYID** ([PidTagIpmNoteEntryId](pidtagipmnoteentryid-canonical-property.md))  <br/> |
|Tasks  <br/> |**PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md))  <br/> |
|Entwürfe  <br/> |**PR_IPM_DRAFTS_ENTRYID** ([PidTagIpmDraftsEntryId](pidtagipmdraftsentryid-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Ordner](mapi-folders.md)

