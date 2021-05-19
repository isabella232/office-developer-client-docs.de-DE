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
ms.openlocfilehash: f1d1895cc6f9e65929781cb0e966873d2bce197c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423377"
---
# <a name="mapi-messages"></a>MAPI-Nachrichten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachrichten sind MAPI-Objekte, die über den MAPI-Spooler und Dienstanbieter über ein Messagingsystem von einer Clientanwendung an eine andere übertragen werden. Fast jede Komponente in MAPI funktioniert mit Nachrichten. Clients ermöglichen Benutzern das Erstellen, Speichern, Senden und Löschen von Nachrichten sowie das Kopieren und Verschieben von Nachrichten aus einem Ordner in einen anderen. Nachrichtenspeicheranbieter sind für die Nachrichtenverwaltung und die Zuführung von Nachrichten an den MAPI-Spooler oder einen Transportanbieter verantwortlich. Der MAPI-Spooler verschiebt Nachrichten an einen geeigneten Transportanbieter, während Transportanbieter die Zustellung und den Empfang von Nachrichten an ein und von einem Messagingsystem verarbeiten und Empfänger- und Nachrichtenoptionseigenschaften festlegen. Adressbuchanbieter arbeiten indirekt mit Nachrichten und unterstützen Eigenschaften, die Nachrichtenempfänger beschreiben.
  
Nachrichten werden in Ordnern in einem Nachrichtenspeicher gespeichert, in der Regel Ordner, die im Stammordner für zwischenpersonelle Nachrichten (IPM) erstellt werden. Nachrichten werden in der Regel auf derselben Ebene wie die standardmäßigen IPM-Posteingangsordner, gesendeten Elemente, gelöschten Elemente und Posteingangsordner oder auf niedrigeren Ebenen in der Hierarchie gespeichert. Nachrichten können jedoch auch außerhalb der IPM-Unterstruktur gespeichert werden.
  
Nachrichten, die in der standardmäßigen IPM-Unterstruktur erstellt werden, haben Standardinhalte (d. h. Inhalte, die für den Benutzer einer Clientanwendung sichtbar sind). Notizen und Berichte sind Beispiele für Nachrichten mit Standardinhalten. Nachrichten können auch mit zugeordneten Inhalten oder Inhalten erstellt werden, die im typischen Client nicht sichtbar sind. Ordner unterstützen zwei unterschiedliche Inhaltstabellen, um die verschiedenen Nachrichtentypen zu speichern: eine Standardinhaltstabelle für Standardnachrichten und eine zugeordnete Inhaltstabelle für zugeordnete Nachrichten. Da MAPI keine Standards für den Inhalt zugeordneter Nachrichten festgelegt hat, können sie beliebige Informationen enthalten. 
  
Einer Nachricht können zusätzliche Daten in Form einer Datei, einer anderen Nachricht oder eines OLE-Objekts zugeordnet sein. Diese zusätzlichen Daten, die als Anlage bezeichnet werden, werden entweder als Symbol oder für eine RTF-Nachricht als Metadatei im Nachrichtentext angezeigt. Eine Nachricht kann 0, 1 oder viele Anlagen haben. Anlagen werden immer mit der Nachricht übertragen.
  
Eine übermittelte Nachricht hat einen oder mehrere Empfänger (Adressen, die einem bestimmten Messagingsystem zugeordnet sind). Einige Empfänger sind Einträge in einem Container, der zu einem Adressbuchanbieter im aktuellen Profil gehört. Andere Empfänger werden nur zum Übertragen der Nachricht erstellt. Da auf Empfänger und Anlagen über die Nachricht zugegriffen werden muss, der sie zugeordnet sind, werden die Empfänger und Anlagen einer Nachricht als Unterobjekte bezeichnet. 
  
Nachrichtenspeicheranbieter unterstützen Nachrichten, Anlagen und Empfänger über Methoden in drei Schnittstellen: 
  
|**Schnittstelle**|**Beschreibung**|
|:-----|:-----|
|[IMessage](imessageimapiprop.md) <br/> |Verwaltet Anlagen und Empfänger, sendet Nachrichten, legt den Lesestatus fest.  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Erstellt, kopiert und verschiebt Nachrichten und Unterordner und verwaltet den Nachrichtenstatus.  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |Verwaltet Anlageneigenschaften.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Anwendungsentwicklung](mapi-application-development.md)

