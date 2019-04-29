---
title: Behandeln von Adressbuchbenachrichtigungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 122e50328272a4009e5a129233d449613817dfc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413535"
---
# <a name="handing-address-book-notification"></a>Behandeln von Adressbuchbenachrichtigungen
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Adressbuch Benachrichtigungen ermöglichen einem Client das Erlernen von Ereignissen, die für einen Adressbucheintrag oder einen bestimmten Eintrag auftreten. Sie können sich für diese Benachrichtigungen entweder über das MAPI-Adressbuch registrieren, indem Sie [IAddrBook:: Advise](iaddrbook-advise.md) oder die Hierarchie-oder Inhaltstabelle eines Adressbuch Containers aufrufen, indem Sie [IMAPITable:: Advise](imapitable-advise.md)aufrufen. 
  
Geben Sie die Eintrags-ID eines Adressbuch Containers, einer Verteilerliste oder eines Messaging Benutzers an, wenn Sie sich für Benachrichtigungen zu einem bestimmten Eintrag registrieren, und NULL, wenn Sie sich für Benachrichtigungen im gesamten Adressbuch registrieren. Die Eintrags-ID muss einen Messagingbenutzer oder eine Verteilerliste in einem Adressbuchcontainer darstellen. **IAddrBook:: Advise** überprüft diese Eintrags-ID, um zu bestimmen, welcher Adressbuchanbieter für das entsprechende Objekt verantwortlich ist, und leitet den Anruf an die [IABLogon:: Advise](iablogon-advise.md) -Methode des entsprechenden Adressbuch Anbieters weiter. 
  
Clients können sich für die folgenden Ereignistypen bei Adressbucheinträgen registrieren:
  
- Kritischer Fehler
    
- Beliebige Objekt Ereignisse (erstellt, geändert, gelöscht, verschoben oder kopiert)
    
- Tabelle geändert
    
In der Regel erfolgt die Registrierung nur in Adressbuchcontainer-Inhalts-und Hierarchietabellen. Es ist selten, dass Clients sich bei den untergeordneten Messaging-Benutzer-und Verteilerlisten Objekten registrieren. Dies liegt daran, dass:
  
- Viele Adressbuchanbieter unterstützen keine Benachrichtigungen zu ihren Messaging Benutzern und Verteilerlisten.
    
- Tabellen Benachrichtigungen sind ausreichend, um Änderungen nachzuverfolgen und Benutzern zu melden.
    

