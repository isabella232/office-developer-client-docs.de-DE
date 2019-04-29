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
  
Wenn ein Client oder Anbieter angefordert hat, dass eines ihrer Objekte geöffnet werden soll, ruft MAPI die [IABLogon:: OpenEntry](iablogon-openentry.md) -Methode Ihres Anbieters auf. MAPI bestimmt, dass die Eintrags-ID, die das Zielobjekt darstellt, zu Ihrem Anbieter gehört, indem Sie den [MAPIUID](mapiuid.md) -Teil der Eintrags-ID untersuchen und mit dem **MAPIUID** vergleichen, den Ihr Anbieter im Aufruf **von IMAPISupport:: SetProviderUID**. Dann ruft MAPI Ihre **OpenEntry** -Methode auf. Der Anbieter muss Antworten, indem er das entsprechende Objekt (einen Container, eine Verteilerliste oder einen Messagingbenutzer) abruft. 
  
Eine NULL-Eintrags-ID gibt eine Anforderung zum Öffnen des Stammcontainers des Adressbuch Anbieters an. Clients öffnen den Stammcontainer für den Zugriff auf die Hierarchietabelle und die zugehörigen Empfänger. Adressbuchanbieter, die nur Vorlagen zum Erstellen von einmaligen Empfängern bereitstellen, **** unterstützen den OpenEntry-Aufruf für den Stammcontainer nicht. 
  
### <a name="to-implement-iablogonopenentry"></a>So implementieren Sie IABLogon:: openEntry
  
1. Stellen Sie sicher, dass die Eintrags-ID ein gültiger Bezeichner ist, den Ihr Anbieter unterstützt. Wenn es sich nicht um eine gültige Eintrags-ID handelt, geben Sie MAPI_E_INVALID_ENTRYID. 
    
2. Überprüfen Sie das Kennzeichen, das mit dem _ulFlags_ -Parameter übergeben wird. Wenn MAPI in MAPI_MODIFY übergeben hat und Ihr Anbieter nicht zulässt, dass seine Objekte geändert werden können, schlagen Sie fehl, und geben Sie den MAPI_E_ACCESS_DENIED-Fehlerwert zurück. 
    
3. Überprüfen Sie, ob die im _lpInterface_ -Parameter angeforderte Schnittstelle für den Objekttyp gültig ist, den Ihr Anbieter öffnen muss. Wenn ein ungültiger Parameter übergeben wurde, schlagen Sie fehl, und geben Sie den MAPI_E_INTERFACE_NOT_SUPPORTED-Fehlerwert zurück. 
    
4. Wenn der _cbEntryID_ -Parameter NULL ist, ist dies eine Anforderung zum Öffnen des Stammcontainers Ihres Anbieters. Erstellen Sie den Stammcontainer, und geben Sie einen Zeiger auf die Implementierung der **IABContainer** -Schnittstelle zurück. 
    
5. Wenn Ihr Anbieter mehrere Anmeldeobjekte implementiert, die jeweils über eine eigene registrierte **MAPIUID**verfügen, ordnen Sie die in der Eintrags-ID enthaltenen **MAPIUID** mit dem entsprechenden Logon-Objekt zu. 
    
6. Bestimmen Sie, welcher Objekttyp der Eintragsbezeichner darstellt: ein Messagingbenutzer, eine Verteilerliste oder ein Container, die zu Ihrem Anbieter oder einem einmaligen Messagingbenutzer oder einer Verteilerliste gehören, damit der entsprechende Wert für die _lpulObjectType_ festgelegt werden kann. Parameter. 
    
7. Erstellen Sie das Objekt des entsprechenden Typs, und legen Sie die folgenden grundlegenden Eigenschaften fest:
    
    - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    - **PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))
    - **PR_ADDRTYPE** ([Pidtagaddresstype (](pidtagaddresstype-canonical-property.md))
    
8. Berechnen Sie **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) und **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) aus Informationen in der Eintrags-ID.
    
9. Zurückgeben eines Zeigers auf die Schnittstellenimplementierung für das Objekt. 
    

