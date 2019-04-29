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
  
Es gibt viele verschiedene Typen von Tabellen, wobei jeder Typ durch die Informationen differenziert wird, die er präsentiert. Mit Tabellen können Clientanwendungen und Dienstanbieter problemlos auf die wichtigen Eigenschaften vieler Objekttypen zugreifen und diese bearbeiten. 
  
Einige Tabellen, wie Inhaltstabellen, bieten eine alternative Möglichkeit, auf Eigenschaften zuzugreifen. Beispielsweise kann ein Client den Betreff einer Nachricht abrufen – seine **PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md))-Eigenschaft, entweder direkt aus der Nachricht durch Aufrufen seiner [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode oder über die Inhaltstabelle der Nachricht. Andere Tabellen bieten die einzige Möglichkeit, auf Objekteigenschaften zuzugreifen. Ein Client kann beispielsweise nicht auf die **PR_ATTACH_METHOD** ([pidtagattachmethod (](pidtagattachmethod-canonical-property.md))-Eigenschaft einer Anlage zugreifen, indem er **IMAPIProp::** GetProps aufruft. Sie muss immer die Attachment-Tabelle der Nachricht abrufen, an die Sie angefügt ist. **PR_ATTACH_METHOD** ist eine erforderliche Spalte in allen Attachment-Tabellen. 
  
Eine Tabellenansicht kann statisch oder dynamisch sein. Bei einer statischen Tabellenansicht führen Änderungen an den zugrunde liegenden Daten nicht dazu, dass die Ansicht aktualisiert wird. Sobald die Ansicht instanziiert wurde, wird Sie nicht geändert. Benutzer von statischen Tabellen können über Änderungen an Daten über Tabellen Benachrichtigungen informiert werden. Eine dynamische Tabellenansicht wird aktualisiert, wenn Änderungen an den Daten vorgenommen werden. Es gibt zwei Arten von dynamischen Tabellen: eine, die die Spalten jeder Zeile aktualisiert, aber die Zeilen bleiben statisch und eine, die sowohl die Spalten als auch die Zeilen aktualisiert. Dieser zweite Tabellentyp reflektiert die zugrunde liegenden Daten immer genau.
  
Tabellen verfügen über eine Standardspaltengruppe, die Mindestgruppe von Spalten, die ein Client oder Dienstanbieter beim Abrufen von Zeilen aus einer Tabelle erwarten kann, die noch nicht von einem [IMAPITable::](imapitable-setcolumns.md) SetColumns-Aufruf betroffen waren. Clients und Dienstanbieter können Spalten zu diesem Standardsatz hinzufügen oder diese entfernen, indem Sie **** die SetColumns-Methode aufrufen. Änderungen können nach einer Clientanforderung statisch oder dynamisch vorgenommen werden. Nicht alle Tabellen unterstützen die Änderung des dynamischen Spaltensatzes. 
  
Die MAPI-Tabellen und ihre Implementierer und Benutzer sind:
  
|**Table**|**Implementierer**|
|:-----|:-----|
|Attachment  <br/> |Von Nachrichtenspeicher Anbietern implementiert. Wird von Clients und Transportanbietern verwendet.  <br/> |
|Inhalt  <br/> |Von Nachrichtenspeicher-und Adressbuch Anbietern implementiert. Von Clients verwendet.  <br/> |
|Anzeige  <br/> |Von MAPI und Dienstanbietern implementiert. Wird von MAPI-und Dienstanbietern verwendet.  <br/> |
|Hierarchie  <br/> |Von Nachrichtenspeicher-und Adressbuch Anbietern implementiert. Von Clients verwendet.  <br/> |
|Nachrichtendienst  <br/> |Von MAPI implementiert. Von Clients verwendet.  <br/> |
|Nachrichtenspeicher  <br/> |Von MAPI implementiert. Von Clients verwendet.  <br/> |
|Einmaliges  <br/> |Von Adressbuch Anbietern implementiert. Von MAPI verwendet.  <br/> |
|Ausgehende Warteschlange  <br/> |Von Nachrichtenspeicher Anbietern implementiert. Wird von MAPI-Spooler verwendet.  <br/> |
|Profil  <br/> |Von MAPI implementiert. Von Clients verwendet.  <br/> |
|Anbieter  <br/> |Von MAPI implementiert. Von Clients verwendet.  <br/> |
|Ordner empfangen  <br/> |Von Nachrichtenspeicher Anbietern implementiert. Von Clients verwendet.  <br/> |
|Empfänger  <br/> |Von Nachrichtenspeicher Anbietern implementiert. Wird von Clients und Transportanbietern verwendet.  <br/> |
|Status  <br/> |Von MAPI und Dienstanbietern implementiert. Von Clients verwendet.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

