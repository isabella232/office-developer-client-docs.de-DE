---
title: Arten von Tabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1fc4f20-511f-4721-8f09-ec2a5fd0ccb0
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 36456c6226b2eb74b8f15995ad0925381302523a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795768"
---
# <a name="types-of-tables"></a>Arten von Tabellen

  
  
**Betrifft**: Outlook 
  
Es gibt viele verschiedene Typen von Tabellen, jede Art von den Informationen, den er stellt unterschieden. Tabellen-Clientanwendungen und Dienstanbieter leicht aufrufen und bearbeiten wichtigen Eigenschaften der viele Objekttypen aktivieren. 
  
Einige Tabellen, z. B. Inhalt Tabellen, bieten eine alternative zum Zugreifen auf Eigenschaften. Beispielsweise kann ein Client Abrufen des Betreffs einer Nachricht – seine Eigenschaft **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) – entweder direkt aus der Nachricht durch Aufrufen der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode oder über die Meldung Inhaltstabelle. Andere Tabellen sind die einzige Möglichkeit, Eigenschaften des Access-Objekts. Beispielsweise kann kein Client eine Anlage **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))-Eigenschaft zugreifen, indem **IMAPIProp::GetProps**; Es muss immer die Anlagentabelle der Nachricht abrufen, mit der sie verbunden ist. **PR_ATTACH_METHOD** ist eine erforderliche Spalte in allen Anlagentabellen. 
  
Eine Tabellenansicht kann es sich um statische oder dynamische sein. Eine statische Tabelle-Ansicht führen Änderungen an den zugrunde liegenden Daten nicht die Ansicht aktualisiert werden. Nach die Ansicht instanziiert wurde, wird es nicht geändert. Benutzer von statischen Tabellen können der Änderungen an Daten über Tabelle Benachrichtigungen darüber informiert werden. Eine dynamische Tabellenansicht wird aktualisiert, wenn die Daten geändert werden. Es gibt zwei Arten von dynamischen Tabellen: eine, die die Spalten in der jede Zeile, aber die Zeilen aktualisiert bleiben statische und diejenige, die Spalten und Zeilen aktualisiert. Letztere Typ der Tabelle entspricht genau immer die zugrunde liegenden Daten.
  
Tabellen ist eine Standardspalte festgelegt, den minimalen Satz von Spalten an, denen ein Client oder Dienstanbieter zu erwarten ist beim Abrufen von Zeilen aus einer Tabelle, die noch nicht durch eine [IMAPITable::SetColumns](imapitable-setcolumns.md) betroffen aufrufen. Clients und Dienstanbieter können Spalten an, um Spalten hinzufügen oder Entfernen aus dieser Standard festlegen, indem der **SetColumns** -Methode aufrufen. Änderungen können statisch oder dynamisch vorgenommen werden eine Clientanforderung folgen. Nicht alle Tabellen unterstützen dynamische Spalte Set Änderung. 
  
Die MAPI-Tabellen und ihre Implementierer und Benutzer sind:
  
|**Table**|**Implementierer**|
|:-----|:-----|
|Anlage  <br/> |Nachricht Zeichenfolgeneigenschaften implementiert. Wird von Clients und Transportanbieter verwendet.  <br/> |
|Inhalt  <br/> |Durch die Nachricht implementiert speichern und address Book-Anbieter. Wird von Clients verwendet.  <br/> |
|Anzeige  <br/> |Von MAPI implementierte und Dienstanbieter. MAPI verwendet und Dienstanbieter.  <br/> |
|Hierarchie  <br/> |Durch die Nachricht implementiert speichern und address Book-Anbieter. Wird von Clients verwendet.  <br/> |
|Messagingdiensts  <br/> |Von MAPI implementiert. Wird von Clients verwendet.  <br/> |
|Nachrichtenspeicher  <br/> |Von MAPI implementiert. Wird von Clients verwendet.  <br/> |
|Einmaligen  <br/> |Von adressbuchanbietern implementierte implementiert. Von MAPI verwendet.  <br/> |
|Ausgehende Warteschlange  <br/> |Nachricht Zeichenfolgeneigenschaften implementiert. Von MAPI-Warteschlange verwendet.  <br/> |
|Profil  <br/> |Von MAPI implementiert. Wird von Clients verwendet.  <br/> |
|Provider  <br/> |Von MAPI implementiert. Wird von Clients verwendet.  <br/> |
|Ordner empfangen  <br/> |Nachricht Zeichenfolgeneigenschaften implementiert. Wird von Clients verwendet.  <br/> |
|Recipient  <br/> |Nachricht Zeichenfolgeneigenschaften implementiert. Wird von Clients und Transportanbieter verwendet.  <br/> |
|Status  <br/> |Von MAPI implementierte und Dienstanbieter. Wird von Clients verwendet.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

