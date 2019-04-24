---
title: Implementieren eines Formular-Viewers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a567185c-bd72-4307-928c-08cac5494c1a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bbd0792b0e3e3f274797fabd7f5d5eb49cfc73fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332893"
---
# <a name="implementing-a-form-viewer"></a>Implementieren eines Formular-Viewers

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Formular Betrachter umfasst drei Objekte: eine Nachrichtenwebsite, eine Ansicht Advise-Senke und einen Ansichtskontext. Jedes dieser Objekte ermöglicht die Interaktion mit einem Formularserver und seinen Formularen.
  
Bei einer Nachrichtenwebsite handelt es sich um ein Objekt, das die [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) -Schnittstelle implementiert und Formularserver bei Aufgaben wie dem bewegen, speichern oder Löschen von Nachrichten, beim Erstellen neuer Nachrichten oder beim Starten neuer Formularserver unterstützt. Nachrichtenwebsites werden von Formularen verwendet, um Informationen zum Status des Clients in Bezug auf verschiedene Dienstanbieter abzurufen. Ein Formular kann beispielsweise Ihre Nachrichtenwebsite verwenden, um einen Zeiger auf den aktuellen Nachrichtenspeicher, eine Nachricht oder einen Ordner zu erhalten. 
  
Es gibt zwei Arten von Methoden in der **IMAPIMessageSite** -Schnittstelle: 
  
- Methoden, die Informationen für Formularobjekte bereitstellen.
    
- Methoden zum Bearbeiten von Nachrichten.
    
Die Methoden, die Informationen für Formularobjekte bereitstellen, sind einfach zu implementieren. In allen Fällen, außer [IMAPIMessageSite:: GetSiteStatus](imapimessagesite-getsitestatus.md), sollten die für jede Methode erforderlichen Informationen bereits verfügbar sein.
  
Die Methoden zum Bearbeiten von Nachrichten sollten so agieren, als ob Sie über Ihre reguläre Benutzeroberfläche ausgelöst wurden. Wenn beispielsweise ein Form-Objekt ihre [IMAPIMessageSite:: PostMessage](imapimessagesite-newmessage.md) -Methode aufruft, Verhalten Sie sich, als ob der Benutzer eine neue benutzerdefinierte Nachricht mit ihrer regulären Benutzeroberfläche erstellt hätte. Befehle, die dieses Verhalten in der **** Regel generieren, sind verfassen, **Öffnen**, **Antworten**, **allen Empfängern antworten**und **weiterleiten**. 
  
Ein Ansichtskontext ist ein Objekt, das die [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) -Schnittstelle implementiert und Formularserver mit einem Kontext für die aktuelle Nachricht bereitstellt, sodass Server problemlos zur nächsten oder vorherigen Nachricht im Ordner wechseln können. Ein Formular verwendet einen Ansichtskontext für die Freigabe von Informationen. Bei einem View-Kontextobjekt kann ein Formular Folgendes: 
  
- Registrieren Sie sich bei Ihrem Client für Benachrichtigungen.
    
- Die nächste oder vorherige Nachricht im Ordner aktivieren.
    
- Druckinformationen abrufen.
    
- Rufen Sie den Status Ihres Clients ab.
    
- Dient zum Abrufen eines Streams, der zum Speichern der Textversion einer Nachricht verwendet werden kann.
    
Ähnlich wie bei den Methoden in der [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) -Schnittstelle korrelieren die Methoden in **IMAPIViewContext** mit Benutzeraktionen und Clientfeatures, die sich auf den Ansichtskontext beziehen. Beispielsweise ist ein Ansichtskontext an der Aktivierung der nächsten oder der vorherigen Nachricht beteiligt, wobei der Inhalt des Ordners sortiert und der Inhalt des Ordners gefiltert wird. 
  
Es ist nicht wichtig, welchen Mechanismus Sie Benutzern zur Aktivierung dieser Funktionen zur Verfügung stellen, es ist nur wichtig, dass die Semantik dieser Features den Methoden in der **IMAPIViewContext** -Schnittstelle gut zugeordnet ist. 
  
Eine View Advise-Senke ist ein Objekt, das die [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) -Schnittstelle implementiert und Benachrichtigungen von Formular Servern verarbeitet, die sich auf den Betrachter auswirken, und Formulare und Formular Betrachter bei der Zusammenarbeit unterstützen. Weitere Informationen finden Sie unter [senden und empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md). 
  

