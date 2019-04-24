---
title: MAPI-Empf�nger
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 88a4360d-6ab8-466e-8ebd-af80227ee00a
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ebdaf47b4f20763574ffac73bddeb3eb4eeb95df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328217"
---
# <a name="mapi-recipients"></a>MAPI-Empf�nger

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Every message to be transmitted has one or more recipients, or a set of properties that describe where the message is to be delivered. Because recipients are used only in the context of a message, they are considered subobjects of a message instead of separate MAPI objects. Clients and providers work with recipients using the **IMessage** interface. For more information, see [IMessage: IMAPIProp](imessageimapiprop.md).
  
Clients greifen �ber seine Empf�nger Tabelle Empf�nger einer Nachricht auf. Jede Nachricht weist eine Empf�nger Tabelle, die zusammenfassende Informationen zu den einzelnen Empf�nger enth�lt. Die Spalten in der Tabelle enthalten, abh�ngig von den Status der Nachricht. Wenn eine Nachricht verfasst, m�glicherweise die Empf�nger nur die drei Spalten in der Tabelle:
  
- Anzeigename oder **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- Empfängertyp oder **PR_RECIPIENT_TYPE** ([pidtagrecipienttype (](pidtagrecipienttype-canonical-property.md))
    
- Zeilenbezeichner oder **PR_ROWID** ([pidtagrowid (](pidtagrowid-canonical-property.md))
    
Nachdem die Nachricht den Prozess der Namensauflösung durchlaufen hat, verfügt jeder Empfänger auch über eine Eintrags-ID oder **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Spalte. Und wenn die Nachricht gesendet wurde, werden die Zeilen in der Tabelle Empf�nger von zwei weitere Spalten hinzugef�gt:
  
- Adresstyp oder **PR_ADDRTYPE** ([pidtagaddresstype (](pidtagaddresstype-canonical-property.md))
    
- Transport Verantwortlichkeit oder **PR_RESPONSIBILITY** ([pidtagresponsibility (](pidtagresponsibility-canonical-property.md))
    
Clients can retrieve a message's recipient table by calling its **IMessage::GetRecipientTable** method or its **IMAPIProp::OpenProperty** method. For more information, see [IMessage::GetRecipientTable](imessage-getrecipienttable.md) and [IMAPIProp::OpenProperty](imapiprop-openproperty.md). Message store providers are expected to support both of these approaches. The **OpenProperty** approach requires that the client specify IID_IMAPITable as the interface identifier and **PR_MESSAGE_RECIPIENTS** as the property tag. **PR_MESSAGE_RECIPIENTS** ([Pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md)) ist eine Table-Objekteigenschaft, die die Empfängertabelle einer Nachricht darstellt. Message store providers are required to set **PR_MESSAGE_RECIPIENTS** for each message and include it in the array of property tags returned from the **IMAPIProp::GetPropList** method. For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).
  
For more information about how to work with a recipient table, see [Empf�nger Tabellen](recipient-tables.md).
  
Zus�tzlich zum Zugriff auf eine Tabelle Empf�nger verwendet wird, kann **PR_MESSAGE_RECIPIENTS** verwendet werden: 
  
- With **IMAPIProp::CopyTo** or **IMAPIProp::CopyProps** to exclude or include recipients when copying. For more information see, [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md).
    
- In einer Einschr�nkung Unterobjekt um anzugeben, dass die untergeordneten Restiction an Empf�nger angewendet werden soll.
    
Clients k�nnen Empf�nger einer Nachricht durch Kopieren von Eintr�gen aus dem Adressbuch MAPI oder durch die Erstellung neuer Eintr�ge hinzuf�gen. Diese neuen Eintr�gen aufgerufen One, k�nnen vor�bergehend vorhanden oder in einem Container ge�ndert werden dauerhaft gespeichert werden. W�hrend die haben Empf�nger an, die aus dem Adressbuch getroffen werden Eintragsbezeichner ihre Adressbuchanbieter zugeordnet haben, einmaligen Empf�nger Eintragsbezeichner, die MAPI formatiert sind. Transport-Anbieter und Clients zuordnen einmaligen Eintragsbezeichner mit verschiedenen Typen von Adressen. 
  
Transportanbieter aufrufen **IMAPISupport::CreateOneOff** zum Erstellen einer einmaligen Eintrags-ID f�r eine Adresse auf eine ausgehende Meldung an, wenn: 
  
- Die Adresse geh�rt zu einem Gateway.
    
- Die Adresse kann nicht vom Adressbuch-Dienstanbieter im aktuellen Profil behandelt werden.
    
For more information, see [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md).
  
Clients aufrufen **IAddrBook::CreateOneOff** zum Erstellen einer einmaligen Eintrags-ID f�r eine Adresse auf eine eingehende Meldung an, wenn: 
  
- Die Adresse wird als einmaligen Adresse formatiert.
    
- Die Adresse wird als eine IP-Adresse formatiert.
    
For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md).
  
For more information about one-off entry identifiers and addresses, see [Einmaligen-Eintragsbezeichner](one-off-entry-identifiers.md) and [Einmal-Adressen](one-off-addresses.md).
  
Die Eigenschaften eines Empf�ngers sind eine Kombination von Adressbucheigenschaften und spezifische Eigenschaften an Empf�nger. Alle Empf�nger haben die Basisadresse-Eigenschaften, die von adressbuchanbietern implementierte zugewiesen. Wenn Sie ein Eintrag f�r eine ausgehende Nachricht als Empf�nger verwendet wird, werden die Basisadresse-Eigenschaften auf die Struktur **ADRLIST** kopiert, die die Eigenschaften f�r alle Empf�nger einer Nachricht enth�lt. 
  
Zwei Eigenschaften, die speziell f�r Empf�nger festgelegt sind, sind **PR_RECIPIENT_TYPE** und **PR_RESPONSIBILITY**. **PR_RECIPIENT_TYPE** gibt an, ob ein Empf�nger ein prim�rer, Carbon Copy, Blindkopie, blind Carbon Copy, Blindkopie oder einen Empf�nger erneut ist. Die ersten drei Typen werden an Empf�nger f�r Nachrichten zugewiesen, die zum ersten Mal gesendet werden. 
  
Wenn Sie ein Empf�nger erh�lt die Meldung keine, und es wird versucht, zu senden, der Empf�nger wird so kopiert, und dieses Typs auf MAPI_P1 festgelegt, um anzugeben, dass er einen Empf�nger erneut senden. Wenn nur einige der Empf�nger eine Meldung angezeigt, werden deren Eigenschaften **PR_RECIPIENT_TYPE** durch das Hinzuf�gen des MAPI_SUBMITTED-Flags markiert, wenn die Nachricht erneut gesendet wird. Clients sind erforderlich, um die prim�ren Empf�nger zu behandeln oder Empf�nger mit ihren **PR_RECIPIENT_TYPE** auf MAPI_TO festgelegt. Alle anderen Typen sind optional. 
  
 **PR_RESPONSIBILITY** wird festgelegt, um der Adressbuchhierarchie anzugeben, ob er behandeln soll, an den Empf�nger gesendet. Wenn eine ausgehende Nachricht zuerst gesendet wird, k�nnen alle Empf�nger **PR_RESPONSIBILITY** auf FALSE festgelegt. Wie ein Transport Verantwortung f�r eine oder mehrere Empf�nger senden Forderungsanbieter, werden ihre **PR_RESPONSIBILITY** -Eigenschaften auf TRUE festgelegt. 
  

