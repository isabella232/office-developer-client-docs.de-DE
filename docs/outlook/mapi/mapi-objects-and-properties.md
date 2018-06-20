---
title: MAPI-Objekten und Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0aebf536-dcfb-406d-86ac-65db98c78139
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0efc111523ad285d54fc40e37fe83a1130f1d291
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793030"
---
# <a name="mapi-objects-and-properties"></a>MAPI-Objekten und Eigenschaften

  
  
**Betrifft**: Outlook 
  
Einige Eigenschaften werden von vielen verschiedenen Arten von Objekten unterstützt. Die folgenden Eigenschaften sind Beispiele für Eigenschaften, die von mehreren Objekten verwendet werden:
  
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) ist eine binäre ID verwendet, um Objekte zu öffnen.
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) ist eine Konstante verwendet, um die Art des Objekts zu identifizieren.
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ist eine Zeichenfolge, die ein Objekt, das dem Benutzer beschrieben.
    
Andere Eigenschaften sinnvoll für einen einzelnen Objekttyp an. Die folgenden Eigenschaften sind Beispiele für Eigenschaften, die für einen Objekttyp gelten:
  
- **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) ist eine Zeichenfolge, die den Typ einer Nachricht beschrieben.
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) ist eine ganze Zahl verwendet, um eine Zeile in einer Tabelle zu identifizieren.
    
- **PR_ATTACH_SIZE** ([PidTagAttachSize](pidtagattachsize-canonical-property.md)) ist eine ganze Zahl verwendet, um die Anzahl von Bytes in einer Anlage zu speichern.
    
Andere Eigenschaften sind weiterhin nur für einen Typ des Objekts in einen bestimmten Status. Die Eigenschaften dieses Typs sind in der Regel Nachrichteneigenschaften. Wenn eine Nachricht zuerst erstellt wird, ist eine Gruppe von Eigenschaften sehr gering. Wie sie von einem Client an einem Empfänger über die messaging-System gesendet wird, erhöht die Anzahl der Eigenschaften benötigt werden, um die Nachricht zu beschreiben. Einige dieser Eigenschaften hinzugefügten werden nur in der Nachricht angezeigt, wie er übermittelt werden, während andere nur auf die Nachricht angezeigt, wie sie gesendet werden. Nachrichten müssen auch Eigenschaften, die mit der Klasse verknüpft sind, die sie angehören. Berichtnachrichten haben beispielsweise Eigenschaften, die von Nachrichten von anderen Klassen, wie Hinweis Nachrichten nicht unterstützt werden. 
  
Jedes Objekt verfügt über einige erforderlichen Eigenschaften und möglicherweise oder möglicherweise keinen anderen optionalen Eigenschaften. Erforderliche Eigenschaften sind Eigenschaften, die auf ein Objekt vorhanden sein müssen, bevor das Objekt erfolgreich mit seinem [IMAPIProp::SaveChanges](imapiprop-savechanges.md) gespeichert werden kann. Clients oder Dienstanbieter mithilfe eines Objekts können die Verfügbarkeit der erforderlichen Eigenschaften nach dem Aufruf der **SaveChanges** abhängen. D. h., können sie sicher sein, ein Anruf an des Objekts [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode oder [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode zum Abrufen dieser Eigenschaften erfolgreich ausgeführt werden kann. 
  
Optionale Eigenschaften sind, je nach der Implementierung des Objekts, die möglicherweise oder möglicherweise von einem Objekt nicht unterstützt. Ein Client oder Dienstanbieter mithilfe des Objekts kann nicht erwarten, dass die optionale Eigenschaften über die Methoden **GetProps** oder **OpenProperty** verfügbar sein soll und auf gültige Werte festgelegt werden. 
  
Für eine Liste oder Eigenschaften in dieser Referenz finden Sie unter [MAPI-Eigenschaften](mapi-properties.md). Eine Beschreibung der Eigenschaften von jeder der Nachricht speichern und Address Book-Objekten finden Sie in der Beschreibung der Standardschnittstelle für das Objekt. Beispielsweise sind Ordnereigenschaften mit **IMAPIFolder** und messaging Benutzereigenschaften werden mit **IMailUser**diskutiert. Nachrichteneigenschaften, einschließlich Bericht Nachrichteneigenschaften, werden mit **IMessage** und in [Nachricht Eigenschaften (Übersicht)](message-properties-overview.md)beschrieben. Eigenschaften von den verschiedenen Arten von Tabellen werden in das entsprechende Thema [MAPI-Tabellen](mapi-tables.md) beschrieben. Beispielsweise werden Tabelleneigenschaften Hierarchie in [Hierarchietabellen](hierarchy-tables.md)beschrieben. Eigenschaften von Formular Servern werden bei der [Auswahl eines Formulars-Eigenschaft festgelegt](choosing-a-form-s-property-set.md), beschreibt.
  
Wenn ein Client oder Dienstanbieter ein Objekt **GetProps** -Methode ruft, um verschiedene Eigenschaften abzurufen und eine dieser Eigenschaften nicht verfügbar ist, gibt **GetProps** die Warnung MAPI_W_ERRORS_RETURNED zurück. Der Anruf wird als durchgeführt werden, da einige der Eigenschaften zurückgegeben wurden. Wenn ein Client oder -Anbieter Dienstaufrufen **OpenProperty** und die Target-Eigenschaft nicht verfügbar ist, schlägt die Methode mit dem Fehler MAPI_E_NOT_FOUND fehl. Es ist wichtig, um zu überprüfen, dass eine angeforderte-Eigenschaft zurückgegeben wird, bevor Sie versuchen, die damit arbeiten. 
  
Je nach dem Objekt kann der Dienstanbieter Geben Sie dabei die Implementierung und die Eigenschaft eine Eigenschaft Lese-/Schreibzugriff oder nur-Lese-Berechtigung verfügen. Lese-/Schreibberechtigung für ermöglicht einen Client oder Dienstanbieter mithilfe der-Eigenschaft, um dessen Wert zu ändern. Nur-Lese-Berechtigung können nur den Dienstanbieter das Objekt besitzt Änderungen vornehmen. 
  
Um herauszufinden, die genau die Eigenschaften für ein Objekt derzeit festgelegt werden, rufen Sie [IMAPIProp::GetPropList](imapiprop-getproplist.md). Die **GetPropList** -Methode können einen Anrufer herauszufinden, was verfügbar ist, bevor der Versuch, eine potenziell nicht vorhandene Eigenschaft öffnen erfolgt. Da es keine Standardsatz von Eigenschaften, die allen Objekten eines bestimmten Typs unterstützt werden ist, ist es unmöglich zu erraten sein, unabhängig davon, ob ein Objekt eine bestimmte Eigenschaft unterstützt. Aufrufen von **GetPropList** entfällt die Schätzwert Arbeit. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Objekten und Eigenschaften](mapi-objects-and-properties.md)

