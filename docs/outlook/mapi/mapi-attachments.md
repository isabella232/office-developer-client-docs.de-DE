---
title: MAPI-Anlagen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6e6c6ad9-1e07-4234-a5ef-18020d7ce468
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 90fbec8b61499f383228823d69b041a21199a22e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297872"
---
# <a name="mapi-attachments"></a>MAPI-Anlagen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einige Anbieter Nachricht erm�glichen Clients Nachrichten Informationen hinzugef�gt, in Form von Dateien, OLE-Objekte, Nachrichten oder Bin�rdaten zugeordnet. Diese zus�tzlichen Informationen wird eine e-Mail-Nachrichtenanhang aufgerufen. Da Anlagen erstellt, verwaltet und auf die nur �ber ihre Nachrichten zugegriffen werden, werden sie Nachricht Unterobjekte betrachtet. Anlagen enthalten einen fortlaufende Zahlen bekannten statt eines Eintrags-ID f�r den Zugriff als Anlage Zahl. Diese Nummer wird die Anlage in der Nachricht, aber nicht notwendigerweise innerhalb der Nachrichtenspeicher eindeutig identifiziert. Zwei verschiedene Nachrichten k�nnen verschiedene Anlagen mit derselben Anlage Nummer aufweisen. Anlagennummern sind nur gültig, solange die Nachricht geöffnet ist und in der **PR_ATTACH_NUM** ([pidtagattachnumber (](pidtagattachnumber-canonical-property.md))-Eigenschaft gespeichert werden.
  
Zugriff auf zusammenfassende Informationen zu allen eine e-Mail-Anlagen abrufen Clients die Anlagentabelle. Die Anlagentabelle enth�lt Informationen, mit denen Clients eine Anlage direkt, wie die Anzahl der Anlage und aufzeichnen Schl�ssel zuzugreifen. Clients k�nnen eine Anlagentabelle durch Abrufen:
  
- Calling **IMessage::GetAttachmentTable**. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
- Calling **IMAPIProp::OpenProperty**. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
Message store providers are expected to support both of these approaches. Der **OpenProperty** -Ansatz erfordert, dass der Aufrufer IID_IMAPITable als Schnittstellenbezeichner und **PR_MESSAGE_ATTACHMENTS** ([pidtagmessageattachments (](pidtagmessageattachments-canonical-property.md)) als das Property-Tag angibt. **PR_MESSAGE_ATTACHMENTS** is a table object property that represents a message's attachment table. Message store providers are required to set **PR_MESSAGE_ATTACHMENTS** for each message and include it in the array of property tags returned from the **IMAPIProp::GetPropList** method. For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).
  
 **PR_MESSAGE_ATTACHMENTS** kann verwendet werden: 
  
- Mit **IMAPIProp::OpenProperty** Zugriff auf eine Anlage oder ein Empf�nger-Tabelle. 
    
- With **IMAPIProp::CopyTo** or **IMAPIProp::CopyProps** to exclude or include attachments when copying. For more information, see [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md).
    
- In einer Einschr�nkung Unterobjekt um anzugeben, dass die untergeordneten Einschr�nkung auf Anlagen angewendet werden soll.
    
For more information, see [Anlagentabellen](attachment-tables.md).
  

