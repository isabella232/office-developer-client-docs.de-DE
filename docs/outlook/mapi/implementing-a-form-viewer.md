---
title: Implementieren einer Formularanzeige
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a567185c-bd72-4307-928c-08cac5494c1a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bbd0792b0e3e3f274797fabd7f5d5eb49cfc73fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435817"
---
# <a name="implementing-a-form-viewer"></a>Implementieren einer Formularanzeige

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Formularanzeige umfasst drei Objekte: eine Nachrichtenwebsite, eine Ansichtssenke und einen Ansichtskontext. Mit jedem dieser Objekte können Sie mit einem Formularserver und dessen Formularen interagieren.
  
Eine Nachrichtenwebsite ist ein Objekt, das die [IMAPIMessageSite : IUnknown-Schnittstelle](imapimessagesiteiunknown.md) implementiert und Formularserver bei Aufgaben wie dem Verschieben, Speichern oder Löschen von Nachrichten, dem Erstellen neuer Nachrichten oder dem Starten neuer Formularserver unterstützt. Nachrichtenwebsites werden von Formularen verwendet, um Informationen über den Status Ihres Clients in Bezug auf verschiedene Dienstanbieter zu erhalten. Beispielsweise kann ein Formular Ihre Nachrichtenwebsite verwenden, um einen Zeiger auf Den aktuellen Nachrichtenspeicher, eine Nachricht oder einen Ordner zu erhalten. 
  
Die **IMAPIMessageSite-Schnittstelle** bietet zwei Methodentypen: 
  
- Methoden, die Informationen zu Formularobjekten bereitstellen.
    
- Methoden zum Bearbeiten von Nachrichten.
    
Die Methoden, die Informationen zu Formularobjekten bereitstellen, sind einfach zu implementieren. In allen Fällen außer [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)sollten Sie bereits über die für jede Methode erforderlichen Informationen verfügen.
  
Die Methoden zum Bearbeiten von Nachrichten sollten so tun, als wären sie über Ihre reguläre Benutzeroberfläche ausgelöst worden. Wenn z. B. ein Formularobjekt Ihre [IMAPIMessageSite::NewMessage-Methode](imapimessagesite-newmessage.md) aufruft, verhalten Sie sich so, als hätte der Benutzer eine neue benutzerdefinierte Nachricht mit der regulären Benutzeroberfläche erstellt. Befehle, die in der Regel dieses Verhalten generieren, sind **Compose**, **Open**, **Reply**, Reply to **All Recipients** und **Forward**. 
  
Ein Ansichtskontext ist ein Objekt, das die [IMAPIViewContext : IUnknown-Schnittstelle](imapiviewcontextiunknown.md) implementiert und Formularservern einen Kontext für die aktuelle Nachricht bietet, sodass Server problemlos zur nächsten oder vorherigen Nachricht im Ordner wechseln können. Ein Formular verwendet einen Ansichtskontext für die Freigabe von Informationen. Mit einem Ansichtskontextobjekt kann ein Formular: 
  
- Registrieren Sie sich bei Ihrem Client für Benachrichtigungen.
    
- Aktivieren Sie die nächste oder vorherige Nachricht im Ordner.
    
- Hier finden Sie Druckinformationen.
    
- Erhalten Sie den Status Ihres Clients.
    
- Dient zum Anzeigen eines Datenstroms, der zum Speichern der Textversion einer Nachricht verwendet werden kann.
    
Ähnlich wie die Methoden in der [IMAPIMessageSite : IUnknown-Schnittstelle](imapimessagesiteiunknown.md) korrelieren die Methoden in **IMAPIViewContext** mit Benutzeraktionen und Clientfeatures, die sich auf den Ansichtskontext beziehen. Beispielsweise ist ein Ansichtskontext mit der Aktivierung der nächsten oder vorherigen Nachricht, dem Sortieren des Ordnerinhalts und dem Filtern des Ordnerinhalts beteiligt. 
  
Es ist nicht wichtig, welchen Mechanismus Sie für Benutzer bereitstellen, um diese Features zu aktivieren. Es ist nur wichtig, dass die Semantik dieser Features den Methoden in der **IMAPIViewContext-Schnittstelle** gut zugeordnet ist. 
  
Eine Ansichtssenke ist ein Objekt, das die [IMAPIViewAdviseSink : IUnknown-Schnittstelle](imapiviewadvisesinkiunknown.md) implementiert und Benachrichtigungen von Formularservern verarbeitet, die sich auf Ihren Viewer auswirken und Formular- und Formularanzeigen bei der Zusammenarbeit unterstützen. Weitere Informationen finden Sie unter [Senden und Empfangen von Formularbenachrichtigungen](sending-and-receiving-form-notifications.md). 
  

