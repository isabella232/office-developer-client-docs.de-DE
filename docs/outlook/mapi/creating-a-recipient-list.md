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
  
Eine Empfängerliste ist eine [ADRLIST](adrlist.md) -Struktur, die ein Array von Eigenschaftswert Strukturen für jeden Nachrichtenempfänger enthält – Ziel für die Nachricht. Ein Empfänger kann einen Benutzer, einen Computer oder einen Ordner darstellen. Für alle Nachrichten, die gesendet werden sollen, ist mindestens ein Empfänger erforderlich, der über den Prozess der Namensauflösung verfügt, um sicherzustellen, dass die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft im Eigenschaftswert Array des Empfängers enthalten ist. 
  
Die Eigenschaften eines Empfängers sind eine Kombination aus Adressbucheigenschaften und Nachrichteneigenschaften. Empfänger Eigenschaften können entweder auf alle Nachrichten für einen bestimmten Empfänger oder nur auf die aktuelle Nachricht angewendet werden. Sowohl Nachrichtenspeicher-als auch Transportanbieter können Empfänger Eigenschaften festlegen. 
  
Jeder Empfänger muss über eine zentrale Gruppe von Eigenschaften in seinem Eigenschaftswert Array verfügen, bis die Nachricht gesendet werden kann. Zu den erforderlichen Empfänger Eigenschaften gehört Folgendes:
  
- **PR_ADDRTYPE** ([Pidtagaddresstype (](pidtagaddresstype-canonical-property.md)) 
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md)) 
    
- **PR_SEARCH_KEY** ([Pidtagsearchkey (](pidtagsearchkey-canonical-property.md)) 
    
Diese Eigenschaften werden verwendet, um auf den Empfänger zuzugreifen, Nachrichten zu senden und mit anderen zu vergleichen. Nicht alle diese Eigenschaften müssen sofort verfügbar sein. Sie können einen Empfänger zunächst hinzufügen, ohne dessen Eintrags-ID zu kennen, indem Sie den namens Auflösungsprozess zum Zuweisen dieser Eigenschaft verwenden. Rufen Sie [IAddrBook::](iaddrbook-resolvename.md) ResolveName zu einem bestimmten Zeitpunkt vor dem Senden einer Nachricht auf, um sicherzustellen, dass alle Empfänger in der Empfängerliste aufgelöst werden. Weitere Informationen finden Sie unter [Auflösen eines Empfängernamens](resolving-a-recipient-name.md).
  
Empfängerlisten können aus Messaging Benutzern oder Verteilerlisten Einträgen in einem Adressbuchcontainer oder aus einmaligen erfolgen erstellt werden. Einmalig sind Empfänger, die entweder als temporäre Einträge erstellt werden, die nur für die Adressierung einer einzelnen Nachricht oder als Einträge verwendet werden, die einem persönlichen Adressbuch hinzugefügt werden sollen. Das Format für eine einmalige Eintrags-ID und-Adresse wird durch MAPI definiert. Weitere Informationen zu diesen Formaten finden Sie unter [einmalige Adressen](one-off-addresses.md) und [einmalige Eintrags-IDs](one-off-entry-identifiers.md).
  
Sie können Benutzern das Erstellen Ihrer Empfängerlisten ermöglichen:
  
- Nur mit Einträgen aus dem Adressbuch.
    
- Nur mit einmaligen Einträgen.
    
- Mit einer Kombination aus Adressbuch Empfängern und einmaligen.
    
 **So erstellen Sie eine Empfängerliste mithilfe des Dialogfelds "allgemeine Adresse"**
  
1. Reservieren Sie eine [ADRPARM](adrparm.md) -Struktur und einen Zeiger auf eine [ADRLIST](adrlist.md) -Struktur. 
    
2. NULL der Speicher in der **ADRPARM** -Struktur und legen Sie den **ADRLIST** -Zeiger auf NULL. 
    
3. Rufen Sie [IAddrBook:: Address](iaddrbook-address.md) auf, um das Dialogfeld Adresse anzuzeigen und die **ADRPARM** -Struktur aufzufüllen. 
    
4. Rufen Sie [IMessage:: ModifyRecipients](imessage-modifyrecipients.md)auf, und übergeben Sie den **ADRLIST** -Zeiger. Diese Struktur enthält die Eigenschaften aller Empfänger, die vom Benutzer ausgewählt werden. 
    
 **So erstellen Sie eine Empfängerliste programmgesteuert**
  
1. Reservieren Sie eine **ADRLIST** -Struktur, die eine [Miet](adrentry.md) Struktur für jeden der Empfänger enthält, der in der Liste enthalten sein soll. Legen Sie die einzelnen **Miet** Strukturen so hoch fest, dass Sie alle erforderlichen Eigenschaften und **PR_RECIPIENT_TYPE** ([pidtagrecipienttype (](pidtagrecipienttype-canonical-property.md)) enthalten.
    
2. Legen Sie für jeden Empfänger das Eigenschaftswert Array für sein **aEntries** -Element in der **ADRLIST** -Struktur fest. 
    
3. Rufen Sie [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) mit dem MODRECIP_ADD-Kennzeichen Satz auf. 
    

