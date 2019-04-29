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
  
Eine Clientanwendung bereitet Empfänger vor, indem Sie Ihre kurzfristigen Eintrags-IDs in langfristige Eintrags-IDs konvertieren und möglicherweise Eigenschaften hinzufügen, ändern oder neu anordnen. Sie können Empfänger, die Teil einer Empfängerliste sind, für eine Nachricht oder Empfänger vorbereiten, die nichts mit einer Nachricht zu tun haben. In der Regel rufen Clients [IAddrBook::P reparerecips](iaddrbook-preparerecips.md) direkt auf, um kurzfristige Eintragsbezeichner in langfristige Eintragsbezeichner für Empfänger zu übersetzen, die im Dialogfeld Allgemeine Adresse enthalten sind. Bei Empfängern, die einer ausgehenden Nachricht zugeordnet sind, wird die Empfänger Vorbereitung vom Prozess der Namensauflösung behandelt. 
  
Um eine Liste von Empfängern vorzubereiten, rufen Sie **IAddrBook::P Reparerecips**auf. **PrepareRecips** akzeptiert eine [ADRLIST](adrlist.md) -Struktur und eine Liste von Property-Tags. Die **ADRLIST** -Struktur enthält die zu präparierenden Empfänger, während die Eigenschaftsliste Eigenschaften darstellt, die von jedem Empfänger unterstützt werden sollen. **PrepareRecips** versucht, die Eigenschaften, die in der Eigenschaftsliste enthalten sind, am Anfang der **ADRLIST** -Struktur zu platzieren. Wenn eine der Eigenschaften in der Liste in der **ADRLIST** -Struktur fehlt, ruft MAPI den Adressbuchanbieter zur Bereitstellung auf. Wenn Sie nur langfristige Eintragsbezeichner überprüfen müssen, übergeben Sie NULL für den _lpSPropTagArray_ -Parameter. 
  
Angenommen, Sie arbeiten mit fünf Empfängern. Alle fünf Empfänger werden in der **ADRLIST** -Struktur mit den folgenden Eigenschaften in der folgenden Reihenfolge angezeigt: 
  
1. **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
2. **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
3. **PR_SEARCH_KEY** ([Pidtagsearchkey (](pidtagsearchkey-canonical-property.md))
    
4. **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
5. **PR_ADDRTYPE** ([Pidtagaddresstype (](pidtagaddresstype-canonical-property.md))
    
Drei weitere Eigenschaften sind in der **ADRLIST** -Struktur für die ersten beiden Empfänger enthalten. 
  
1. **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))
    
2. **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))
    
3. **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))
    
Da alle Empfänger als erste drei Eigenschaften **PR_ADDRTYPE**, **PR_ENTRYID**und **PR_HOME_TELEPHONE_NUMBER** ([pidtaghometelephonenumber (](pidtaghometelephonenumber-canonical-property.md)) verfügen müssen, erstellen Sie ein Property-Tag-Array mit diesen Eigenschaften, und führen Sie und die **ADRLIST** -Struktur zu **PrepareRecips**. **PrepareRecips** Ruft die **IMAPIProp::** GetProps-Methode der einzelnen Empfänger auf, um **PR_HOME_TELEPHONE_NUMBER** abzurufen, da es derzeit nicht Teil der **ADRLIST** -Struktur ist. Wenn **PrepareRecips** zurückgibt, stellt die Empfängerliste eine zusammengeführte Liste von Empfängern dar, wobei die Eigenschaften in der **ADRLIST** -Struktur aufgeführt sind, die zuerst für jeden Empfänger angezeigt wird. 
  
Die Empfängerliste für Empfänger 1 und 2 enthält Eigenschaften in der folgenden Reihenfolge:
  
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
    
Die Empfängerliste für Empfänger 3, 4 und 5 enthält Eigenschaften in der folgenden Reihenfolge:
  
1. **PR_ADDRTYPE**
    
2. **PR_ENTRYID**
    
3. **PR_HOME_TELEPHONE_NUMBER**
    
4. **PR_DISPLAY_NAME**
    
5. **PR_SEARCH_KEY**
    
6. **PR_EMAIL_ADDRESS**
    
7. **PR_ADDRTYPE**
    
Als Alternative zum Aufrufen von **IAddrBook::P reparerecips** , um mit Eigenschaften zu arbeiten, rufen Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode der einzelnen Empfänger und gegebenenfalls deren [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode auf. Wenn nur ein Empfänger beteiligt ist, ist beide Techniken zufrieden stellend. Wenn jedoch mehrere Empfänger beteiligt sind, spart der Aufruf von **PrepareRecips** anstelle der **IMAPIProp** -Methoden Zeit und, wenn Sie Remote arbeiten, viele Remoteprozeduraufrufe. **PrepareRecips** verarbeitet alle Empfänger in einem einzelnen Aufruf, **** während getProps und SetProps einen Anruf für jeden Empfänger durchführen. **** 
  

