---
title: MAPI-Objekte und-Eigenschaften
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
# <a name="mapi-objects-and-properties"></a>MAPI-Objekte und-Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einige Eigenschaften werden von vielen verschiedenen Objekttypen unterstützt. Die folgenden Eigenschaften sind Beispiele für Eigenschaften, die von mehreren Objekten verwendet werden:
  
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) ist ein binärer Bezeichner, der zum Öffnen von Objekten verwendet wird.
    
- **PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md)) ist eine Konstante, die verwendet wird, um die Art des Objekts zu identifizieren.
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ist eine Zeichenfolge, die verwendet wird, um ein Objekt für den Benutzer zu beschreiben.
    
Andere Eigenschaften sind für einen einzelnen Objekttyp sinnvoll. Die folgenden Eigenschaften sind Beispiele für Eigenschaften, die für einen Objekttyp gelten:
  
- **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) ist eine Zeichenfolge, die zum Beschreiben des Typs einer Nachricht verwendet wird.
    
- **PR_ROWID** ([Pidtagrowid (](pidtagrowid-canonical-property.md)) ist eine ganze Zahl, die verwendet wird, um eine Zeile in einer Tabelle zu identifizieren.
    
- **PR_ATTACH_SIZE** ([Pidtagattachsize (](pidtagattachsize-canonical-property.md)) ist eine ganze Zahl, die zum Speichern der Anzahl von Bytes in einer Anlage verwendet wird.
    
Weitere Eigenschaften sind nur für einen einzelnen Objekttyp in einem bestimmten Zustand anwendbar. Eigenschaften dieses Typs sind in der Regel Nachrichteneigenschaften. Wenn eine Nachricht zuerst erstellt wird, ist Ihre Eigenschaftengruppe sehr klein. Die Anzahl der Eigenschaften, die zum Beschreiben der Nachricht erforderlich sind, wird durch einen Client an einen Empfänger über das Messagingsystem erhöht. Einige dieser hinzugefügten Eigenschaften werden nur in der Nachricht angezeigt, während Sie übermittelt werden, während andere nur in der Nachricht angezeigt werden, während Sie gesendet werden. Nachrichten weisen auch Eigenschaften auf, die der Klasse zugeordnet sind, zu der Sie gehören. Berichtnachrichten haben beispielsweise Eigenschaften, die von Nachrichten anderer Klassen, wie beispielsweise Notizen, nicht unterstützt werden. 
  
Jedes Objekt verfügt über einige erforderliche Eigenschaften und hat möglicherweise andere optionale Eigenschaften. Erforderliche Eigenschaften sind Eigenschaften, die für ein Objekt vorhanden sein müssen, bevor das Objekt mit der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode erfolgreich gespeichert werden kann. Clients oder Dienstanbieter, die ein Objekt verwenden, können nach dem Aufruf von SaveChanges **** von der Verfügbarkeit der erforderlichen Eigenschaften abhängig sein. Das heißt, Sie können sicher sein, dass ein Aufruf der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode oder [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode des Objekts zum Abrufen dieser Eigenschaften erfolgreich ausgeführt werden kann. 
  
Optionale Eigenschaften sind Eigenschaften, die je nach Implementierer des Objekts möglicherweise von einem Objekt unterstützt werden. Ein Client oder Dienstanbieter, der das Objekt verwendet, kann nicht erwarten, dass optionale **** Eigenschaften über die GetProps-oder **OpenProperty** -Methoden verfügbar sind und auf gültige Werte festgelegt werden können. 
  
Eine Liste oder Eigenschaften in dieser Referenz finden Sie unter [MAPI Properties](mapi-properties.md). Beschreibungen der Eigenschaften, die zu jedem der Nachrichtenspeicher-und Adressbuch Objekte gehören, finden Sie in der Erläuterung der Standardschnittstelle des Objekts. Beispielsweise werden Ordner Eigenschaften mit **IMAPIFolder** und Messaging-Benutzereigenschaften mit **IMailUser**besprochen. Nachrichteneigenschaften, einschließlich Berichtsnachrichten Eigenschaften, werden mit **IMessage** und der [Übersicht über Nachrichteneigenschaften](message-properties-overview.md)beschrieben. Eigenschaften, die zu den verschiedenen Tabellentypen gehören, werden im Thema entsprechende [MAPI-Tabellen](mapi-tables.md) beschrieben. Hier werden beispielsweise die Eigenschaften der Hierarchietabelle in den [Hierarchietabellen](hierarchy-tables.md)beschrieben. Eigenschaften, die zu Formular Servern gehören, beschreiben die [Auswahl eines formularEigenschaften Satzes](choosing-a-form-s-property-set.md).
  
Wenn ein Client oder Dienstanbieter die getProps **** -Methode eines Objekts aufruft, um mehrere seiner Eigenschaften abzurufen, und eine dieser Eigenschaften nicht verfügbar ist, gibt GetProps die Warnung MAPI_W_ERRORS_RETURNED zurück. **** Der Aufruf wird als erfolgreich eingestuft, da einige der Eigenschaften zurückgegeben wurden. Wenn ein Client oder Dienstanbieter **OpenProperty** aufruft und die Target-Eigenschaft nicht verfügbar ist, schlägt die Methode mit dem Fehler MAPI_E_NOT_FOUND fehl. Es ist wichtig zu überprüfen, ob eine angeforderte Eigenschaft zurückgegeben wird, bevor Sie mit der Arbeit daran arbeiten. 
  
Abhängig vom Objekt, dem Dienstanbieter, der die Implementierung bereitstellt, und der Eigenschaft kann eine Eigenschaft Lese-/Schreibzugriff oder schreibgeschützt sein. Mit Lese-/Schreibzugriff kann ein Client oder ein Dienstanbieter die Eigenschaft verwenden, um den Wert zu ändern. schreibgeschützte Berechtigung ermöglicht es nur dem Dienstanbieter, der das Objekt besitzt, Änderungen vorzunehmen. 
  
Um genau herauszufinden, welche Eigenschaften derzeit für ein Objekt festgelegt sind, rufen Sie [IMAPIProp::](imapiprop-getproplist.md)getproplist auf. Mit **** der getproplist-Methode kann ein Aufrufer herausfinden, was verfügbar ist, bevor versucht wird, eine potenziell nicht vorhandene Eigenschaft zu öffnen. Da es keinen Standardsatz von Eigenschaften gibt, die von allen Objekten eines bestimmten Typs unterstützt werden, ist es unmöglich zu erraten, ob ein Objekt eine bestimmte Eigenschaft unterstützt. Durch **** das Aufrufen von getproplist wird die vermutungs Arbeit eliminiert. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Objekte und-Eigenschaften](mapi-objects-and-properties.md)

