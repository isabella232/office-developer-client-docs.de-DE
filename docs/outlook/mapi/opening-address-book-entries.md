---
title: Öffnen von Adressbucheinträgen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 017a62c0-49c6-47fb-acce-db58e6bb9cc5
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c36c70eacffcb4a41af0e73eea85143ab737867f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793318"
---
# <a name="opening-address-book-entries"></a>Öffnen von Adressbucheinträgen

**Betrifft**: Outlook 
  
MAPI Ihres Anbieters [IABLogon::OpenEntry](iablogon-openentry.md) Methode aufgerufen, wenn ein Client oder Anbieter angefordert hat, dass eines Ihrer Objekte geöffnet werden. MAPI bestimmt, dass die Eintrags-ID, das Zielobjekt darstellt, die an Ihren Anbieter durch Untersuchen des [MAPIUID](mapiuid.md) Teils die Eintrags-ID und an die **MAPIUID** , die vom Dienstanbieter im Aufruf **registriert übereinstimmende gehört IMAPISupport::SetProviderUID**. MAPI ruft dann die **OpenEntry** -Methode. Vom Dienstanbieter muss durch Abrufen des entsprechenden-Objekts reagieren – eine Container, Verteilerliste oder messaging-Benutzer. 
  
Eine NULL-Eintrags-ID gibt eine Anforderung zum Öffnen der Adressbuchanbieter Stammcontainer. Clients öffnen Sie im Stamm der Hierarchietabelle und deren Empfänger für den Zugriff. Von adressbuchanbietern implementierte, die nur Vorlagen zum Erstellen von einmaligen Empfänger angeben unterstützt den Anruf **OpenEntry** nicht für den Container Root. 
  
### <a name="to-implement-iablogonopenentry"></a>Implementieren von IABLogon::OpenEntry
  
1. Überprüfen Sie, dass die Eintrags-ID ein gültiger Bezeichner ist, den vom Anbieter unterstützt. Wenn es sich nicht um eine gültige Eintrags-ID ist, geben Sie MAPI_E_INVALID_ENTRYID zurück. 
    
2. Überprüfen Sie die Kennzeichen, die sich mit der _UlFlags_ -Parameter übergeben wird. Wenn MAPI in MAPI_MODIFY verstrichen ist und vom Dienstanbieter lässt sich nicht auf seine Objekte geändert werden soll, ein Fehler auftritt, und geben Sie den Fehlerwert MAPI_E_ACCESS_DENIED zurück. 
    
3. Überprüfen Sie, dass die im Parameter _LpInterface_ angeforderte Schnittstelle für den Typ des Objekts gültig ist, die zum Öffnen des Anbieters aufgefordert wurde. Wenn in ein ungültiger Parameter übergeben wurde, wird ein Fehler auftritt, und geben Sie den Fehlerwert MAPI_E_INTERFACE_NOT_SUPPORTED zurück. 
    
4. Wenn der Parameter _CbEntryID_ gleich NULL ist, ist dies eine Anforderung zum Öffnen des Anbieters Stammcontainer. Erstellen Sie den Stammcontainer, und zurückgegeben Sie ein Zeiger auf die Implementierung eines **IABContainer** . 
    
5. Wenn der Anbieter mehrere Logon-Objekten implementiert, registriert jeweils mit eigenem **MAPIUID**, Zuordnung, in der **MAPIUID** die Eintrags-ID mit dem entsprechenden Anmeldung-Objekt enthalten. 
    
6. Bestimmen, welche Art des Objekts darstellt, die Eintrags-ID: messaging Benutzer, Verteilerliste oder Container, die auf Ihrem Anbieter oder eine einmalige messaging Benutzer oder eine Verteilergruppe gehören, damit Sie der entsprechende Wert für die _LpulObjectType_ festgelegt werden kann der Parameter. 
    
7. Erstellen Sie das Objekt des entsprechenden Typs, und legen Sie die folgenden grundlegenden Eigenschaften:
    
    - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    - **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
8. Berechnen Sie anhand der Informationen in die Eintrags-ID **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) und **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
    
9. Ein Zeiger auf die schnittstellenimplementierung für das Objekt zurückgegeben. 
    

