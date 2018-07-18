---
title: Zuzuteilen Address Book-Benachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f198be78dd36a6d0c9439da68ab322cd8cfa4172
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791791"
---
# <a name="handing-address-book-notification"></a>Zuzuteilen Address Book-Benachrichtigung
  
**Betrifft**: Outlook 
  
Address Book Benachrichtigungen ermöglichen einen Client Hier erfahren, die Adressbuch Adresseintrag oder zu einem bestimmten Eintrag Auftreten von Ereignissen. Sie können für diese Benachrichtigungen über das MAPI-Adressbuch durch Aufrufen von [IAddrBook::Advise](iaddrbook-advise.md) oder über ein Adressbuchcontainer Hierarchie oder Inhaltstabelle durch Aufrufen von [IMAPITable::Advise](imapitable-advise.md)registrieren. 
  
Geben Sie den Eintrag Bezeichner eines Adressbuchcontainer, Verteilerliste oder messaging-Benutzer, wenn Sie für Benachrichtigungen auf einen bestimmten Eintrag und NULL registrieren, wenn für Benachrichtigungen auf das gesamte Adressbuch registrieren. Die Eintrags-ID muss es sich um ein messaging-Benutzer oder eine Verteilerliste in einem Adressbuchcontainer darstellen. **IAddrBook::Advise** untersucht dieses Eintrags-ID, um zu bestimmen, welche Adresse Adressbuchanbieter für das entsprechende Objekt zuständig ist, und leitet den Anruf an die entsprechenden-Adressbuchanbieter [IABLogon::Advise](iablogon-advise.md) -Methode. 
  
Clients können für die folgenden Typen von Ereignissen auf Adressbucheinträge registrieren:
  
- Schwerwiegender Fehler
    
- Eines der Objektereignisse (erstellt, geändert, gelöscht, verschoben oder kopiert)
    
- Tabelle geändert
    
In der Regel erfolgt Registrierung nur unter Address Book Containerinhalt und Hierarchietabellen. Es ist nur in seltenen Fällen Clients mit der unteren Ebene messaging Benutzer- und Verteilung List-Objekten zu registrieren. Dies ist, da:
  
- Viele adressbuchanbietern implementierte unterstützen keine Benachrichtigungen ihrer messaging-Benutzern und Verteilerlisten.
    
- Tabelle Benachrichtigungen reichen zum Nachverfolgen von Änderungen und Berichten sie Benutzern zur Verfügung.
    

