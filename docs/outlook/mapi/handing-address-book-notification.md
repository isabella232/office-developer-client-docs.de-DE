---
title: Behandeln von Adressbuchbenachrichtigungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a5d3114d3aa01ec20783393b7831f7c661f65adf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551534"
---
# <a name="handing-address-book-notification"></a>Behandeln von Adressbuchbenachrichtigungen
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Adressbuchbenachrichtigungen ermöglichen es einem Client, über Ereignisse zu erfahren, die bei einem Adressbucheintrag oder einem bestimmten Eintrag auftreten. Sie können sich für diese Benachrichtigungen entweder über das MAPI-Adressbuch registrieren, indem Sie [IAddrBook::Advise](iaddrbook-advise.md) aufrufen, oder über die Hierarchie oder das Inhaltsverzeichnis eines Adressbuchcontainers, indem [Sie IMAPITable::Advise](imapitable-advise.md)aufrufen. 
  
Geben Sie den Eintragsbezeichner eines Adressbuchcontainers, einer Verteilerliste oder eines Messagingbenutzers an, wenn Sie sich für Benachrichtigungen für einen bestimmten Eintrag registrieren, und NULL, wenn Sie sich für Benachrichtigungen im gesamten Adressbuch registrieren. Der Eintragsbezeichner muss einen Messagingbenutzer oder eine Verteilerliste in einem Adressbuchcontainer darstellen. **IAddrBook::Advise** untersucht diesen Eintragsbezeichner, um zu ermitteln, welcher Adressbuchanbieter für das entsprechende Objekt verantwortlich ist, und leitet den Aufruf an die [IABLogon::Advise-Methode](iablogon-advise.md) des entsprechenden Adressbuchanbieters weiter. 
  
Clients können sich für die folgenden Ereignistypen für Adressbucheinträge registrieren:
  
- Kritischer Fehler
    
- Eines der Objektereignisse (erstellt, geändert, gelöscht, verschoben oder kopiert)
    
- Tabelle geändert
    
In der Regel erfolgt die Registrierung nur für Adressbuchcontainerinhalte und Hierarchietabellen. Es ist selten, dass Clients sich bei den Nachrichtenbenutzer- und Verteilerlistenobjekten auf niedrigerer Ebene registrieren. Dies liegt daran:
  
- Viele Adressbuchanbieter unterstützen keine Benachrichtigungen für ihre Messagingbenutzer und Verteilerlisten.
    
- Tabellenbenachrichtigungen sind ausreichend, um Änderungen nachzuverfolgen und sie benutzern zu melden.
    

