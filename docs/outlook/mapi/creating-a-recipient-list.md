---
title: Erstellen einer Empfängerliste
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 270f86dd-2c1f-47eb-80f7-9d0d63936d61
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e3aa1f2b2e1e7c6d8a9be3fff451002952930ffb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428214"
---
# <a name="creating-a-recipient-list"></a>Erstellen einer Empfängerliste

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Empfängerliste ist eine [ADRLIST-Struktur,](adrlist.md) die ein Array von Eigenschaftenwertstrukturen für jeden Nachrichtenempfänger enthält – Ziel für die Nachricht. Ein Empfänger kann einen menschlichen Benutzer, einen Computer oder einen Ordner darstellen. Für alle zu sendenden Nachrichten ist mindestens ein Empfänger erforderlich, der den Namenauflösungsprozess durchgef?nnen hat– ein Prozess, mit dem sichergestellt wird, dass die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft im Eigenschaftenwertarray des Empfängers enthalten ist. 
  
Die Eigenschaften eines Empfängers sind eine Kombination aus Adressbucheigenschaften und Nachrichteneigenschaften. Empfängereigenschaften können entweder auf alle Nachrichten für einen bestimmten Empfänger oder nur auf die aktuelle Nachricht angewendet werden. Sowohl Nachrichtenspeicher als auch Transportanbieter können Empfängereigenschaften festlegen. 
  
Jeder Empfänger muss über einen Kernsatz von Eigenschaften in seinem Eigenschaftswertarray verfügen, bis die Nachricht gesendet werden kann. Zu den erforderlichen Empfängereigenschaften gehören:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) 
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) 
    
- **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) 
    
Diese Eigenschaften werden verwendet, um auf den Empfänger zu zugreifen, Nachrichten an ihn zu senden und ihn mit anderen zu vergleichen. Nicht alle diese Eigenschaften müssen sofort verfügbar sein. Sie können einen Empfänger zunächst hinzufügen, ohne dessen Eintrags-ID zu kennen, und diese Eigenschaft im Namenauflösungsprozess zuweisen. Rufen Sie vor dem Senden einer Nachricht [IAddrBook::ResolveName](iaddrbook-resolvename.md) auf, um sicherzustellen, dass alle Empfänger in der Empfängerliste aufgelöst werden. Weitere Informationen finden Sie unter [Resolving a Recipient Name](resolving-a-recipient-name.md).
  
Empfängerlisten können aus Nachrichtenbenutzern oder Verteilerlisteneinträgen in einem Adressbuchcontainer oder aus einmal erstellt werden. Einmalige Nachrichten sind Empfänger, die entweder als temporäre Einträge erstellt werden, die nur für die Adressierung einer einzelnen Nachricht oder als Einträge verwendet werden, die einem persönlichen Adressbuch hinzugefügt werden sollen. Das Format für eine eindeutige Eintrags-ID und -Adresse wird durch MAPI definiert. Weitere Informationen zu diesen Formaten finden Sie unter [One-Off Addresses](one-off-addresses.md) and [One-Off Entry Identifiers](one-off-entry-identifiers.md).
  
Sie können Benutzern das Erstellen ihrer Empfängerlisten ermöglichen:
  
- Nur mit Einträgen aus dem Adressbuch.
    
- Nur mit einmalen Einträgen.
    
- Mit einer Kombination aus Adressbuchempfängern und Einmalempfängern.
    
 **So erstellen Sie eine Empfängerliste mithilfe des Dialogfelds allgemeine Adresse**
  
1. Weisen Sie [einer ADRPARM-Struktur](adrparm.md) und einem Zeiger eine [ADRLIST-Struktur](adrlist.md) zu. 
    
2. Null des Arbeitsspeichers in der **ADRPARM-Struktur,** und legen Sie den **ADRLIST-Zeiger** auf NULL. 
    
3. Rufen [Sie IAddrBook::Address auf,](iaddrbook-address.md) um das Adressdialogfeld anzuzeigen und die **ADRPARM-Struktur** auffüllen. 
    
4. Rufen [Sie IMessage::ModifyRecipients auf,](imessage-modifyrecipients.md)und übergeben Sie den **ADRLIST-Zeiger.** Diese Struktur enthält die Eigenschaften der einzelnen vom Benutzer ausgewählten Empfänger. 
    
 **So erstellen Sie eine Empfängerliste programmgesteuert**
  
1. Weisen Sie **eine ADRLIST-Struktur** zu, die eine [ADRENTRY-Struktur](adrentry.md) für jeden empfänger enthält, der in die Liste aufgenommen werden soll. Machen Sie **jede ADRENTRY-Struktur** so groß, dass jede der erforderlichen Eigenschaften und PR_RECIPIENT_TYPE **(** [PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) enthalten ist.
    
2. Legen Sie für jeden Empfänger das Eigenschaftswertarray für das **Element aEntries** in der **ADRLIST-Struktur.** 
    
3. Rufen [Sie IMessage::ModifyRecipients](imessage-modifyrecipients.md) mit dem MODRECIP_ADD auf. 
    

