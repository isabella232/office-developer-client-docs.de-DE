---
title: Registrieren für eine Benachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 45625387-dbd2-4ca8-926b-ef87998d01d7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5a35add66fb685b3c17464269456edf6b456711e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570212"
---
# <a name="registering-for-a-notification"></a>Registrieren für eine Benachrichtigung

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ein Client kann als Teil der Initialisierungsprozesses für Address Book oder einer Nachricht Store Benachrichtigungen registrieren.
  
MAPI unterstützt Benachrichtigung auf das Adressbuch, unabhängig davon, ob eines der adressbuchanbietern implementierte unterstützen. Unterstützung für die Benachrichtigung auf Nachrichtenspeicher hängt von dem Anbieter für bestimmte Nachricht anmelden. Überprüfen Sie die **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft, um zu bestimmen, ob eine bestimmte Nachricht Speicheranbieter Benachrichtigungen unterstützt. Wenn der Nachrichtenspeicher Benachrichtigungen unterstützt, wird das Bit STORE_NOTIFY_OK festgelegt. 
  
Registrieren Sie sich für Benachrichtigungen, durch eine Advise-Quellobjekt **Advise** -Methode aufrufen. Viele Objekte **Advise** implementieren, und Clients können mit diesen Objekten in verschiedene Arten registrieren. 
  
 **Registrieren für eine Benachrichtigung**
  
1. Erstellen von MAPI advise-Empfängerobjekt und erhöht den Referenzzähler.
    
2. Gegebenenfalls [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) um ein Advise-Empfängerobjekt zu erstellen, der Ihrer ursprünglichen Advise-Empfänger umbrochen wird und dann den ursprünglichen Empfänger Ratschläge für die Version. 
    
3. Rufen Sie eine der folgenden Methoden **Advise** zur Durchführung der Registrierung: 
    
  - Rufen Sie [IMAPISession::Advise](imapisession-advise.md) für Sitzung Benachrichtigungen oder für Benachrichtigungen für ein Objekt Address Book oder einer Nachricht Store zu registrieren. 
    
  - Rufen Sie [IAddrBook::Advise](iaddrbook-advise.md) für Address Book Benachrichtigungen oder für Benachrichtigungen messaging Benutzer, Container oder Verteilung Liste zu registrieren. 
    
  - Rufen Sie [IABLogon::Advise](iablogon-advise.md) direkt mit Adressbuch-Dienstanbieter für Benachrichtigungen messaging Benutzer, Container oder Verteilung Liste registrieren. 
    
  - Rufen Sie [IMsgStore::Advise](imsgstore-advise.md) für Benachrichtigungen über Textnachrichten Store oder für Benachrichtigungen auf einen Ordner oder eine Nachricht zu registrieren. 
    
  - Rufen Sie [IMSLogon::Advise](imslogon-advise.md) direkt mit einem Message-Anbieter für Benachrichtigungen auf einen Ordner oder eine Nachricht zu registrieren. 
    
  - Rufen Sie [IMAPITable::Advise](imapitable-advise.md) für Tabelle Benachrichtigungen registriert. 
    
4. Zwischenspeichern von **Advise**zurückgegebene Verbindungsnummer.
    
5. Wenn Sie eine gepackten Advise-Empfänger verwenden, freigeben. Sobald der gepackten Advise-Empfänger registriert ist, werden nicht mehr es benötigen.
    
Aufrufen von ** IMAPISession::Advise ** können Sie für kritische Fehler Benachrichtigungen auf die gesamte Sitzung oder für verschiedene Benachrichtigungen für einzelne Objekte zu registrieren. Sitzungen senden Schwerwiegender Fehler Benachrichtigungen an Clients angemeldet sind auf freigegebene Sitzungen, wenn ein anderer Client mit freigegebenen Sitzung die [IMAPISession::Logoff](imapisession-logoff.md) -Methode aufruft. Um für die Sitzung Benachrichtigungen zu registrieren, übergeben Sie NULL für den Eintrag ID-Parameter. Übergeben Sie zum Registrieren für Benachrichtigungen auf ein einzelnes Objekt Eintrags-ID für das Objekt. Die **IMAPISession** -Methode leitet den Anruf an den entsprechenden Dienstanbieter, wie durch den **MAPIUID** Teil der Eintrags-ID bestimmt. Aufrufen von **IMAPISession::Advise** für Objekt Benachrichtigungen registriert ist einfacher als einem Dienstanbieter **Advise** -Methode aufrufen. 
  
Registrieren mit dem Adressbuch ähnelt dem Registrieren mit der Sitzung. Zum Registrieren für kritische Fehler Benachrichtigung aus dem Adressbuch, übergeben Sie NULL für die Eintrags-ID ein. Geben Sie zum Registrieren für Benachrichtigungen für ein bestimmtes Adresse Adressbuch-Objekt der entsprechenden Eintrags-ID und das Ereignis oder die Ereignisse von Interesse. Beachten Sie, dass viele adressbuchanbietern implementierte Benachrichtigungen nicht für einzelne Objekte unterstützen. Vielmehr unterstützen sie die Tabelle Benachrichtigungen auf ihren Inhalt und Hierarchietabellen. 
  
Es wird empfohlen freizugebende Advise-Empfänger, den Sie implementieren, oder erstellen Sie mit [HrAllocAdviseSink](hrallocadvisesink.md) sofort nach dem erfolgreichen Beenden von einem **Advise** -Aufruf. Dies ist, da es ist möglich für Dienstanbieter Advise-Empfänger nach dem Aufruf der **Advise** -Version, aber bevor ein **Unadvise** wird aufgerufen. Nachdem Sie der Advise-Quelle einen Zeiger, an der Advise-Empfänger gegeben haben und der Referenzzähler wurde auf diese Advise-Empfänger inkrementiert, ist es empfehlenswert, die sie freigeben, es sei denn, Sie haben eine langfristige dafür verwenden. 
  
> [!NOTE]
> Alle Verbindung Zahlen, die gültige Advise Registrierungen darstellen werden nicht freigegeben werden, bis der Anruf **Unadvise** hergestellt wird. 
  

