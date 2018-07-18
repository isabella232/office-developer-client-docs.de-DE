---
title: Implementieren eines Formular-Viewers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a567185c-bd72-4307-928c-08cac5494c1a
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 645f98342b4b3ec2bebf3f233f719bd5cae69da9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792528"
---
# <a name="implementing-a-form-viewer"></a>Implementieren eines Formular-Viewers

  
  
**Betrifft**: Outlook 
  
Ein Formular Viewer umfasst drei Objekte: eine Nachricht-Website eine Ansicht advise-Empfänger, und ein Ansichtskontext. Jedes dieser Objekte können Sie mit einem Formular Server und den Formularen interagieren.
  
Eine Website für die Nachricht wird ein Objekt, das implementiert die [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) -Schnittstelle und hilft beim Formular Servern mit Aufgaben wie das Verschieben, speichern, oder Löschen von Nachrichten, Erstellen von neuen Nachrichten oder neuen Formular Servern starten. Nachricht Websites werden durch Formulare zum Abrufen von Informationen zu Ihrer Client-Status in Bezug auf verschiedenen-Dienstanbieter verwendet. Angenommen, können ein Formular Ihrer Website Nachricht Sie einen Zeiger auf den aktuellen Nachrichtenspeicher, eine Nachricht oder einen Ordner abzurufen. 
  
Es gibt zwei Arten von Methoden in der **IMAPIMessageSite** -Schnittstelle: 
  
- Methoden, die Informationen für Formularobjekte enthalten.
    
- Methoden, die Nachrichten zu bearbeiten.
    
Die Methoden, die Informationen für Formularobjekte enthalten sind einfach implementieren. In allen Fällen außer [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)sollte bereits Ihnen zur Verfügung stehen die Informationen, die von jeder Methode erforderlich.
  
Die Methoden, die Nachrichten bearbeiten sollte fungieren, als ob sie über die normale Benutzeroberfläche ausgelöst. Beispielsweise, wenn ein Form-Objekt die [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) -Methode aufruft, Verhalten Sie, als ob der Benutzer sich, zum Erstellen einer neuen benutzerdefinierten Nachricht mit der normale Benutzeroberfläche entschieden hat. Befehle, die dieses Verhalten in der Regel generieren sind **zum Verfassen**, **Öffnen**, **Antworten**, **Antwort an alle Empfänger**und **Weiterleiten**. 
  
Ein Ansichtskontext ist ein Objekt, das implementiert die [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) -Schnittstelle und bietet Formular Servern mit einem Kontext für die aktuelle Nachricht, Servern und einfach zu der nächsten oder der vorherigen Nachricht im Ordner wechseln. Ein Formular verwendet ein Ansichtskontext für die Freigabe von Informationen. Mit einer Ansicht Context-Objekt können ein Formular: 
  
- Registrieren Sie Ihre Client für Benachrichtigungen.
    
- Aktivieren der nächsten oder der vorherigen Nachricht im Ordner.
    
- Möchten Sie Drucken von Informationen erhalten.
    
- Abrufen des Status des Clients.
    
- Rufen Sie einen Datenstrom, der zum Speichern der Textversion einer Nachricht verwendet werden kann.
    
Ähnlich wie die Methoden in der [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) -Schnittstelle, die Methoden in **IMAPIViewContext** Korrelation mit Benutzeraktionen und Clientfeatures, die mit dem Ansichtskontext verknüpft sind. Beispielsweise ist ein Ansichtskontext beteiligt, mit die nächste oder der vorherige Nachricht aktivieren, den Inhalt des Ordners sortieren und Filtern von den Inhalt des Ordners. 
  
Es ist nicht wichtig sind, welche Mechanismus, die Sie für Benutzer bereitstellen, um diese Features zu aktivieren, es ist nur wichtig, dass die Semantik dieser Features sowie die Methoden in der **IMAPIViewContext** -Schnittstelle zugeordnet. 
  
Eine Ansicht advise-Empfänger ist ein Objekt, das implementiert die [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) -Schnittstelle und Handles Benachrichtigungen von Formular-Servern, die Einfluss auf Viewer und Hilfe-Formularen und Formular Viewer zusammenarbeiten. Weitere Informationen finden Sie unter [Senden und Empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md). 
  

