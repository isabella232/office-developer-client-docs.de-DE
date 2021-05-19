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
ms.openlocfilehash: ccc2758b59a9227afbc50360102e793892bbdc52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424903"
---
# <a name="registering-for-a-notification"></a>Registrieren für eine Benachrichtigung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Client kann sich im Rahmen seines Initialisierungsprozesses für Adressbuch- oder Nachrichtenspeicherbenachrichtigungen registrieren.
  
MAPI unterstützt Benachrichtigungen im Adressbuch, unabhängig davon, ob dies von adressbuchanbietern unterstützt wird. Die Unterstützung für Benachrichtigungen in Nachrichtenspeichern hängt vom jeweiligen Nachrichtenspeicheranbieter ab. Um zu ermitteln, ob ein bestimmter Nachrichtenspeicheranbieter Benachrichtigungen unterstützt, überprüfen Sie die **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) -Eigenschaft. Wenn der Nachrichtenspeicher Benachrichtigungen unterstützt, wird STORE_NOTIFY_OK festgelegt. 
  
Registrieren Sie sich für Benachrichtigungen, indem Sie die Advise-Methode eines **Advise-Quellobjekts** aufrufen. Viele Objekte implementieren **Advise,** und Clients können sich auf unterschiedliche Weise bei diesen Objekten registrieren. 
  
 **So registrieren Sie sich für eine Benachrichtigung**
  
1. Erstellen Sie ein MAPI advise sink-Objekt, und erhöhen Sie die Referenzanzahl.
    
2. Rufen Sie gegebenenfalls [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) auf, um ein Empfehlungssenke-Objekt zu erstellen, das Ihre ursprüngliche Empfehlungssenke umschließt, und geben Sie dann die ursprüngliche Empfehlungssenke frei. 
    
3. Rufen Sie eine der folgenden **Advise-Methoden auf,** um die Registrierung abzuschließen: 
    
  - Rufen [Sie IMAPISession::Advise auf,](imapisession-advise.md) sich für Sitzungsbenachrichtigungen oder für Benachrichtigungen in einem Adressbuch- oder Nachrichtenspeicherobjekt zu registrieren. 
    
  - Rufen [Sie IAddrBook::Empfehlen,](iaddrbook-advise.md) sich für Adressbuchbenachrichtigungen oder für Benachrichtigungen in einem Messagingbenutzer, Container oder einer Verteilerliste zu registrieren. 
    
  - Rufen [Sie IABLogon::Empfehlen](iablogon-advise.md) Sie, sich direkt bei einem Adressbuchanbieter für Benachrichtigungen in einem Messagingbenutzer, -container oder einer Verteilerliste zu registrieren. 
    
  - Rufen [Sie IMsgStore::Empfehlen, sich](imsgstore-advise.md) für Nachrichtenspeicherbenachrichtigungen oder für Benachrichtigungen in einem Ordner oder einer Nachricht zu registrieren. 
    
  - Rufen [Sie IMSLogon::Advise auf,](imslogon-advise.md) sich direkt bei einem Nachrichtenspeicheranbieter für Benachrichtigungen für einen Ordner oder eine Nachricht zu registrieren. 
    
  - Rufen [Sie IMAPITable::Advise auf, sich](imapitable-advise.md) für Tabellenbenachrichtigungen zu registrieren. 
    
4. Zwischenspeichern der von Advise zurückgegebenen **Verbindungsnummer.**
    
5. Wenn Sie eine umschlossene Ratensenke verwenden, lassen Sie sie los. Nachdem die umschlossene Ratensenke registriert wurde, benötigen Sie sie nicht mehr.
    
Durch Aufrufen ** IMAPISession::Advise ** können Sie sich für kritische Fehlerbenachrichtigungen in der gesamten Sitzung oder für verschiedene Benachrichtigungen für einzelne Objekte registrieren. Sitzungen senden kritische Fehlerbenachrichtigungen an Clients, die bei freigegebenen Sitzungen angemeldet sind, wenn ein anderer Client, der die freigegebene Sitzung verwendet, die [IMAPISession::Logoff-Methode](imapisession-logoff.md) aufruft. Um sich für Sitzungsbenachrichtigungen zu registrieren, übergeben Sie NULL für den Eintrags-ID-Parameter. Um sich für Benachrichtigungen für ein einzelnes Objekt zu registrieren, übergeben Sie den Eintragsbezeichner des Objekts. Die **IMAPISession-Methode** gibt den Aufruf an den entsprechenden Dienstanbieter weiter, wie durch den **MAPIUID-Teil** der Eintrags-ID bestimmt. Das **Aufrufen von IMAPISession::Advise zum** Registrieren für Objektbenachrichtigungen ist einfacher als das Aufrufen der **Advise-Methode** eines Dienstanbieters. 
  
Die Registrierung beim Adressbuch ähnelt der Registrierung bei der Sitzung. Um sich für kritische Fehlerbenachrichtigungen aus dem Adressbuch zu registrieren, übergeben Sie NULL für die Eintrags-ID. Um sich für Benachrichtigungen für ein bestimmtes Adressbuchobjekt zu registrieren, geben Sie die entsprechende Eintrags-ID und das entsprechende Ereignis oder ereignisse an. Beachten Sie, dass viele Adressbuchanbieter keine Benachrichtigungen für einzelne Objekte unterstützen. Stattdessen unterstützen sie Tabellenbenachrichtigungen für ihre Inhalte und Hierarchietabellen. 
  
Es empfiehlt sich, die von Ihnen implementierte oder mit [HrAllocAdviseSink erstellte](hrallocadvisesink.md) Ratensenke sofort nach einer erfolgreichen Rückgabe eines **Advise-Anrufs frei** zu geben. Dies liegt daran, dass Dienstanbieter Ihre Ratgebersenke nach dem **Anruf "Advise"** veröffentlichen können, aber bevor ein **Unadvise-Anruf** erfolgt. Sobald Sie der Ratenquelle einen Zeiger auf Ihre Ratensenke gegeben haben und die Referenzanzahl für diese Ratensenke erhöht wurde, ist es ratsam, sie frei zu geben, es sei denn, Sie haben eine langfristige Verwendung dafür. 
  
> [!NOTE]
> Alle Verbindungsnummern, die gültige Empfehlungsregistrierungen darstellen, werden erst freigegeben, wenn der **Unadvise-Aufruf** erfolgt ist. 
  

