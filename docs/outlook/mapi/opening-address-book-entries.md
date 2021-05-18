---
title: Öffnen von Adressbucheinträgen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 017a62c0-49c6-47fb-acce-db58e6bb9cc5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6ebd6009700742e9b1159bc95ff0496c423e512c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422159"
---
# <a name="opening-address-book-entries"></a>Öffnen von Adressbucheinträgen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn ein Client oder Anbieter das Öffnen eines Ihrer Objekte angefordert hat, ruft MAPI die [IABLogon::OpenEntry-Methode](iablogon-openentry.md) Ihres Anbieters auf. MAPI bestimmt, dass der Eintragsbezeichner, der das Zielobjekt darstellt, zu Ihrem Anbieter gehört, indem sie den [MAPIUID-Teil](mapiuid.md) der Eintrags-ID untersucht und mit der **MAPIUID** abgleicht, die Ihr Anbieter im Aufruf von **IMAPISupport::SetProviderUID** registriert hat. MAPI ruft dann Ihre **OpenEntry-Methode** auf. Ihr Anbieter muss antworten, indem er das entsprechende Objekt abruft – einen Container, eine Verteilerliste oder einen Messagingbenutzer. 
  
Ein NULL-Eintragsbezeichner gibt eine Anforderung zum Öffnen des Stammcontainers des Adressbuchanbieters an. Clients öffnen den Stammcontainer, um auf seine Hierarchietabelle und ihre Empfänger zu zugreifen. Adressbuchanbieter, die nur Vorlagen zum Erstellen von Einmalempfängern angeben, unterstützen den **OpenEntry-Aufruf** für den Stammcontainer nicht. 
  
### <a name="to-implement-iablogonopenentry"></a>So implementieren Sie IABLogon::OpenEntry
  
1. Überprüfen Sie, ob es sich bei der Eintrags-ID um einen gültigen Bezeichner handelt, den Ihr Anbieter unterstützt. Wenn es sich nicht um einen gültigen Eintragsbezeichner handelt, geben Sie MAPI_E_INVALID_ENTRYID. 
    
2. Überprüfen Sie das Flag, das mit dem  _ulFlags-Parameter übergeben_ wird. Wenn MAPI die MAPI_MODIFY übergeben hat und Ihr Anbieter die Änderung der Objekte nicht zusent lässt, führen Sie einen Fehler aus, und geben Sie den MAPI_E_ACCESS_DENIED zurück. 
    
3. Überprüfen Sie, ob die im  _lpInterface-Parameter_ angeforderte Schnittstelle für den Objekttyp gültig ist, den Ihr Anbieter öffnen soll. Wenn ein ungültiger Parameter übergeben wurde, führen Sie einen Fehler aus, und geben Sie den MAPI_E_INTERFACE_NOT_SUPPORTED zurück. 
    
4. Wenn der  _cbEntryID-Parameter_ null ist, ist dies eine Anforderung zum Öffnen des Stammcontainers Ihres Anbieters. Erstellen Sie den Stammcontainer, und geben Sie einen Zeiger auf die **IABContainer-Schnittstellenimplementierung** zurück. 
    
5. Wenn Ihr Anbieter mehrere Anmeldeobjekte implementiert, die jeweils über eine eigene registrierte **MAPIUID** verfügen, ordnen Sie die im Eintragsbezeichner enthaltene **MAPIUID** dem entsprechenden Anmeldeobjekt zu. 
    
6. Bestimmen Sie, welcher Objekttyp der Eintragsbezeichner darstellt: ein Messagingbenutzer, eine Verteilerliste oder ein Container, der zu Ihrem Anbieter gehört, oder einen one-off-Messagingbenutzer oder eine Verteilerliste, damit der entsprechende Wert für den  _lpulObjectType-Parameter_ festgelegt werden kann. 
    
7. Erstellen Sie das Objekt des entsprechenden Typs, und legen Sie die folgenden grundlegenden Eigenschaften ein:
    
    - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    - **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
8. Berechnen **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) und **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) aus Informationen in der Eintrags-ID.
    
9. Gibt einen Zeiger auf die Schnittstellenimplementierung für das Objekt zurück. 
    

