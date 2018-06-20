---
title: MAPI-Eintragsbezeichner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 84c37696-da7a-42e0-b8c0-29658a6c9a48
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b8212f4a055125858b77ee615a5d929a4a62bb82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792976"
---
# <a name="mapi-entry-identifiers"></a>MAPI-Eintragsbezeichner

  
  
**Betrifft**: Outlook 
  
Eintragsbezeichner sind Binärdaten in ein [ENTRYID](entryid.md) -Struktur gespeichert, mit denen eindeutig zu identifizieren, und öffnen Sie ein MAPI-Objekt. Die meisten MAPI-Objekte weisen Eintragsbezeichner. Eintragsbezeichner für Objekte sind analog zu Dateinamen für Dateien. Allerdings sind nicht Übertragungseinehit und kann nicht verwendet werden, auf anderen Systemen als das System, dem sie auf stammen. 
  
## <a name="entry-identifiers"></a>Eintragsbezeichner

Nachricht Anbieter Rolle Eintragsbezeichner Nachrichtenspeicher, Ordner und Nachrichten. von adressbuchanbietern implementierte weisen Sie diese Adresse Adressbuch Container, Verteilerlisten und messaging-Benutzer. Eintragsbezeichner dienen auch zum Öffnen eines Objekts, um eine Zeile in einer Tabelle, wie ein Statusobjekt in der Tabelle "Status" dargestellt. Speichern von Objekten ihre Eintragsbezeichner in ihre **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft. 
  
Dienstanbieter erstellen, zuweisen und untersuchen-Eintragsbezeichner-Verwendung-Clientanwendungen deren nur als Tools für Objekte geöffnet. Clients Eintragsbezeichner undurchsichtig Datenelemente binary und nichts mit der zugrunde liegenden messaging-System zu tun haben. 
  
Clients rufen Sie ein Objekt [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode, um dessen **PR_ENTRYID** -Eigenschaft abzurufen oder eine Tabelle [IMAPITable::QueryColumns](imapitable-querycolumns.md) -Methode, um die Spalte abzurufen, die die **PR_ENTRYID** -Eigenschaft enthält. 
  
Eintragsbezeichner werden als Parameter an die Methoden **OpenEntry** und **CompareEntryIDs** übergeben. Mehrere MAPI-Objekte implementieren die **OpenEntry** und **CompareEntryIDs** -Methoden. Clients können mit **OpenEntry**ein Objekt zu öffnen. **CompareEntryIDs**können Clients im Vergleich zu zwei Eintragsbezeichner, um zu bestimmen, ob sie sich auf dasselbe Objekt verweisen. Da Eintragsbezeichner nicht notwendigerweise binary sind vergleichbar, Clients müssen sie vergleichen von der **CompareEntryIDs** -Methode. 
  
Clients sollte immer natürlich ausgerichtet-Eintragsbezeichner in ihre Anrufe für Dienstanbieter, übergeben werden, da zwar Dienstanbieter Eintragsbezeichner behandelt werden sollen, die willkürlich ausgerichtet werden, dies nicht immer der Fall ist. Eine Adresse natürlich ausgerichteten Speicher ermöglicht den Computer, der einen beliebigen Datentyp zugreifen, die an dieser Adresse ohne Ausrichtungsfehler durch eine generieren unterstützt. Faktor natürlichen Ausrichtung ist in der Regel den gleichen Ausrichtung Faktor durch das System Arbeitsspeicher Zuweisung verwendet und ist in der Regel 8 Bytes.
  
Eintragsbezeichner gibt zwei Arten: kurzfristigen und langfristigen. Kurzfristige-Eintragsbezeichner sind schneller zu erstellen, aber ihre Eindeutigkeit wird sichergestellt, dass nur während der Lebensdauer der aktuellen Sitzung auf der Arbeitsstation. Langfristige-Eintragsbezeichner verfügen über einen längeren Lebensdauer. Kurzfristige-Eintragsbezeichner werden in erster Linie für Zeilen in Tabellen und Einträge in Dialogfeldern verwendet, während die langfristige-Eintragsbezeichner dienen für viele Objekte wie Dateien, Ordner und Verteilerlisten.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Anwendungsentwicklung](mapi-application-development.md)

