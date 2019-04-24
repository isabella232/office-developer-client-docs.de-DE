---
title: MAPI-BenachrichtigungsEreignisse
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ef082d7b-9b2d-4267-beb5-d3ed1d9c7bbf
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0d05672a0b136520216357cc85a6b7a125415759
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345850"
---
# <a name="mapi-notification-events"></a>MAPI-BenachrichtigungsEreignisse

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Clientanwendungen für die Ereignisbenachrichtigung registriert werden, müssen Sie ein oder mehrere Ereignisse angeben. Die Ereignisse, die Sie angeben können, hängen von den Ereignissen ab, die von der beabsichtigten Advise-Quelle unterstützt werden. Es gibt zehn Arten von Benachrichtigungen, für die sich Clients und Dienstanbieter registrieren können, die jeweils durch eine Konstante dargestellt werden. Die Status Objekt Benachrichtigung ist eine Ausnahme. Status Objekt Benachrichtigung ist eine interne MAPI-Benachrichtigung; Clients können sich nicht für IT registrieren, und Dienstanbieter können Sie nicht generieren. In der folgenden Tabelle werden die Ereignistypen und die Advise-Quellobjekte beschrieben, die Sie unterstützen können. Die Ereignis Konstante ist im Ereignistyp enthalten.
  
|**Ereignistyp**|**Beschreibung**|**Quellobjekte beraten**|
|:-----|:-----|:-----|
|Kritischer Fehler ( _fnevCriticalError_)  <br/> |Es ist ein globaler Fehler oder ein globales Ereignis aufgetreten, beispielsweise das Beenden eines Sitzungs Stillstands.  <br/> |Sitzung, alle Arten von Nachrichtenspeicher-und Adressbuch Objekten, Tabelle, Status  <br/> |
|Objekt geändert ( _fnevObjectModified_)  <br/> |Ein MAPI-Objekt wurde geändert.  <br/> |Ordner, Nachrichten, alle Arten von Adressbuch Objekten  <br/> |
|Objekt erstellt ( _fnevObjectCreated_)  <br/> |Es wurde ein MAPI-Objekt erstellt.  <br/> |Ordner, Nachrichten, alle Arten von Adressbuch Objekten  <br/> |
|Objekt verschoben ( _fnevObjectMoved_)  <br/> |Ein MAPI-Objekt wurde verschoben.  <br/> |Ordner, Nachrichten, alle Arten von Adressbuch Objekten  <br/> |
|Objekt gelöscht ( _fnevObjectDeleted_)  <br/> |Ein MAPI-Objekt wurde gelöscht.  <br/> |Ordner, Nachrichten, alle Arten von Adressbuch Objekten  <br/> |
|Objekt kopiert ( _fnevObjectCopied_)  <br/> |Ein MAPI-Objekt wurde kopiert.  <br/> |Ordner, Nachrichten, alle Arten von Adressbuch Objekten  <br/> |
|Extended-Ereignis ( _fnevExtended_)  <br/> |Ein internes Ereignis, das von einem bestimmten Dienstanbieter definiert wurde, ist aufgetreten.  <br/> |Beliebiges Advise-Quellobjekt  <br/> |
|Suche abgeschlossen ( _fnevSearchComplete_)  <br/> |Der Suchvorgang ist abgeschlossen, und die Ergebnisse der Suche sind verfügbar.  <br/> |Ordner  <br/> |
|Tabelle geändert ( _fnevTableModified_)  <br/> |Informationen in einem MAPI-Tabellenobjekt wurden geändert.  <br/> |Tables  <br/> |
|Neue e-Mail ( _uleventmaskfnevnewmail_)  <br/> |Eine Nachricht wurde übermittelt und wartet auf die Verarbeitung.  <br/> |Nachrichtenspeicher, Ordner  <br/> |
   
Das Extended-Ereignis wird von einem Dienstanbieter definiert, der ein Ereignis darstellt, das von keinem der anderen vordefinierten Ereignisse abgedeckt werden kann. Nur Clients, die vor Ihrer Registrierung wissen, dass ein Dienstanbieter ein erweitertes Ereignis unterstützt, können sich für dieses Ereignis registrieren. Es ist nicht möglich, dass Clients ohne Vorkenntnisse ermitteln, ob ein Dienstanbieter ein erweitertes Ereignis unterstützt und, falls dies der Fall ist, wie ein solches Ereignis beim Empfang behandelt wird.
  

