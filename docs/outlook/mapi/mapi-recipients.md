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
ms.openlocfilehash: f83f3f51c8b11aececa31fa277fb799ce1ada512
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793065"
---
# <a name="mapi-recipients"></a>MAPI-Empf�nger

  
  
**Betrifft**: Outlook 
  
Every message to be transmitted has one or more recipients, or a set of properties that describe where the message is to be delivered. Because recipients are used only in the context of a message, they are considered subobjects of a message instead of separate MAPI objects. Clients and providers work with recipients using the **IMessage** interface. For more information, see [IMessage: IMAPIProp](imessageimapiprop.md).
  
Clients greifen �ber seine Empf�nger Tabelle Empf�nger einer Nachricht auf. Jede Nachricht weist eine Empf�nger Tabelle, die zusammenfassende Informationen zu den einzelnen Empf�nger enth�lt. Die Spalten in der Tabelle enthalten, abh�ngig von den Status der Nachricht. Wenn eine Nachricht verfasst, m�glicherweise die Empf�nger nur die drei Spalten in der Tabelle:
  
- Der Anzeigename oder die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- Empfängertyp oder **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- Zeilen-ID oder **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))
    
Wenn die Nachricht Vorgang der Lösung unterzogen wurde, werden jeden Empfänger auch eine Eintrags-ID oder ein Spaltenfeld **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) haben. Und wenn die Nachricht gesendet wurde, werden die Zeilen in der Tabelle Empf�nger von zwei weitere Spalten hinzugef�gt:
  
- Adresstyp oder **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- Transport Verantwortung oder **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))
    
Clients can retrieve a message's recipient table by calling its **IMessage::GetRecipientTable** method or its **IMAPIProp::OpenProperty** method. For more information, see [IMessage::GetRecipientTable](imessage-getrecipienttable.md) and [IMAPIProp::OpenProperty](imapiprop-openproperty.md). Message store providers are expected to support both of these approaches. The **OpenProperty** approach requires that the client specify IID_IMAPITable as the interface identifier and **PR_MESSAGE_RECIPIENTS** as the property tag. **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) ist ein Table-Objekt-Eigenschaft, die Empfänger einer Nachricht-Tabelle darstellt. Message store providers are required to set **PR_MESSAGE_RECIPIENTS** for each message and include it in the array of property tags returned from the **IMAPIProp::GetPropList** method. For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).
  
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
  

