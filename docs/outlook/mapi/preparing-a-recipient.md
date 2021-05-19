---
title: Vorbereiten eines Empfängers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9573f10c-66e1-4e87-93f0-89687e906b8b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bb6bc8b8d0199ab07d5dad353dbc25da240593e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419877"
---
# <a name="preparing-a-recipient"></a>Vorbereiten eines Empfängers

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Clientanwendung bereitet Empfänger vor, indem sie ihre kurzfristigen Eintragsbezeichner in langfristige Eintragsbezeichner konvertieren und möglicherweise Eigenschaften hinzufügen, ändern oder neu anordnen. Sie können Empfänger vorbereiten, die Teil einer Empfängerliste sind, für eine Nachricht oder Empfänger, die nicht mit einer Nachricht in Zusammenhang stehen. In der Regel rufen Clients [IAddrBook::P repareRecips](iaddrbook-preparerecips.md) direkt auf, um bezeichner für kurzfristige Eingaben in langfristige Eintragsbezeichner für Empfänger zu übersetzen, die im Dialogfeld allgemeine Adresse enthalten sind. Bei Empfängern, die einer ausgehenden Nachricht zugeordnet sind, wird die Empfängervorbereitung durch den Namensauflösungsprozess behandelt. 
  
Um eine Liste der Empfänger vorzubereiten, rufen Sie **IAddrBook::P repareRecips auf.** **PrepareRecips** akzeptiert eine [ADRLIST-Struktur](adrlist.md) und eine Liste von Eigenschaftstags. Die **ADRLIST-Struktur** enthält die empfänger, die vorbereitet werden sollen, während die Eigenschaftstagliste Eigenschaften darstellt, die von jedem Empfänger unterstützt werden sollen. **PrepareRecips** versucht, die Eigenschaften, die in der Eigenschaftstagliste enthalten sind, am Anfang der **ADRLIST-Struktur zu** platzieren. Wenn eine der Eigenschaften in der Liste in der **ADRLIST-Struktur** fehlt, ruft MAPI den Adressbuchanbieter auf, diese zu liefern. Wenn Sie nur nach langfristigen Eintragsbezeichnern suchen müssen, übergeben Sie NULL für den _lpSPropTagArray-Parameter._ 
  
Angenommen, Sie arbeiten mit fünf Empfängern. Alle fünf Empfänger werden in der **ADRLIST-Struktur** mit den folgenden Eigenschaften in der folgenden Reihenfolge angezeigt: 
  
1. **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
2. **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
3. **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
4. **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
5. **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
Drei weitere Eigenschaften sind in der **ADRLIST-Struktur** für die ersten beiden Empfänger enthalten. 
  
1. **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))
    
2. **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))
    
3. **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))
    
Da alle Empfänger als erste drei Eigenschaften **PR_ADDRTYPE**, **PR_ENTRYID** und **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)) verfügen müssen, erstellen Sie ein Eigenschaftentagarray mit diesen Eigenschaften und übergeben es und die **ADRLIST-Struktur** an **PrepareRecips**. **PrepareRecips** ruft die **IMAPIProp::GetProps-Methode** jedes Empfängers auf, um PR_HOME_TELEPHONE_NUMBER **abzurufen,** da sie derzeit nicht Teil der **ADRLIST-Struktur** ist. Wenn **PrepareRecips** zurückgegeben wird, stellt die Empfängerliste eine zusammengeführte Liste von Empfängern dar, deren Eigenschaften in der **ADRLIST-Struktur** für jeden Empfänger zuerst angezeigt werden. 
  
Die Empfängerliste für empfänger 1 und 2 enthält Eigenschaften in der folgenden Reihenfolge:
  
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
    
Die Empfängerliste für empfänger 3, 4 und 5 enthält Eigenschaften in der folgenden Reihenfolge:
  
1. **PR_ADDRTYPE**
    
2. **PR_ENTRYID**
    
3. **PR_HOME_TELEPHONE_NUMBER**
    
4. **PR_DISPLAY_NAME**
    
5. **PR_SEARCH_KEY**
    
6. **PR_EMAIL_ADDRESS**
    
7. **PR_ADDRTYPE**
    
Rufen Sie als Alternative zum Aufrufen von **IAddrBook::P repareRecips** für die Arbeit mit Eigenschaften die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) und gegebenenfalls die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) jedes Empfängers auf. Wenn nur ein Empfänger beteiligt ist, ist beide Technik zufriedenstellend. Wenn jedoch mehrere Empfänger beteiligt sind, spart das Aufrufen von **PrepareRecips** anstelle der **IMAPIProp-Methoden** Zeit und, wenn Sie remote arbeiten, viele Remoteprozeduraufrufe. **PrepareRecips** verarbeitet alle Empfänger in einem einzigen Anruf, **während GetProps** und **SetProps** einen Aufruf für jeden Empfänger erstellen. 
  

