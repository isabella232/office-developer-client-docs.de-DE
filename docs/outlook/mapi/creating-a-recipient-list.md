---
title: Erstellen einer Empfängerliste
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 270f86dd-2c1f-47eb-80f7-9d0d63936d61
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e460765d57e4e40cc2739b39521b995c64ba5cf0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584668"
---
# <a name="creating-a-recipient-list"></a>Erstellen einer Empfängerliste

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Empfängerliste ist eine [ADRLIST-Struktur,](adrlist.md) die ein Array von Eigenschaftswertstrukturen für jeden Nachrichtenempfänger enthält – Ziel für die Nachricht. Ein Empfänger kann einen menschlichen Benutzer, einen Computer oder einen Ordner darstellen. Alle zu sendenden Nachrichten erfordern mindestens einen Empfänger, der den Namensauflösungsprozess durchlaufen hat – ein Prozess, um sicherzustellen, dass die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft im Eigenschaftenwertarray des Empfängers enthalten ist. 
  
Die Eigenschaften eines Empfängers sind eine Kombination aus Adressbucheigenschaften und Nachrichteneigenschaften. Empfängereigenschaften können entweder auf alle Nachrichten für einen bestimmten Empfänger oder nur auf die aktuelle Nachricht angewendet werden. Sowohl Nachrichtenspeicher- als auch Transportanbieter können Empfängereigenschaften festlegen. 
  
Jeder Empfänger muss einen Kernsatz von Eigenschaften in seinem Eigenschaftenwertarray haben, bis die Nachricht gesendet werden kann. Zu den erforderlichen Empfängereigenschaften gehören:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) 
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) 
    
- **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) 
    
Diese Eigenschaften werden verwendet, um auf den Empfänger zuzugreifen, Nachrichten an ihn zu senden und ihn mit anderen zu vergleichen. Nicht alle diese Eigenschaften müssen sofort verfügbar sein. Sie können einen Empfänger zunächst hinzufügen, ohne dessen Eintragsbezeichner zu kennen, und sich dabei auf den Namensauflösungsprozess verlassen, um diese Eigenschaft zuzuweisen. Rufen Sie zu einem bestimmten Zeitpunkt vor dem Senden einer Nachricht [IAddrBook::ResolveName](iaddrbook-resolvename.md) auf, um sicherzustellen, dass alle Empfänger in Der Empfängerliste aufgelöst sind. Weitere Informationen finden Sie unter [Auflösen eines Empfängernamens.](resolving-a-recipient-name.md)
  
Empfängerlisten können aus Nachrichtenbenutzern oder Verteilerlisteneinträgen in einem Adressbuchcontainer oder aus einmaligen Listen erstellt werden. Einmalige Einträge sind Empfänger, die entweder als temporäre Einträge erstellt werden, die nur zum Adressieren einer einzelnen Nachricht verwendet werden sollen, oder als Einträge, die einem persönlichen Adressbuch hinzugefügt werden sollen. Das Format für einen einmaligen Eintragsbezeichner und eine Adresse wird durch die MAPI definiert. Weitere Informationen zu diesen Formaten finden Sie unter ["One-Off Addresses"](one-off-addresses.md) und ["One-Off Entry Identifiers".](one-off-entry-identifiers.md)
  
Sie können Benutzern das Erstellen ihrer Empfängerlisten ermöglichen:
  
- Nur mit Einträgen aus dem Adressbuch.
    
- Nur mit einmaligen Einträgen.
    
- Mit einer Kombination aus Adressbuchempfängern und Einmaligen.
    
 **So erstellen Sie eine Empfängerliste mithilfe des allgemeinen Adressdialogfelds**
  
1. Weisen Sie einer [ADRPARM-Struktur eine ADRPARM-Struktur](adrparm.md) und einen Zeiger zu. [](adrlist.md) 
    
2. Null des Speichers in der **ADRPARM-Struktur,** und legen Sie den **ADRLIST-Zeiger** auf NULL fest. 
    
3. Rufen Sie [IAddrBook::Address](iaddrbook-address.md) auf, um das Adressdialogfeld anzuzeigen und die **ADRPARM-Struktur** aufzufüllen. 
    
4. Rufen Sie [IMessage::ModifyRecipients auf,](imessage-modifyrecipients.md)und übergeben Sie den **ADRLIST-Zeiger.** Diese Struktur enthält die Eigenschaften der einzelnen Empfänger, die vom Benutzer ausgewählt wurden. 
    
 **So erstellen Sie programmgesteuert eine Empfängerliste**
  
1. Weisen Sie eine **ADRLIST-Struktur** zu, die eine [ADRENTRY-Struktur](adrentry.md) für jeden Empfänger enthält, der in die Liste aufgenommen werden soll. Legen Sie jede **ADRENTRY-Struktur** so groß, dass sie alle erforderlichen Eigenschaften und **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) enthalten kann.
    
2. Legen Sie für jeden Empfänger das Eigenschaftswertarray für sein **aEntries-Element** in der **ADRLIST-Struktur** fest. 
    
3. Rufen Sie [IMessage::ModifyRecipients](imessage-modifyrecipients.md) auf, wobei das MODRECIP_ADD-Flag festgelegt ist. 
    

