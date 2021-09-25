---
title: MAPI-Eintragsbezeichner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 84c37696-da7a-42e0-b8c0-29658a6c9a48
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cdd5486bc68a6799c4da2d44ffc033176d6ada31
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579614"
---
# <a name="mapi-entry-identifiers"></a>MAPI-Eintragsbezeichner

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eintragsbezeichner sind Binärdatenelemente, die in einer [ENTRYID-Struktur](entryid.md) gespeichert sind und verwendet werden, um ein MAPI-Objekt eindeutig zu identifizieren und zu öffnen. Die meisten MAPI-Objekte verfügen über Eintragsbezeichner. Eintragsbezeichner für Objekte entsprechen Dateinamen für Dateien. Sie können jedoch nicht übertragen werden und können nicht auf anderen Systemen als dem System verwendet werden, auf dem sie ihren Ursprung haben. 
  
## <a name="entry-identifiers"></a>Eintragsbezeichner

Nachrichtenspeicheranbieter weisen Nachrichtenspeichern, Ordnern und Nachrichten Eintragsbezeichner zu. Adressbuchanbieter weisen sie Adressbuchcontainern, Verteilerlisten und Messagingbenutzern zu. Eintragsbezeichner werden auch verwendet, um ein Objekt zu öffnen, das durch eine Zeile in einer Tabelle dargestellt wird, z. B. ein Statusobjekt in der Statustabelle. Objekte speichern ihre Eintragsbezeichner in ihrer **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft. 
  
Während Dienstanbieter Eintragsbezeichner erstellen, zuweisen und untersuchen, verwenden Clientanwendungen sie nur als Tools zum Öffnen von Objekten. Für Clients sind Eintragsbezeichner undurchsichtige Binärdaten und haben nichts mit dem zugrunde liegenden Messagingsystem zu tun. 
  
Clients rufen die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) eines Objekts auf, um seine **PR_ENTRYID-Eigenschaft** oder die [IMAPITable::QueryColumns-Methode](imapitable-querycolumns.md) einer Tabelle abzurufen, um die Spalte abzurufen, die die **PR_ENTRYID-Eigenschaft** enthält. 
  
Eintragsbezeichner werden als Parameter an die **Methoden OpenEntry** und **CompareEntryIDs** übergeben. Mehrere MAPI-Objekte implementieren die **Methoden OpenEntry** und **CompareEntryIDs.** Mit **OpenEntry** können Clients ein Objekt öffnen. Mit **CompareEntryIDs** können Clients zwei Eintragsbezeichner vergleichen, um zu bestimmen, ob sie auf dasselbe Objekt verweisen. Da Eintragsbezeichner nicht unbedingt binär vergleichbar sind, müssen Clients sie mit der **CompareEntryIDs-Methode** vergleichen. 
  
Clients sollten in ihren Aufrufen an Dienstanbieter immer natürlich ausgerichtete Eintragsbezeichner übergeben, da dies nicht immer der Fall ist, obwohl Dienstanbieter willkürlich ausgerichtete Eintragsbezeichner behandeln sollten. Eine natürlich ausgerichtete Speicheradresse ermöglicht es dem Computer, auf jeden Datentyp zuzugreifen, der an dieser Adresse unterstützt wird, ohne dass ein Ausrichtungsfehler generiert wird. Der natürliche Ausrichtungsfaktor ist in der Regel derselbe Ausrichtungsfaktor, der von der Systemspeicher-Verteilfunktion verwendet wird, und beträgt in der Regel 8 Bytes.
  
Eintragsbezeichner werden in zwei Typen verwendet: kurz- und langfristig. Kurzfristige Eintragsbezeichner lassen sich schneller erstellen, aber ihre Eindeutigkeit ist nur während der Gesamten Lebensdauer der aktuellen Sitzung auf der aktuellen Arbeitsstation gewährleistet. Langfristige Eintragsbezeichner haben eine längere Lebensdauer. Bezeichner für kurzfristige Einträge werden in erster Linie für Zeilen in Tabellen und Einträge in Dialogfeldern verwendet, während langfristige Eintragsbezeichner für viele Objekte wie Nachrichten, Ordner und Verteilerlisten verwendet werden.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Anwendungsentwicklung](mapi-application-development.md)

