---
title: Implementieren einer Formularanzeige
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a567185c-bd72-4307-928c-08cac5494c1a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 624bc14887f05052f69776d9862716bab3c9e47f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567354"
---
# <a name="implementing-a-form-viewer"></a>Implementieren einer Formularanzeige

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Formularanzeige enthält drei Objekte: eine Nachrichtenwebsite, eine Ansichts-Empfehlungssenke und einen Ansichtskontext. Mit jedem dieser Objekte können Sie mit einem Formularserver und dessen Formularen interagieren.
  
Eine Nachrichtenwebsite ist ein Objekt, das die [IMAPIMessageSite implementiert: IUnknown-Schnittstelle](imapimessagesiteiunknown.md) und unterstützt Formularserver bei Aufgaben wie Verschieben, Speichern oder Löschen von Nachrichten, Erstellen neuer Nachrichten oder Starten neuer Formularserver. Nachrichtenwebsites werden von Formularen verwendet, um Informationen über den Status Ihres Clients in Bezug auf verschiedene Dienstanbieter abzurufen. Beispielsweise kann ein Formular Ihre Nachrichtenwebsite verwenden, um einen Zeiger auf Den aktuellen Nachrichtenspeicher, eine Nachricht oder einen Ordner abzurufen. 
  
Es gibt zwei Arten von Methoden in der **IMAPIMessageSite-Schnittstelle:** 
  
- Methoden, die Formularobjekten Informationen bereitstellen.
    
- Methoden zum Bearbeiten von Nachrichten.
    
Die Methoden, die Informationen für Formularobjekte bereitstellen, sind einfach zu implementieren. In allen Fällen außer [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)sollten Sie bereits über die für die einzelnen Methoden erforderlichen Informationen verfügen.
  
Die Methoden zum Bearbeiten von Nachrichten sollten so wirken, als ob sie über die reguläre Benutzeroberfläche ausgelöst worden wären. Wenn beispielsweise ein Formularobjekt Ihre [IMAPIMessageSite::NewMessage-Methode](imapimessagesite-newmessage.md) aufruft, verhalten Sie sich so, als ob der Benutzer sich entschieden hätte, eine neue benutzerdefinierte Nachricht mit Ihrer regulären Benutzeroberfläche zu verfassen. Befehle, die in der Regel dieses Verhalten generieren, sind **Compose**, **Open**, **Reply**, Reply to **All Recipients** und **Forward**. 
  
Ein Ansichtskontext ist ein Objekt, das die [IMAPIViewContext : IUnknown-Schnittstelle](imapiviewcontextiunknown.md) implementiert und Formularservern einen Kontext für die aktuelle Nachricht bereitstellt, sodass Server problemlos zur nächsten oder vorherigen Nachricht im Ordner wechseln können. Ein Formular verwendet einen Ansichtskontext zum Freigeben von Informationen. Bei einem Ansichtskontextobjekt kann ein Formular Folgendes: 
  
- Registrieren Sie sich bei Ihrem Client für Benachrichtigungen.
    
- Aktivieren Sie die nächste oder vorherige Nachricht im Ordner.
    
- Abrufen von Druckinformationen.
    
- Rufen Sie den Status Ihres Clients ab.
    
- Rufen Sie einen Datenstrom ab, der zum Speichern der Textversion einer Nachricht verwendet werden kann.
    
Ähnlich wie die Methoden in der [IMAPIMessageSite : IUnknown-Schnittstelle](imapimessagesiteiunknown.md) korrelieren die Methoden in **IMAPIViewContext** mit Benutzeraktionen und Clientfeatures, die sich auf den Ansichtskontext beziehen. Beispielsweise ist ein Ansichtskontext mit der Aktivierung der nächsten oder vorherigen Nachricht, dem Sortieren des Inhalts des Ordners und dem Filtern des Inhalts des Ordners verbunden. 
  
Es ist nicht wichtig, welchen Mechanismus Sie für Benutzer bereitstellen, um diese Features zu aktivieren. Es ist nur wichtig, dass die Semantik dieser Features den Methoden in der **IMAPIViewContext-Schnittstelle** gut zugeordnet ist. 
  
Eine Ansichts-Empfehlungssenke ist ein Objekt, das die [IMAPIViewAdviseSink implementiert: IUnknown-Schnittstelle](imapiviewadvisesinkiunknown.md) und verarbeitet Benachrichtigungen von Formularservern, die sich auf Ihren Viewer auswirken, und hilft Formularen und Formularviewern bei der Zusammenarbeit. Weitere Informationen finden Sie unter [Senden und Empfangen von Formularbenachrichtigungen.](sending-and-receiving-form-notifications.md) 
  

