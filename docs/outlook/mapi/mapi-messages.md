---
title: MAPI-Nachrichten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 417c113f-bd98-4515-85d1-09db7fc3a227
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cf7876dacac40420fdedb8b6f55c99efcf56c4f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579935"
---
# <a name="mapi-messages"></a>MAPI-Nachrichten

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Nachrichten werden MAPI-Objekten, die von einer Clientanwendung an eine andere über die MAPI-Warteschlange und Dienstanbieter in einem messaging-System übertragen werden. Fast jeder Komponente in MAPI arbeitet mit Nachrichten. Clients können Benutzer erstellen, speichern, senden und Löschen von Nachrichten in zusätzlich zu kopieren und verschieben Sie sie aus einem Ordner in einen anderen. Nachricht Anbieter sind verantwortlich für die Verwaltung von Nachrichten und zum Übermitteln von Nachrichten an die Warteschlange MAPI oder eines Transportdienstes. Die MAPI-Warteschlange verschiebt Nachrichten an einen entsprechenden Transport Dienstanbieter während Transportanbieter, die Bereitstellung und den Empfang von Nachrichten an und von einem messaging-System behandeln und Empfänger und Nachricht Optionseigenschaften. Von adressbuchanbietern implementierte arbeiten indirekt mit Nachrichten, Unterstützung von Eigenschaften, die Empfänger der Nachricht zu beschreiben.
  
Nachrichten werden in Ordnern in der gesamten eines Nachrichtenspeichers in der Regel im Stammordner zwischen Personen Nachricht (IPM) erstellten Ordner gespeichert. Nachrichten werden in der Regel auf der gleichen Ebene als standard IPM Posteingang, Gesendete Objekte, Gelöschte Objekte und Postausgang-Ordner oder auf niedrigeren Ebenen in der Hierarchie gespeichert. Nachrichten können jedoch auch außerhalb der IPM-Unterstruktur gespeichert werden.
  
Nachrichten, die in der standard-IPM-Unterstruktur erstellt haben standard Inhalt (d. h., Inhalt, die für den Benutzer einer Clientanwendung sichtbar sind). Notizen und Berichte sind Beispiele für Nachrichten, die standard-Inhalt enthalten. Nachrichten können auch erstellt werden, mit der zugehörigen Inhalt oder Inhalt, die nicht in der normalen Client sichtbar sind. Ordner unterstützt zwei verschiedene Inhalte Tabellen, um die verschiedenen Arten von Nachrichten enthalten: ein Standard Inhalt der Tabelle für die standard-Nachrichten und eine zugeordnete Inhaltstabelle für zugeordnete Nachrichten. Da MAPI Standards für den Inhalt der zugeordneten Nachrichten nicht festgelegt wird, können sie beliebigen Informationen enthalten. 
  
Eine Nachricht kann zusätzliche Daten haben – in Form einer Datei, eine andere Nachricht oder ein OLE-Objekt – zugeordnet. Diese zusätzlichen Daten, die eine Anlage aufgerufen wird, wird als Symbol oder, für eine Nachricht RTF als eine Metadatei im Nachrichtentext angezeigt. Eine Nachricht kann 0 (null), 1 oder viele Anlagen haben. Anlagen werden immer mit der Meldung übertragen.
  
Eine Nachricht, die übertragen werden verfügt über einen oder mehrere Empfänger (Adressen, die mit einem bestimmten Messagingsystem verknüpft sind). Einige Empfänger sind Einträge in einem Container, zu der Adressbuch-Dienstanbieter im aktuellen Profil gehört. andere Empfänger werden nur zum Übertragen der Nachricht erstellt. Da Empfänger und Anlagen über die Nachricht müssen mit denen sie zugeordnet sind zugegriffen werden, werden Empfänger und Anlagen einer Nachricht als dessen Unterobjekte bezeichnet. 
  
Nachricht-Anbieter werden Nachrichten, die Anlagen und Empfänger über Methoden in drei Schnittstellen unterstützen: 
  
|**Schnittstelle**|**Beschreibung**|
|:-----|:-----|
|[IMessage](imessageimapiprop.md) <br/> |Anlagen und Empfänger verwaltet, sendet die Nachrichten, gelesen-Status festgelegt.  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Erstellt, kopiert, und verschiebt Nachrichten und Unterordner und Nachrichtenstatus verwaltet.  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |Eigenschaften für Dateianlage verwaltet.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Anwendungsentwicklung](mapi-application-development.md)

