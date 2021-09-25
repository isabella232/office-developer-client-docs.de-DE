---
title: MAPI-Objekte und -Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 0aebf536-dcfb-406d-86ac-65db98c78139
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 02d1cae165e19664039deefc8292c28d24d11191
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610258"
---
# <a name="mapi-objects-and-properties"></a>MAPI-Objekte und -Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einige Eigenschaften werden von vielen verschiedenen Objekttypen unterstützt. Die folgenden Eigenschaften sind Beispiele für Eigenschaften, die von mehreren Objekten verwendet werden:
  
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) ist ein binärer Bezeichner, der zum Öffnen von Objekten verwendet wird.
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) ist eine Konstante, die verwendet wird, um die Art des Objekts zu identifizieren.
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ist eine Zeichenfolge, die verwendet wird, um dem Benutzer ein Objekt zu beschreiben.
    
Andere Eigenschaften sind für einen einzelnen Objekttyp sinnvoll. Die folgenden Eigenschaften sind Beispiele für Eigenschaften, die für einen Objekttyp gelten:
  
- **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) ist eine Zeichenfolge, die zum Beschreiben des Nachrichtentyps verwendet wird.
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) ist eine ganze Zahl, die zum Identifizieren einer Zeile in einer Tabelle verwendet wird.
    
- **PR_ATTACH_SIZE** ([PidTagAttachSize](pidtagattachsize-canonical-property.md)) ist eine ganze Zahl, die zum Speichern der Anzahl von Bytes in einer Anlage verwendet wird.
    
Andere Eigenschaften gelten jedoch nur für einen einzelnen Objekttyp in einem bestimmten Zustand. Eigenschaften dieses Typs sind in der Regel Nachrichteneigenschaften. Wenn eine Nachricht zum ersten Mal erstellt wird, ist der Satz von Eigenschaften sehr klein. Da es von einem Client über das Messagingsystem an einen Empfänger gesendet wird, nimmt die Anzahl der Eigenschaften zu, die zum Beschreiben der Nachricht erforderlich sind. Einige dieser hinzugefügten Eigenschaften werden nur in der Nachricht angezeigt, da sie übermittelt wird, während andere nur in der Nachricht angezeigt werden, während sie gesendet wird. Nachrichten verfügen auch über Eigenschaften, die der Klasse zugeordnet sind, zu der sie gehören. Berichtsnachrichten verfügen beispielsweise über Eigenschaften, die von Nachrichten anderer Klassen, z. B. Notizmeldungen, nicht unterstützt werden. 
  
Jedes Objekt verfügt über einige erforderliche Eigenschaften und verfügt möglicherweise über andere optionale Eigenschaften. Erforderliche Eigenschaften sind Eigenschaften, die in einem Objekt vorhanden sein müssen, bevor das Objekt mit seiner [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) erfolgreich gespeichert werden kann. Clients oder Dienstanbieter, die ein Objekt verwenden, können von der Verfügbarkeit der erforderlichen Eigenschaften nach dem **SaveChanges-Aufruf** abhängen. Das heißt, sie können sicher sein, dass ein Aufruf der [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Objekts oder der [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) zum Abrufen dieser Eigenschaften erfolgreich ist. 
  
Optionale Eigenschaften sind Eigenschaften, die je nach Implementierer des Objekts möglicherweise von einem Objekt unterstützt werden. Ein Client oder Dienstanbieter, der das Objekt verwendet, kann nicht erwarten, dass optionale Eigenschaften über die **Methoden GetProps** oder **OpenProperty** verfügbar sind und auf gültige Werte festgelegt werden. 
  
Eine Liste oder Eigenschaften in dieser Referenz finden Sie unter [MAPI-Eigenschaften.](mapi-properties.md) Beschreibungen der Eigenschaften, die zu den einzelnen Nachrichtenspeicher- und Adressbuchobjekten gehören, finden Sie in der Erläuterung der Standardschnittstelle des Objekts. Ordnereigenschaften werden beispielsweise mit **IMAPIFolder** und Messaging-Benutzereigenschaften mit **IMailUser** erläutert. Nachrichteneigenschaften, einschließlich Berichtsnachrichteneigenschaften, werden mit **IMessage** und in der [Nachrichteneigenschaftenübersicht](message-properties-overview.md)beschrieben. Eigenschaften, die zu den einzelnen Tabellentypen gehören, werden im entsprechenden Thema zu [MAPI-Tabellen](mapi-tables.md) beschrieben. Hierarchietabelleneigenschaften werden z. B. in [Hierarchietabellen](hierarchy-tables.md)beschrieben. Eigenschaften, die zu Formularservern gehören, werden in [der Auswahl des Eigenschaftensatzes eines Formulars](choosing-a-form-s-property-set.md)beschrieben.
  
Wenn ein Client oder Dienstanbieter die **GetProps-Methode** eines Objekts aufruft, um mehrere seiner Eigenschaften abzurufen, und eine dieser Eigenschaften nicht verfügbar ist, gibt **GetProps** die Warnung MAPI_W_ERRORS_RETURNED zurück. Der Aufruf wird als erfolgreich betrachtet, da einige der Eigenschaften zurückgegeben wurden. Wenn ein Client oder Dienstanbieter **OpenProperty aufruft** und die Zieleigenschaft nicht verfügbar ist, schlägt die Methode mit dem Fehler MAPI_E_NOT_FOUND fehl. Es ist wichtig zu überprüfen, ob eine angeforderte Eigenschaft zurückgegeben wird, bevor Sie versuchen, damit zu arbeiten. 
  
Abhängig vom Objekt, dem Dienstanbieter, der die Implementierung angibt, und der Eigenschaft kann eine Eigenschaft lese-/schreibgeschützt sein. Mit der Lese-/Schreibberechtigung kann ein Client oder Dienstanbieter, der die Eigenschaft verwendet, seinen Wert ändern. Mit der Schreibschutzberechtigung kann nur der Dienstanbieter, der das Objekt besitzt, Änderungen vornehmen. 
  
Um herauszufinden, welche Eigenschaften für ein Objekt derzeit festgelegt sind, rufen [Sie IMAPIProp::GetPropList](imapiprop-getproplist.md)auf. Mit **der GetPropList-Methode** kann ein Aufrufer herausfinden, was verfügbar ist, bevor versucht wird, eine potenziell nicht vorhandene Eigenschaft zu öffnen. Da es keine Standardeigenschaften gibt, die von allen Objekten eines bestimmten Typs unterstützt werden, ist es unmöglich zu erraten, ob ein Objekt eine bestimmte Eigenschaft unterstützt. Das Aufrufen von **GetPropList** eliminiert die Erraten-Arbeit. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Objekte und -Eigenschaften](mapi-objects-and-properties.md)

