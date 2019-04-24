---
title: MAPI-Nachrichten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 417c113f-bd98-4515-85d1-09db7fc3a227
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f1d1895cc6f9e65929781cb0e966873d2bce197c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345857"
---
# <a name="mapi-messages"></a>MAPI-Nachrichten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachrichten sind MAPI-Objekte, die über ein Messagingsystem von einer Clientanwendung zu einer anderen über die MAPI-Spooler-und Dienstanbieter übertragen werden. Fast jede Komponente in MAPI funktioniert mit Nachrichten. Clients ermöglichen Benutzern das Erstellen, speichern, senden und Löschen von Nachrichten zusätzlich zu kopieren und Verschieben von einem Ordner in einen anderen. Nachrichtenspeicher Anbieter sind für die Nachrichtenverwaltung und für die Zustellung von Nachrichten an den MAPI-Spooler oder einen Transportanbieter zuständig. Der MAPI-Spooler verschiebt Nachrichten an einen geeigneten Transportanbieter, wohingegen Transportanbieter die Zustellung und den Empfang von Nachrichten an ein und aus einem Messagingsystem behandeln und die Eigenschaften der Empfänger-und Nachrichten Option festlegen. Adressbuchanbieter arbeiten indirekt mit Nachrichten und unterstützen Eigenschaften zur Beschreibung von Nachrichtenempfängern.
  
Nachrichten werden in Ordnern in einem Nachrichtenspeicher gespeichert, in der Regel in Ordnern, die im Stammordner der zwischenmenschlichen Nachricht (IPM) erstellt werden. Nachrichten werden normalerweise auf derselben Ebene wie die Standardordner "IPM", "Gesendete Elemente", "Gelöschte Elemente" und "Postausgang" oder auf niedrigeren Ebenen in der Hierarchie gespeichert. Nachrichten können jedoch auch außerhalb der IPM-Unterstruktur gespeichert werden.
  
Nachrichten, die in der standardmäßigen IPM-Unterstruktur erstellt wurden, verfügen über Standardinhalte (also Inhalte, die für den Benutzer einer Clientanwendung sichtbar sind). Notizen und Berichte sind Beispiele für Nachrichten mit Standardinhalten. Nachrichten können auch mit zugeordneten Inhalten oder Inhalten erstellt werden, die im typischen Client nicht sichtbar sind. Ordner unterstützen zwei verschiedene Inhaltstabellen für die unterschiedlichen Nachrichtentypen: eine Standardinhalts Tabelle für Standardnachrichten und eine zugehörige Inhaltstabelle für zugeordnete Nachrichten. Da MAPI keine Standards für den Inhalt der zugeordneten Nachrichten festgelegt wird, können Sie beliebige Informationen enthalten. 
  
Eine Nachricht kann zusätzliche Daten enthalten – in Form einer Datei, einer anderen Nachricht oder eines OLE-Objekts, die ihr zugeordnet ist. Diese zusätzlichen Daten, die als Anlage bezeichnet werden, werden entweder als Symbol oder für eine RTF-Nachricht als Metadatei im Nachrichtentext angezeigt. Eine Nachricht kann 0, 1 oder viele Anlagen enthalten. Anlagen werden immer mit der Nachricht übertragen.
  
Eine gesendete Nachricht verfügt über einen oder mehrere Empfänger (Adressen, die einem bestimmten Messagingsystem zugeordnet sind). Einige Empfänger sind Einträge in einem Container, der zu einem Adressbuchanbieter im aktuellen Profil gehört; andere Empfänger werden nur zum Übertragen der Nachricht erstellt. Da auf Empfänger und Anlagen über die Nachricht zugegriffen werden muss, der Sie zugeordnet sind, werden Empfänger und Anlagen der Nachricht als unter Objekte bezeichnet. 
  
Nachrichtenspeicher Anbieter unterstützen Nachrichten, Anlagen und Empfänger über Methoden in drei Schnittstellen: 
  
|**Schnittstelle**|**Beschreibung**|
|:-----|:-----|
|[IMessage](imessageimapiprop.md) <br/> |Verwaltet Anlagen und Empfänger, sendet Nachrichten, legt den Lesestatus fest.  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Erstellt, kopiert und verschiebt Nachrichten und Unterordner und verwaltet den Status der Nachricht.  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |Verwaltet Anlageneigenschaften.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Anwendungsentwicklung](mapi-application-development.md)

