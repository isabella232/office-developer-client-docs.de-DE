---
title: Erstellen einer Empfängerliste
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 270f86dd-2c1f-47eb-80f7-9d0d63936d61
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fa23377a8b080ae9dac3e31dfa137ca03a242c74
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791501"
---
# <a name="creating-a-recipient-list"></a>Erstellen einer Empfängerliste

  
  
**Betrifft**: Outlook 
  
Eine Empfängerliste ist eine [ADRLIST](adrlist.md) -Struktur, die ein Array der Eigenschaft Wert Strukturen für jeden Empfänger der Nachricht enthält – Ziel für die Nachricht. Ein Empfänger kann ein human Benutzer, einen Computer oder einen Ordner dar. Alle Nachrichten gesendet werden erfordern mindestens einen Empfänger, die durch den Namen Lösung Prozess wurde – ein Prozess zum sicherstellen, dass die Eigenschaft **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) Wert Array-Eigenschaft gehören des Empfängers enthalten ist. 
  
Die Eigenschaften eines Empfängers sind eine Kombination von Adressbucheigenschaften und Nachrichteneigenschaften. Empfängereigenschaften können auf alle Nachrichten für einen bestimmten Empfänger oder nur für die aktuelle Nachricht anwenden. Beide Nachrichtenspeicher und Transportanbieter Empfängereigenschaften festlegen können. 
  
Jeden Empfänger muss eine Kerngruppe von Eigenschaften des Arrays der Eigenschaft Wert durch die Zeit haben, die die Nachricht gesendet werden kann. Die erforderlichen Empfängereigenschaften beinhaltet:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) 
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) 
    
- **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) 
    
Diese Eigenschaften werden verwendet, für den Zugriff auf den Empfänger senden von Nachrichten an diese, und es mit anderen Personen verglichen. Nicht alle diese Eigenschaften müssen sofort verfügbar sein. Sie können einen Empfänger zunächst hinzufügen ohne die Eintrags-ID auf Vorgang der Lösung, dieser Eigenschaft zuzuweisen. Bevor Sie eine Nachricht senden, rufen Sie zu einem bestimmten Zeitpunkt [IAddrBook::ResolveName](iaddrbook-resolvename.md) , um sicherzustellen, dass alle Empfänger in der Empfängerliste aufgelöst werden. Weitere Informationen finden Sie unter [Auflösen von Namen Empfänger](resolving-a-recipient-name.md).
  
Empfängerlisten können von Benutzern oder Verteilung Listeneinträge in einem Adressbuchcontainer messaging oder Fly erstellt werden. Fly sind Empfänger, die erstellt werden, entweder als temporäre Einträge aus, die nur zum Umgang mit einer Nachricht verwendet werden oder als Einträge, ein persönliches Adressbuch hinzugefügt werden soll. Das Format für einen einmaligen Eintrags-ID und eine Adresse wird durch MAPI definiert. Weitere Informationen zu diesen Formaten finden Sie unter [Einmal-Adressen](one-off-addresses.md) und [Einmaligen-Eintragsbezeichner](one-off-entry-identifiers.md).
  
Sie können Benutzer ihre Empfängerlisten erstellen können:
  
- Nur mit den Einträgen aus dem Adressbuch.
    
- Nur bei einmaligen Einträge.
    
- Mit einer Kombination von Address Book Empfänger und Fly.
    
 **Eine allgemeine Adresse im Dialogfeld Empfängerliste erstellen**
  
1. Weisen Sie eine [ADRPARM](adrparm.md) -Struktur und einen Zeiger auf eine [ADRLIST](adrlist.md) -Struktur. 
    
2. 0 (null) in der Struktur **ADRPARM** Speicher und den **ADRLIST** Zeiger auf NULL festgelegt wurde. 
    
3. Rufen Sie [IAddrBook::Address](iaddrbook-address.md) , um das Dialogfeld Adresse anzeigen, und füllen Sie die **ADRPARM** -Struktur. 
    
4. Rufen Sie [IMessage::ModifyRecipients](imessage-modifyrecipients.md), übergeben den Zeiger **ADRLIST** . Diese Struktur enthält die Eigenschaften der einzelnen der vom Benutzer ausgewählten Empfänger. 
    
 **So erstellen Sie programmgesteuert eine Empfängerliste**
  
1. Reservieren Sie eine **ADRLIST** -Struktur, die enthält eine [ADRENTRY](adrentry.md) -Struktur für die einzelnen Empfänger an, die in der Liste enthalten sein. Stellen Sie jede **ADRENTRY** Struktur groß genug für alle erforderlichen Eigenschaften und **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).
    
2. Legen Sie für jeden Empfänger des Arrays der Eigenschaft Wert für **aEntries** Mitglied in der **ADRLIST** -Struktur. 
    
3. Rufen Sie [IMessage::ModifyRecipients](imessage-modifyrecipients.md) mit der MODRECIP_ADD-Flag. 
    

