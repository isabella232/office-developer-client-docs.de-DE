---
title: MAPI-Objekte und -Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0aebf536-dcfb-406d-86ac-65db98c78139
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7fef84b7519c7a9d6373198283e903fba4fd0780
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411211"
---
# <a name="mapi-objects-and-properties"></a>MAPI-Objekte und -Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einige Eigenschaften werden von vielen verschiedenen Objekttypen unterstützt. Die folgenden Eigenschaften sind Beispiele für Eigenschaften, die von mehreren Objekten verwendet werden:
  
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) ist ein binärer Bezeichner, der zum Öffnen von Objekten verwendet wird.
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) ist eine Konstante, mit der die Art des Objekts identifiziert wird.
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ist eine Zeichenzeichenfolge, die zum Beschreiben eines Objekts für den Benutzer verwendet wird.
    
Andere Eigenschaften sind für einen einzelnen Objekttyp sinnvoll. Die folgenden Eigenschaften sind Beispiele für Eigenschaften, die für einen Objekttyp gelten:
  
- **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) ist eine Zeichenzeichenfolge, die verwendet wird, um den Typ einer Nachricht zu beschreiben.
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) ist eine ganze Zahl, die zum Identifizieren einer Zeile in einer Tabelle verwendet wird.
    
- **PR_ATTACH_SIZE** ([PidTagAttachSize](pidtagattachsize-canonical-property.md)) ist eine ganze Zahl, mit der die Anzahl der Bytes in einer Anlage gespeichert wird.
    
Weitere Eigenschaften gelten nur für einen einzelnen Objekttyp in einem bestimmten Zustand. Eigenschaften dieses Typs sind in der Regel Nachrichteneigenschaften. Wenn eine Nachricht zum ersten Mal erstellt wird, ist ihr Eigenschaftensatz sehr klein. Wenn sie von einem Client über das Messagingsystem an einen Empfänger gesendet wird, nimmt die Anzahl der Eigenschaften zu, die zum Beschreiben der Nachricht erforderlich sind. Einige dieser hinzugefügten Eigenschaften werden nur in der Nachricht angezeigt, während sie zugestellt wird, während andere nur in der Nachricht angezeigt werden, während sie gesendet wird. Nachrichten verfügen auch über Eigenschaften, die der Klasse zugeordnet sind, zu der sie gehören. Berichtsnachrichten verfügen beispielsweise über Eigenschaften, die von Nachrichten anderer Klassen, z. B. Notiznachrichten, nicht unterstützt werden. 
  
Jedes Objekt verfügt über einige erforderliche Eigenschaften und kann auch andere optionale Eigenschaften aufweisen. Erforderliche Eigenschaften sind Eigenschaften, die für ein Objekt vorhanden sein müssen, bevor das Objekt mit seiner [IMAPIProp::SaveChanges-Methode erfolgreich gespeichert werden](imapiprop-savechanges.md) kann. Clients oder Dienstanbieter, die ein Objekt verwenden, können nach dem **SaveChanges-Aufruf** von der Verfügbarkeit der erforderlichen Eigenschaften abhängen. Das heißt, sie können sicherstellen, dass ein Aufruf der [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Objekts oder der [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) zum Abrufen dieser Eigenschaften erfolgreich ist. 
  
Optionale Eigenschaften sind Eigenschaften, die abhängig vom Implementier des Objekts von einem Objekt unterstützt werden können oder nicht. Ein Client oder Dienstanbieter, der das Objekt verwendet, kann nicht erwarten, dass optionale Eigenschaften über die **GetProps-** oder **OpenProperty-Methoden** verfügbar sind und auf gültige Werte festgelegt werden. 
  
Eine Liste oder Eigenschaften in dieser Referenz finden Sie unter [MAPI-Eigenschaften](mapi-properties.md). Beschreibungen der Eigenschaften der einzelnen Nachrichtenspeicher- und Adressbuchobjekte finden Sie in der Erläuterung der Standardschnittstelle des Objekts. Beispielsweise werden Ordnereigenschaften mit **IMAPIFolder** und Nachrichtenbenutzereigenschaften mit **IMailUser erläutert.** Nachrichteneigenschaften, einschließlich Berichtsnachrichteneigenschaften, werden mit **IMessage** und unter [Message Properties Overview beschrieben.](message-properties-overview.md) Eigenschaften, die zu den verschiedenen Tabellentypen gehören, werden im entsprechenden [Thema MAPI Tables](mapi-tables.md) beschrieben. Die Eigenschaften von Hierarchietabellen werden beispielsweise in [Hierarchietabellen beschrieben.](hierarchy-tables.md) Eigenschaften von Formularservern werden unter Auswählen des Eigenschaftensatz eines [Formulars beschrieben.](choosing-a-form-s-property-set.md)
  
Wenn ein Client oder Dienstanbieter die **GetProps-Methode** eines Objekts aufruft, um mehrere seiner Eigenschaften abzurufen, und eine dieser Eigenschaften nicht verfügbar ist, gibt **GetProps** die Warnung MAPI_W_ERRORS_RETURNED. Der Aufruf wird als erfolgreich angesehen, da einige der Eigenschaften zurückgegeben wurden. Wenn ein Client oder Dienstanbieter **OpenProperty aufruft** und die Zieleigenschaft nicht verfügbar ist, schlägt die Methode mit dem Fehler MAPI_E_NOT_FOUND. Es ist wichtig zu überprüfen, ob eine angeforderte Eigenschaft zurückgegeben wird, bevor Sie versuchen, damit zu arbeiten. 
  
Abhängig vom Objekt, dem Dienstanbieter, der die Implementierung liefert, und der Eigenschaft kann eine Eigenschaft über lese-/schreib- oder schreibgeschützte Berechtigungen verfügen. Mit der Lese-/Schreibberechtigung kann ein Client oder Dienstanbieter, der die Eigenschaft verwendet, seinen Wert ändern. Mit der schreibgeschützten Berechtigung kann nur der Dienstanbieter, der das Objekt besitzt, Änderungen vornehmen. 
  
Um herauszufinden, welche Eigenschaften derzeit für ein Objekt festgelegt sind, rufen Sie [IMAPIProp::GetPropList auf.](imapiprop-getproplist.md) Mit **der GetPropList-Methode** kann ein Aufrufer herausfinden, was verfügbar ist, bevor versucht wird, eine potenziell nicht vorhandene Eigenschaft zu öffnen. Da es keinen Standardsatz von Eigenschaften gibt, der von allen Objekten eines bestimmten Typs unterstützt wird, kann nicht erraten werden, ob ein Objekt eine bestimmte Eigenschaft unterstützt. Durch **das Aufrufen von GetPropList** wird die Ratearbeit eliminiert. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Objekte und -Eigenschaften](mapi-objects-and-properties.md)

