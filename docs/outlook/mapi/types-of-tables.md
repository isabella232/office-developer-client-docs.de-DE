---
title: Tabellentypen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a1fc4f20-511f-4721-8f09-ec2a5fd0ccb0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6a6fb115d3a3105777b1b0e68595c960df0a92b2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566248"
---
# <a name="types-of-tables"></a>Tabellentypen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Es gibt viele verschiedene Tabellentypen, die jeweils durch die darin enthaltenen Informationen unterschieden werden. Tabellen ermöglichen Clientanwendungen und Dienstanbietern den einfachen Zugriff auf die wichtigen Eigenschaften vieler Objekttypen und deren Bearbeitung. 
  
Einige Tabellen, z. B. Inhaltstabellen, bieten eine alternative Möglichkeit für den Zugriff auf Eigenschaften. Beispielsweise kann ein Client den Betreff einer Nachricht – seine **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) -Eigenschaft – entweder direkt aus der Nachricht abrufen, indem er seine [IMAPIProp::GetProps-Methode aufruft](imapiprop-getprops.md) oder über die Inhaltstabelle der Nachricht. Andere Tabellen bieten die einzige Möglichkeit, auf Objekteigenschaften zuzugreifen. Beispielsweise kann ein Client nicht auf die **Eigenschaft PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) einer Anlage zugreifen, indem **er IMAPIProp::GetProps**; Sie muss immer die Anlagentabelle der Nachricht abrufen, an die sie angefügt ist. **PR_ATTACH_METHOD** ist eine erforderliche Spalte in allen Anlagentabellen. 
  
Eine Tabellenansicht kann statisch oder dynamisch sein. Bei einer statischen Tabellenansicht führen Änderungen an den zugrunde liegenden Daten nicht dazu, dass die Ansicht aktualisiert wird. Nachdem die Ansicht instanziiert wurde, wird sie nicht mehr geändert. Benutzer statischer Tabellen können über Änderungen an Daten über Tabellenbenachrichtigungen informiert werden. Eine dynamische Tabellenansicht wird aktualisiert, wenn Änderungen an den Daten vorgenommen werden. Es gibt zwei Arten dynamischer Tabellen: eine, die die Spalten jeder Zeile aktualisiert, die Zeilen bleiben jedoch statisch und eine, die sowohl die Spalten als auch die Zeilen aktualisiert. Dieser letzte Tabellentyp gibt immer genau die zugrunde liegenden Daten wieder.
  
Tabellen haben einen Standardspaltensatz, den minimalen Satz von Spalten, den ein Client oder Dienstanbieter beim Abrufen von Zeilen aus einer Tabelle erwarten kann, die noch nicht von einem [IMAPITable::SetColumns-Aufruf](imapitable-setcolumns.md) betroffen ist. Clients und Dienstanbieter können Spalten zu diesem Standardsatz hinzufügen oder spalten daraus entfernen, indem sie die **SetColumns-Methode** aufrufen. Änderungen können entweder statisch oder dynamisch nach einer Clientanforderung vorgenommen werden. Nicht alle Tabellen unterstützen dynamische Spaltensatzänderungen. 
  
Die MAPI-Tabellen und deren Implementierer und Benutzer sind:
  
|**Table**|**Implementierer**|
|:-----|:-----|
|Attachment  <br/> |Implementiert von Nachrichtenspeicheranbietern. Wird von Clients und Transportanbietern verwendet.  <br/> |
|Inhalt  <br/> |Implementiert von Nachrichtenspeicher- und Adressbuchanbietern. Wird von Clients verwendet.  <br/> |
|Anzeige  <br/> |Implementiert von MAPI und Dienstanbietern. Wird von MAPI und Dienstanbietern verwendet.  <br/> |
|Hierarchie  <br/> |Implementiert von Nachrichtenspeicher- und Adressbuchanbietern. Wird von Clients verwendet.  <br/> |
|Nachrichtendienst  <br/> |Implementiert von MAPI. Wird von Clients verwendet.  <br/> |
|Nachrichtenspeicher  <br/> |Implementiert von MAPI. Wird von Clients verwendet.  <br/> |
|Einmaliges  <br/> |Implementiert von Adressbuchanbietern. Wird von MAPI verwendet.  <br/> |
|Ausgehende Warteschlange  <br/> |Implementiert von Nachrichtenspeicheranbietern. Wird vom MAPI-Spooler verwendet.  <br/> |
|Profil  <br/> |Implementiert von MAPI. Wird von Clients verwendet.  <br/> |
|Anbieter  <br/> |Implementiert von MAPI. Wird von Clients verwendet.  <br/> |
|Ordner empfangen  <br/> |Implementiert von Nachrichtenspeicheranbietern. Wird von Clients verwendet.  <br/> |
|Empfänger  <br/> |Implementiert von Nachrichtenspeicheranbietern. Wird von Clients und Transportanbietern verwendet.  <br/> |
|Status  <br/> |Implementiert von MAPI und Dienstanbietern. Wird von Clients verwendet.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

