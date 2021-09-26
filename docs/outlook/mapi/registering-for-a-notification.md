---
title: Registrieren für eine Benachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 45625387-dbd2-4ca8-926b-ef87998d01d7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 63b572f6869f36a1de4b6e85962befd998e93549
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624384"
---
# <a name="registering-for-a-notification"></a>Registrieren für eine Benachrichtigung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Client kann sich im Rahmen seines Initialisierungsprozesses für Adressbuch- oder Nachrichtenspeicherbenachrichtigungen registrieren.
  
MAPI unterstützt Benachrichtigungen im Adressbuch, unabhängig davon, ob es von einem der Adressbuchanbieter unterstützt wird. Die Unterstützung für Benachrichtigungen zu Nachrichtenspeichern hängt vom jeweiligen Nachrichtenspeicheranbieter ab. Um festzustellen, ob ein bestimmter Nachrichtenspeicheranbieter Benachrichtigungen unterstützt, überprüfen Sie dessen **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) -Eigenschaft. Wenn der Nachrichtenspeicher Benachrichtigungen unterstützt, wird das STORE_NOTIFY_OK Bit festgelegt. 
  
Registrieren Sie sich für Benachrichtigungen, indem Sie die **Advise-Methode** eines Advise-Quellobjekts aufrufen. Viele Objekte implementieren **Advise,** und Clients können sich auf unterschiedliche Weise bei diesen Objekten registrieren. 
  
 **So registrieren Sie sich für eine Benachrichtigung**
  
1. Erstellen Sie ein MAPI-Empfehlungssenkenobjekt, und erhöhen Sie dessen Referenzanzahl.
    
2. Rufen Sie gegebenenfalls [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) auf, um ein Empfehlungssenkenobjekt zu erstellen, das Ihre ursprüngliche Empfehlungssenke umschließt, und geben Sie dann die ursprüngliche Empfehlungssenke frei. 
    
3. Rufen Sie eine der folgenden **Advise-Methoden** auf, um die Registrierung abzuschließen: 
    
  - Call [IMAPISession::Advise](imapisession-advise.md) to register for session notifications or for notifications on an address book or message store object. 
    
  - Call [IAddrBook::Advise](iaddrbook-advise.md) to register for address book notifications or for notifications on a messaging user, container, or distribution list. 
    
  - Aufrufen von [IABLogon::Empfehlen Sie,](iablogon-advise.md) sich direkt bei einem Adressbuchanbieter für Benachrichtigungen für einen Messagingbenutzer, -container oder eine Verteilerliste zu registrieren. 
    
  - Aufrufen von [IMsgStore::Empfehlen Sie,](imsgstore-advise.md) sich für Nachrichtenspeicherbenachrichtigungen oder für Benachrichtigungen in einem Ordner oder einer Nachricht zu registrieren. 
    
  - Aufrufen von [IMSLogon::Empfehlen Sie,](imslogon-advise.md) sich direkt bei einem Nachrichtenspeicheranbieter für Benachrichtigungen in einem Ordner oder einer Nachricht zu registrieren. 
    
  - Aufrufen [von IMAPITable::Raten Sie,](imapitable-advise.md) sich für Tabellenbenachrichtigungen zu registrieren. 
    
4. Cache the connection number returned from **Advise**.
    
5. Wenn Sie eine umschlossene Empfehlungssenke verwenden, geben Sie sie frei. Sobald die umschlossene Empfehlungssenke registriert ist, benötigen Sie sie nicht mehr.
    
Durch Aufrufen von ** IMAPISession::Advise ** können Sie sich für kritische Fehlerbenachrichtigungen in der allgemeinen Sitzung oder für verschiedene Benachrichtigungen für einzelne Objekte registrieren. Sitzungen senden kritische Fehlerbenachrichtigungen an Clients, die an freigegebenen Sitzungen angemeldet sind, wenn ein anderer Client, der die freigegebene Sitzung verwendet, die [IMAPISession::Logoff-Methode aufruft.](imapisession-logoff.md) Um sich für Sitzungsbenachrichtigungen zu registrieren, übergeben Sie NULL für den Eintrags-ID-Parameter. Um sich für Benachrichtigungen für ein einzelnes Objekt zu registrieren, übergeben Sie den Eintragsbezeichner des Objekts. Die **IMAPISession-Methode** leitet den Aufruf an den entsprechenden Dienstanbieter weiter, wie durch den **MAPIUID-Teil** des Eintragsbezeichners bestimmt. Das Aufrufen von **IMAPISession::Empfehlen,** sich für Objektbenachrichtigungen zu registrieren, ist einfacher als das Aufrufen der **Advise-Methode** eines Dienstanbieters. 
  
Die Registrierung beim Adressbuch ähnelt der Registrierung bei der Sitzung. Um sich für kritische Fehlerbenachrichtigungen aus dem Adressbuch zu registrieren, übergeben Sie NULL für den Eintragsbezeichner. Um sich für Benachrichtigungen für ein bestimmtes Adressbuchobjekt zu registrieren, geben Sie den entsprechenden Eintragsbezeichner und ereignisse oder Ereignisse von Interesse an. Beachten Sie, dass viele Adressbuchanbieter keine Benachrichtigungen für einzelne Objekte unterstützen. Stattdessen unterstützen sie Tabellenbenachrichtigungen für ihre Inhalte und Hierarchietabellen. 
  
Es empfiehlt sich, die Empfehlungssenke freizugeben, die Sie mit [HrAllocAdviseSink](hrallocadvisesink.md) unmittelbar nach einer erfolgreichen Rückgabe von einem **Advise-Aufruf** implementieren oder erstellen. Dies liegt daran, dass es für Dienstanbieter möglich ist, Ihre Empfehlungssenke nach dem **Advise-Aufruf** freizugeben, aber bevor ein **Unadvise-Aufruf** erfolgt. Sobald Sie der Empfehlungsquelle einen Zeiger auf die Empfehlungssenke gegeben haben und die Referenzanzahl für diese Empfehlungssenke erhöht wurde, empfiehlt es sich, sie freizugeben, es sei denn, Sie haben eine langfristige Verwendung dafür. 
  
> [!NOTE]
> Alle Verbindungsnummern, die gültige Empfehlungsregistrierungen darstellen, werden erst freigegeben, wenn der **Unadvise-Aufruf** erfolgt ist. 
  

