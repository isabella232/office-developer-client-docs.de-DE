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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328406"
---
# <a name="registering-for-a-notification"></a>Registrieren für eine Benachrichtigung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Client kann im Rahmen seines Initialisierungsvorgangs für Adressbuch-oder Nachrichtenspeicher Benachrichtigungen registrieren.
  
MAPI unterstützt Benachrichtigungen im Adressbuch, unabhängig davon, ob der Adressbuchanbieter Sie unterstützt. Die Unterstützung für Benachrichtigungen in Nachrichtenspeicher hängt vom jeweiligen Nachrichtenspeicher Anbieter ab. Um zu ermitteln, ob ein bestimmter Nachrichtenspeicher Anbieter Benachrichtigungen unterstützt, überprüfen Sie die **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft. Wenn der Nachrichtenspeicher Benachrichtigungen unterstützt, wird das STORE_NOTIFY_OK-Bit festgelegt. 
  
Registrieren Sie sich für Benachrichtigungen, indem Sie die **Advise** -Methode eines Advise-Quellobjekts aufrufen. Viele Objekte implementieren **Advise** und Clients können sich auf verschiedene Arten bei diesen Objekten registrieren. 
  
 **So registrieren Sie sich für eine Benachrichtigung**
  
1. Erstellen Sie ein MAPI-Advise-Objekt, und erhöhen Sie den Verweiszähler.
    
2. Rufen Sie gegebenenfalls [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) auf, um ein Advise-Senke-Objekt zu erstellen, das Ihre ursprüngliche Advise-Senke umschließt, und geben Sie dann die ursprüngliche Beratungs Senke frei.. 
    
3. Rufen Sie eine der folgenden **** Methoden zum Abschließen der Registrierung auf: 
    
  - Rufen Sie [IMAPISession:: Advise](imapisession-advise.md) an, um sich für Sitzungs Benachrichtigungen oder für Benachrichtigungen in einem Adressbuch-oder Nachrichtenspeicherobjekt zu registrieren. 
    
  - Call [IAddrBook:: Advise](iaddrbook-advise.md) to Register for Address Book notifications or for Notifications on a Messaging User, Container, or Distribution List. 
    
  - Rufen Sie [IABLogon:: Raten](iablogon-advise.md) Sie auf, sich direkt bei einem Adressbuchanbieter für Benachrichtigungen für einen Messagingbenutzer,-Container oder eine Verteilerliste zu registrieren. 
    
  - Rufen Sie [IMsgStore:: Advise](imsgstore-advise.md) an, um Benachrichtigungen für Nachrichtenspeicher oder Benachrichtigungen für einen Ordner oder eine Nachricht zu registrieren. 
    
  - Rufen Sie [IMSLogon:: Raten](imslogon-advise.md) Sie auf, sich direkt bei einem Nachrichtenspeicher Anbieter für Benachrichtigungen zu einem Ordner oder einer Nachricht zu registrieren. 
    
  - Rufen Sie [IMAPITable:: Advise](imapitable-advise.md) auf, um Tabellen Benachrichtigungen zu registrieren. 
    
4. Zwischenspeichern der von **Advise**zurückgegebenen Verbindungsnummer.
    
5. Wenn Sie eine verpackte Advise-Senke verwenden, lassen Sie sie los. Nachdem die eingebundene Advise-Senke registriert wurde, benötigen Sie Sie nicht mehr.
    
Durch Aufrufen von * * IMAPISession:: Advise * * können Sie sich für kritische Fehlerbenachrichtigungen in der Gesamt Sitzung oder für verschiedene Benachrichtigungen für einzelne Objekte registrieren. Sitzungen senden wichtige Fehlerbenachrichtigungen an Clients, die bei freigegebenen Sitzungen angemeldet sind, wenn ein anderer Client, der die freigegebene Sitzung verwendet, die [IMAPISession:: Abmelde](imapisession-logoff.md) Methode aufruft. Um sich für Sitzungs Benachrichtigungen zu registrieren, übergeben Sie NULL für den Parameter Entry Identifier. Um Benachrichtigungen für ein einzelnes Objekt zu registrieren, müssen Sie die Eintrags-ID des Objekts weiterleiten. Die **IMAPISession** -Methode leitet den Aufruf an den entsprechenden Dienstanbieter weiter, der durch den **MAPIUID** -Teil der Eintrags-ID bestimmt wird. Das Aufrufen von **IMAPISession:: Advise** to Register for Object Notifications ist einfacher als das Aufrufen der **Advise** -Methode eines Dienstanbieters. 
  
Die Registrierung beim Adressbuch ähnelt der Registrierung für die Sitzung. Wenn Sie sich für eine kritische Fehlerbenachrichtigung aus dem Adressbuch registrieren möchten, führen Sie NULL für die Eintrags-ID aus. Um Benachrichtigungen für ein bestimmtes Adressbuchobjekt zu registrieren, geben Sie die entsprechende Eintrags-ID und das Ereignis oder die Ereignisse von Interesse an. Beachten Sie, dass viele Adressbuchanbieter Benachrichtigungen für einzelne Objekte nicht unterstützen. Sie unterstützen vielmehr Tabellen Benachrichtigungen für Ihre Inhalts-und Hierarchietabellen. 
  
Es empfiehlt sich, die Advise-Senke, die Sie mit [HrAllocAdviseSink](hrallocadvisesink.md) implementieren oder erstellen, unmittelbar nach einer erfolgreichen Rückkehr aus einem **Advise** -Aufruf zu veröffentlichen. Dies liegt daran, dass Dienstanbieter Ihre Advise-Senke nach dem **Advise** -Aufruf freigeben können, aber bevor **** ein Unadvise-Anruf getätigt wird. Sobald Sie der Advise-Quelle einen Zeiger auf Ihre Advise-Senke gegeben haben und die Referenzanzahl für diese Advise-Senke erhöht wurde, ist es ratsam, Sie freizugeben, es sei denn, Sie haben eine langfristige Verwendung dafür. 
  
> [!NOTE]
> Alle Verbindungsnummern, die gültige Beratungs Registrierungen darstellen, werden erst freigegeben **** , wenn der Unadvise-Aufruf erfolgt ist. 
  

