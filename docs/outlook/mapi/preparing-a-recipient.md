---
title: Vorbereiten eines Empfängers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9573f10c-66e1-4e87-93f0-89687e906b8b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 51241009262471bf30f7d71e3108b896bbce8df7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795306"
---
# <a name="preparing-a-recipient"></a>Vorbereiten eines Empfängers

  
  
**Betrifft**: Outlook 
  
Eine Clientanwendung vorbereitet Empfänger ihre kurzfristige-Eintragsbezeichner in langfristige-Eintragsbezeichner konvertieren und möglicherweise hinzufügen, ändern oder Neuanordnen von Eigenschaften. Sie können die Empfänger an, die sind Bestandteil einer Empfängerliste für eine Nachricht oder Empfänger, die nicht im Zusammenhang mit einer Nachricht sind vorbereiten. In der Regel rufen Clients [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) direkt um kurzfristige-Eintragsbezeichner in langfristige-Eintragsbezeichner für Empfänger zu übersetzen, die im Dialogfeld allgemeine Adresse enthalten sind. Für den Empfänger an, die eine ausgehende Nachricht zugeordnet sind, wird die Empfänger zur Vorbereitung von Vorgang der Lösung behandelt. 
  
Rufen Sie auf, um eine Liste von Empfängern vorzubereiten, **IAddrBook::PrepareRecips**. **PrepareRecips** akzeptiert eine [ADRLIST](adrlist.md) -Struktur und eine Liste der Eigenschaftentags. Die **ADRLIST** -Datenstruktur enthält die Empfänger vorbereitet werden, während die Eigenschaftenliste Tag Eigenschaften darstellt, die jeden Empfänger unterstützt werden sollen. **PrepareRecips** versucht, die Eigenschaften, die in der Eigenschaftenliste Tag am Anfang der Struktur **ADRLIST** enthalten sind. Wenn eine der Eigenschaften in der Liste aus der Struktur **ADRLIST** fehlen, ruft MAPI--Adressbuchanbieter, um diese bereitgestellt werden. Wenn Sie nur für langfristige-Eintragsbezeichner überprüfen möchten, übergeben Sie NULL für den Parameter _LpSPropTagArray_ . 
  
Angenommen Sie, dass Sie mit fünf Empfänger arbeiten. Alle fünf Empfänger in der **ADRLIST** -Struktur mit den folgenden Eigenschaften in der folgenden Reihenfolge angezeigt werden: 
  
1. **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
2. **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
3. **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
4. **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
5. **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
In der Struktur **ADRLIST** sind drei weitere Eigenschaften für die ersten beiden Empfänger enthalten. 
  
1. **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))
    
2. **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))
    
3. **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))
    
Da alle Empfänger benötigen, als die ersten drei Eigenschaften **PR_ADDRTYPE** **PR_ENTRYID**und **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), ein Tag-Array-Eigenschaft mit folgenden Eigenschaften erstellen und übergeben Sie und die zu **PrepareRecips** **ADRLIST** -Struktur. **PrepareRecips** ruft jeden Empfänger **IMAPIProp::GetProps** -Methode, um **PR_HOME_TELEPHONE_NUMBER** abzurufen, da es nicht Teil der Struktur **ADRLIST** festgelegt ist. Wenn **PrepareRecips** zurückgegeben wird, stellt die Empfängerliste eine Liste von Empfängern mit den Eigenschaften der **ADRLIST** -Struktur wie folgt aussehen für jeden Empfänger enthalten. 
  
Die Empfängerliste für Empfänger 1 und 2 enthält die Eigenschaften in der folgenden Reihenfolge:
  
1. **PR_ADDRTYPE**
    
2. **PR_ENTRYID**
    
3. **PR_HOME_TELEPHONE_NUMBER**
    
4. **PR_DISPLAY_NAME**
    
5. **PR_SEARCH_KEY**
    
6. **PR_EMAIL_ADDRESS**
    
7. **PR_ADDRTYPE**
    
8. **PR_ACCOUNT**
    
9. **PR_GIVEN_NAME**
    
10. **PR_SURNAME**
    
Die Empfängerliste für Empfänger 3, 4 und 5 enthält die Eigenschaften in der folgenden Reihenfolge:
  
1. **PR_ADDRTYPE**
    
2. **PR_ENTRYID**
    
3. **PR_HOME_TELEPHONE_NUMBER**
    
4. **PR_DISPLAY_NAME**
    
5. **PR_SEARCH_KEY**
    
6. **PR_EMAIL_ADDRESS**
    
7. **PR_ADDRTYPE**
    
Rufen Sie als Alternative zum Aufrufen von **IAddrBook::PrepareRecips** arbeiten mit Eigenschaften des Empfängers [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode und, falls erforderlich, dessen [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode. Wenn nur ein Empfänger beteiligt ist, ist ein der Verfahren Standardkontingente. Jedoch, wenn mehrere Empfänger beteiligt sind, **PrepareRecips** statt der **IMAPIProp** Methoden Aufrufen der Beschleunigung und, falls Sie viele Remoteprozeduraufrufe remote ausgeführt werden. **PrepareRecips** verarbeitet alle Empfänger in einem einzigen Aufruf während **GetProps** und **SetProps** tätigen Sie einen Anruf für jeden Empfänger. 
  

