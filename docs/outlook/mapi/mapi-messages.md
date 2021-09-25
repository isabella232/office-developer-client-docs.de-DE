---
title: MAPI-Nachrichten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 417c113f-bd98-4515-85d1-09db7fc3a227
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e6c716595819e4f51d540d88cf528e0ac88313d6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610293"
---
# <a name="mapi-messages"></a>MAPI-Nachrichten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachrichten sind MAPI-Objekte, die über den MAPI-Spooler und Dienstanbieter über ein Messagingsystem von einer Clientanwendung an eine andere übertragen werden. Nahezu jede Komponente in MAPI funktioniert mit Nachrichten. Mit clients let users create, save, send, and delete messages addition to copy and move them from one folder to another. Nachrichtenspeicheranbieter sind für die Nachrichtenverwaltung und die Zustellung von Nachrichten an den MAPI-Spooler oder einen Transportanbieter verantwortlich. Der MAPI-Spooler verschiebt Nachrichten an einen entsprechenden Transportanbieter, während Transportanbieter die Zustellung und den Empfang von Nachrichten zu und von einem Messagingsystem verarbeiten und Empfänger- und Nachrichtenoptionseigenschaften festlegen. Adressbuchanbieter arbeiten indirekt mit Nachrichten und unterstützen Eigenschaften, die Nachrichtenempfänger beschreiben.
  
Nachrichten werden in Ordnern innerhalb eines Nachrichtenspeichers gespeichert, in der Regel Ordner, die im IPM-Stammordner (Interpersonal Message) erstellt wurden. Nachrichten werden in der Regel auf der gleichen Ebene wie der Standardmäßige IPM-Posteingang, gesendete Elemente, gelöschte Elemente und Postausgangsordner oder auf niedrigeren Ebenen in der Hierarchie gespeichert. Nachrichten können jedoch auch außerhalb der IPM-Unterstruktur gespeichert werden.
  
Nachrichten, die in der standardmäßigen IPM-Unterstruktur erstellt wurden, weisen Standardinhalte auf (d. h. Inhalte, die für den Benutzer einer Clientanwendung sichtbar sind). Notizen und Berichte sind Beispiele für Nachrichten mit Standardinhalten. Nachrichten können auch mit zugeordneten Inhalten oder Inhalten erstellt werden, die im typischen Client nicht sichtbar sind. Ordner unterstützen zwei unterschiedliche Inhaltstabellen für die verschiedenen Nachrichtentypen: ein Standardinhaltsverzeichnis für Standardnachrichten und ein zugeordnetes Inhaltsverzeichnis für zugeordnete Nachrichten. Da die MAPI keine Standards für den Inhalt zugeordneter Nachrichten festgelegt hat, können sie beliebige Informationen enthalten. 
  
Einer Nachricht können zusätzliche Daten in Form einer Datei, einer anderen Nachricht oder eines OLE-Objekts zugeordnet sein. Diese zusätzlichen Daten, die als Anlage bezeichnet werden, werden entweder als Symbol oder für eine RTF-Nachricht als Metadatei im Nachrichtentext angezeigt. Eine Nachricht kann null, eine oder viele Anlagen aufweisen. Anlagen werden immer mit der Nachricht übertragen.
  
Eine nachricht, die übertragen wird, hat einen oder mehrere Empfänger (Adressen, die einem bestimmten Messagingsystem zugeordnet sind). Einige Empfänger sind Einträge in einem Container, der zu einem Adressbuchanbieter im aktuellen Profil gehört. Andere Empfänger werden nur erstellt, um die Nachricht zu übertragen. Da auf Empfänger und Anlagen über die Nachricht zugegriffen werden muss, der sie zugeordnet sind, werden die Empfänger und Anlagen einer Nachricht als untergeordnete Objekte einer Nachricht bezeichnet. 
  
Nachrichtenspeicheranbieter unterstützen Nachrichten, Anlagen und Empfänger über Methoden in drei Schnittstellen: 
  
|**Schnittstelle**|**Beschreibung**|
|:-----|:-----|
|[Imessage](imessageimapiprop.md) <br/> |Verwaltet Anlagen und Empfänger, sendet Nachrichten, legt den Lesestatus fest.  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Erstellt, kopiert und verschiebt Nachrichten und Unterordner und verwaltet den Nachrichtenstatus.  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |Verwaltet Anlageneigenschaften.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Anwendungsentwicklung](mapi-application-development.md)

