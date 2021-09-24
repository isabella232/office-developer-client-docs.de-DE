---
title: Vorbereiten eines Empfängers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9573f10c-66e1-4e87-93f0-89687e906b8b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4b04ea717f6fd12b6efb150bdd06c7d2046e4402
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550274"
---
# <a name="preparing-a-recipient"></a>Vorbereiten eines Empfängers

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Clientanwendung bereitet Empfänger vor, indem ihre kurzfristigen Eintragsbezeichner in langfristige Eintragsbezeichner konvertiert und möglicherweise Eigenschaften hinzugefügt, geändert oder neu angeordnet werden. Sie können Empfänger vorbereiten, die Teil einer Empfängerliste sind, für eine Nachricht oder Empfänger, die keine Beziehung zu einer Nachricht haben. In der Regel rufen Clients [IAddrBook::P repareRecips](iaddrbook-preparerecips.md) direkt auf, um kurzfristige Eintragsbezeichner in langfristige Eintragsbezeichner für Empfänger zu übersetzen, die im allgemeinen Adressdialogfeld enthalten sind. Bei Empfängern, die einer ausgehenden Nachricht zugeordnet sind, wird die Empfängervorbereitung durch den Namensauflösungsprozess verarbeitet. 
  
Rufen Sie zum Vorbereiten einer Liste von Empfängern **IAddrBook::P repareRecips** auf. **PrepareRecips** akzeptiert eine [ADRLIST-Struktur](adrlist.md) und eine Liste von Eigenschaftentags. Die **ADRLIST-Struktur** enthält die Empfänger, die vorbereitet werden sollen, während die Eigenschaftentagliste Eigenschaften darstellt, die von jedem Empfänger unterstützt werden sollen. **PrepareRecips** versucht, die Eigenschaften, die in der Eigenschaftentagliste enthalten sind, am Anfang der **ADRLIST-Struktur** zu platzieren. Wenn eine der Eigenschaften in der Liste in der **ADRLIST-Struktur** fehlt, ruft MAPI den Adressbuchanbieter auf, um sie zu liefern. Wenn Sie nur nach langfristigen Eintragsbezeichnern suchen müssen, übergeben Sie NULL für den _LpSPropTagArray-Parameter._ 
  
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
    
Da alle Empfänger als erste drei Eigenschaften **PR_ADDRTYPE**, **PR_ENTRYID** und **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)) verfügen müssen, erstellen Sie ein Eigenschaftentagarray mit diesen Eigenschaften, und übergeben Sie es und die **ADRLIST-Struktur** an **PrepareRecips**. **PrepareRecips** ruft die **IMAPIProp::GetProps-Methode** jedes Empfängers auf, um **PR_HOME_TELEPHONE_NUMBER** abzurufen, da sie derzeit nicht Teil der **ADRLIST-Struktur** ist. When **PrepareRecips** returns, the recipient list represents a merged list of recipients with the properties included in the **ADRLIST** structure appearing first for each recipient. 
  
Die Empfängerliste für die Empfänger 1 und 2 enthält Eigenschaften in der folgenden Reihenfolge:
  
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
    
Die Empfängerliste für die Empfänger 3, 4 und 5 enthält Eigenschaften in der folgenden Reihenfolge:
  
1. **PR_ADDRTYPE**
    
2. **PR_ENTRYID**
    
3. **PR_HOME_TELEPHONE_NUMBER**
    
4. **PR_DISPLAY_NAME**
    
5. **PR_SEARCH_KEY**
    
6. **PR_EMAIL_ADDRESS**
    
7. **PR_ADDRTYPE**
    
Als Alternative zum Aufrufen von **IAddrBook::P repareRecips** zum Arbeiten mit Eigenschaften rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) jedes Empfängers und ggf. die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) auf. Wenn nur ein Empfänger beteiligt ist, ist beide Technik zufriedenstellend. Wenn jedoch mehrere Empfänger beteiligt sind, spart das Aufrufen von **PrepareRecips** anstelle der **IMAPIProp-Methoden** Zeit und, wenn Sie remote arbeiten, viele Remoteprozeduraufrufe. **PrepareRecips** verarbeitet alle Empfänger in einem einzigen Aufruf, während **GetProps** und **SetProps** einen Aufruf für jeden Empfänger ausführen. 
  

