---
title: Tabellentypen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1fc4f20-511f-4721-8f09-ec2a5fd0ccb0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 732b3d724c855d978250afff3d05c7f19909a5b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426464"
---
# <a name="types-of-tables"></a>Tabellentypen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Es gibt viele verschiedene Arten von Tabellen, die sich durch die dargestellten Informationen unterscheiden. Mit Tabellen können Clientanwendungen und Dienstanbieter problemlos auf die wichtigen Eigenschaften vieler Objekttypen zugreifen und diese bearbeiten. 
  
Einige Tabellen, z. B. Inhaltstabellen, bieten eine alternative Möglichkeit für den Zugriff auf Eigenschaften. Ein Client kann beispielsweise den Betreff einer Nachricht – seine **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))-Eigenschaft – entweder direkt aus der Nachricht abrufen, indem er die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) oder die Inhaltstabelle der Nachricht aufruft. Andere Tabellen bieten die einzige Möglichkeit, auf Objekteigenschaften zu zugreifen. Beispielsweise kann ein Client nicht auf die **PR_ATTACH_METHOD** -[PidTagAttachMethod](pidtagattachmethod-canonical-property.md)-Eigenschaft einer Anlage zugreifen, indem **er IMAPIProp::GetProps aufruft.** Sie muss immer die Anlagentabelle der Nachricht abrufen, an die sie angefügt ist. **PR_ATTACH_METHOD** ist eine erforderliche Spalte in allen Anlagentabellen. 
  
Eine Tabellenansicht kann statisch oder dynamisch sein. Bei einer statischen Tabellenansicht führen Änderungen an den zugrunde liegenden Daten nicht dazu, dass die Ansicht aktualisiert wird. Nachdem die Ansicht instanziiert wurde, ändert sie sich nicht. Benutzer statischer Tabellen können über Tabellenbenachrichtigungen über Änderungen an Daten informiert werden. Eine dynamische Tabellenansicht wird aktualisiert, wenn Änderungen an den Daten vorgenommen werden. Es gibt zwei Arten von dynamischen Tabellen: eine, die die Spalten jeder Zeile aktualisiert, aber die Zeilen bleiben statisch, und eine, die sowohl die Spalten als auch die Zeilen aktualisiert. Dieser letzte Tabellentyp spiegelt immer genau die zugrunde liegenden Daten wider.
  
Tabellen verfügen über einen Standardspaltensatz, den minimalen Satz von Spalten, den ein Client oder Dienstanbieter beim Abrufen von Zeilen aus einer Tabelle erwartet, die noch nicht von einem [IMAPITable::SetColumns-Aufruf](imapitable-setcolumns.md) betroffen ist. Clients und Dienstanbieter können Spalten zu diesem Standardsatz hinzufügen oder aus diesem Standardsatz entfernen, indem sie die **SetColumns-Methode** aufrufen. Änderungen können entweder statisch oder dynamisch nach einer Clientanforderung vorgenommen werden. Nicht alle Tabellen unterstützen dynamische Spaltensatzänderungen. 
  
Die MAPI-Tabellen und ihre Implementierer und Benutzer sind:
  
|**Table**|**Implementierer**|
|:-----|:-----|
|Attachment  <br/> |Implementiert von Nachrichtenspeicheranbietern. Wird von Clients und Transportanbietern verwendet.  <br/> |
|Inhalt  <br/> |Implementiert von Nachrichtenspeicher- und Adressbuchanbietern. Wird von Clients verwendet.  <br/> |
|Anzeigen  <br/> |Implementiert von MAPI und Dienstanbietern. Wird von MAPI und Dienstanbietern verwendet.  <br/> |
|Hierarchie  <br/> |Implementiert von Nachrichtenspeicher- und Adressbuchanbietern. Wird von Clients verwendet.  <br/> |
|Nachrichtendienst  <br/> |Implementiert von MAPI. Wird von Clients verwendet.  <br/> |
|Nachrichtenspeicher  <br/> |Implementiert von MAPI. Wird von Clients verwendet.  <br/> |
|Einmal  <br/> |Implementiert von Adressbuchanbietern. Wird von MAPI verwendet.  <br/> |
|Ausgehende Warteschlange  <br/> |Implementiert von Nachrichtenspeicheranbietern. Wird vom MAPI-Spooler verwendet.  <br/> |
|Profil  <br/> |Implementiert von MAPI. Wird von Clients verwendet.  <br/> |
|Anbieter  <br/> |Implementiert von MAPI. Wird von Clients verwendet.  <br/> |
|Ordner empfangen  <br/> |Implementiert von Nachrichtenspeicheranbietern. Wird von Clients verwendet.  <br/> |
|Empfänger  <br/> |Implementiert von Nachrichtenspeicheranbietern. Wird von Clients und Transportanbietern verwendet.  <br/> |
|Status  <br/> |Implementiert von MAPI und Dienstanbietern. Wird von Clients verwendet.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

