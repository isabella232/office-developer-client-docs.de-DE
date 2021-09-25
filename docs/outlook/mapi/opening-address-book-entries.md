---
title: Öffnen von Adressbucheinträgen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 017a62c0-49c6-47fb-acce-db58e6bb9cc5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f18ba37549f0ea6ee1a4dfa4028fb71289bae274
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600729"
---
# <a name="opening-address-book-entries"></a>Öffnen von Adressbucheinträgen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn ein Client oder Anbieter das Öffnen eines Ihrer Objekte angefordert hat, ruft MAPI die [IABLogon::OpenEntry-Methode](iablogon-openentry.md) Ihres Anbieters auf. MAPI ermittelt, dass der Eintragsbezeichner, der das Zielobjekt darstellt, zu Ihrem Anbieter gehört, indem der [MAPIUID-Teil](mapiuid.md) des Eintragsbezeichners untersucht und mit der **MAPIUID** übereinstimmt, die Ihr Anbieter im Aufruf von **IMAPISupport::SetProviderUID** registriert hat. MAPI ruft dann die **OpenEntry-Methode** auf. Ihr Anbieter muss antworten, indem er das entsprechende Objekt – einen Container, eine Verteilerliste oder einen Messaging-Benutzer – abruft. 
  
Ein NULL-Eintragsbezeichner gibt eine Anforderung zum Öffnen des Stammcontainers des Adressbuchanbieters an. Clients öffnen den Stammcontainer, um auf seine Hierarchietabelle und seine Empfänger zuzugreifen. Adressbuchanbieter, die nur Vorlagen zum Erstellen von einmaligen Empfängern bereitstellen, unterstützen den **OpenEntry-Aufruf** für den Stammcontainer nicht. 
  
### <a name="to-implement-iablogonopenentry"></a>So implementieren Sie IABLogon::OpenEntry
  
1. Überprüfen Sie, ob der Eintragsbezeichner ein gültiger Bezeichner ist, den Ihr Anbieter unterstützt. Wenn es sich nicht um einen gültigen Eintragsbezeichner handelt, geben Sie MAPI_E_INVALID_ENTRYID zurück. 
    
2. Überprüfen Sie das Flag, das mit dem  _ulFlags-Parameter_ übergeben wird. Wenn die MAPI MAPI_MODIFY übergeben hat und ihr Anbieter das Ändern seiner Objekte nicht zulässt, schlagen Sie fehl, und geben Sie den MAPI_E_ACCESS_DENIED Fehlerwert zurück. 
    
3. Überprüfen Sie, ob die im  _lpInterface-Parameter_ angeforderte Schnittstelle für den Objekttyp gültig ist, zu dem Ihr Anbieter aufgefordert wurde, es zu öffnen. Wenn ein ungültiger Parameter übergeben wurde, schlagen Sie fehl, und geben Sie den MAPI_E_INTERFACE_NOT_SUPPORTED Fehlerwert zurück. 
    
4. Wenn der  _parameter cbEntryID_ null ist, ist dies eine Anforderung zum Öffnen des Stammcontainers Ihres Anbieters. Erstellen Sie den Stammcontainer, und geben Sie einen Zeiger auf die Implementierung der **IABContainer-Schnittstelle** zurück. 
    
5. Wenn Ihr Anbieter mehrere Anmeldeobjekte implementiert, jedes mit einer eigenen registrierten **MAPIUID,** ordnen Sie die **MAPIUID,** die im Eintragsbezeichner enthalten ist, dem entsprechenden Anmeldeobjekt zu. 
    
6. Bestimmen Sie den Typ des Objekts, den der Eintragsbezeichner darstellt: einen Messagingbenutzer, eine Verteilerliste oder einen Container, der zu Ihrem Anbieter gehört, oder einen einmaligen Messagingbenutzer oder eine Verteilerliste, sodass der entsprechende Wert für den  _lpulObjectType-Parameter_ festgelegt werden kann. 
    
7. Erstellen Sie das Objekt des entsprechenden Typs, und legen Sie die folgenden grundlegenden Eigenschaften fest:
    
    - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    - **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
8. Berechnen **sie PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) und **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) aus Informationen im Eintragsbezeichner.
    
9. Gibt einen Zeiger auf die Schnittstellenimplementierung für das Objekt zurück. 
    

