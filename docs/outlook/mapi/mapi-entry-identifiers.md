---
title: MAPI-Eintragsbezeichner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 84c37696-da7a-42e0-b8c0-29658a6c9a48
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4c414b9f8a1d70fd5eea94da326674a749ccefe2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414963"
---
# <a name="mapi-entry-identifiers"></a>MAPI-Eintragsbezeichner

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eintragsbezeichner sind Binärdaten, die in einer [ENTRYID-Struktur](entryid.md) gespeichert sind und zum eindeutigen Identifizieren und Öffnen eines MAPI-Objekts verwendet werden. Die meisten MAPI-Objekte verfügen über Eintragsbezeichner. Eintragsbezeichner für Objekte sind mit Dateinamen für Dateien vergleichbar. Sie können jedoch nicht übertragen werden und können nicht auf anderen Systemen als dem System verwendet werden, auf dem sie entstanden sind. 
  
## <a name="entry-identifiers"></a>Eintragsbezeichner

Nachrichtenspeicheranbieter weisen Nachrichtenspeichern, Ordnern und Nachrichten Eintragsbezeichner zu. Adressbuchanbieter weisen sie Adressbuchcontainern, Verteilerlisten und Messagingbenutzern zu. Eintragsbezeichner werden auch zum Öffnen eines Objekts verwendet, das durch eine Zeile in einer Tabelle dargestellt wird, z. B. ein Statusobjekt in der Statustabelle. Objekte speichern ihre Eintragsbezeichner in ihrer **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft. 
  
Während Dienstanbieter Eingabebezeichner erstellen, zuweisen und untersuchen, verwenden Clientanwendungen sie nur als Tools zum Öffnen von Objekten. Für Clients sind Eingabebezeichner undurchsichtige Binärdaten und haben nichts mit dem zugrunde liegenden Messagingsystem zu tun. 
  
Clients rufen die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) eines Objekts auf, um die **PR_ENTRYID-Eigenschaft** oder die [IMAPITable::QueryColumns-Methode](imapitable-querycolumns.md) einer Tabelle abzurufen, um die Spalte abzurufen, die die **PR_ENTRYID-Eigenschaft** enthält. 
  
Eintragsbezeichner werden als Parameter an die **Methoden OpenEntry** und **CompareEntryIDs übergeben.** Mehrere MAPI-Objekte implementieren die **Methoden OpenEntry** und **CompareEntryIDs.** Mit **OpenEntry** können Clients ein Objekt öffnen. Mit **CompareEntryIDs** können Clients zwei Eintragsbezeichner vergleichen, um festzustellen, ob sie auf dasselbe Objekt verweisen. Da Eingabebezeichner nicht unbedingt binär vergleichbar sind, müssen Clients sie mit der **CompareEntryIDs-Methode** vergleichen. 
  
Clients sollten immer natürlich ausgerichtete Eintragsbezeichner in ihren Aufrufen an Dienstanbieter übergeben, da Dienstanbieter zwar willkürlich ausgerichtete Eintragsbezeichner behandeln sollten, dies jedoch nicht immer der Fall ist. Eine natürlich ausgerichtete Speicheradresse ermöglicht es dem Computer, auf jeden datentyp zu zugreifen, der an dieser Adresse unterstützt wird, ohne einen Ausrichtungsfehler zu generieren. Der natürliche Ausrichtungsfaktor ist in der Regel der gleiche Ausrichtungsfaktor, der von der Systemspeicherzuweisung verwendet wird, und beträgt in der Regel 8 Byte.
  
Eintragsbezeichner werden in zwei Typen verwendet: kurz- und langfristig. Kurzfristige Eintragsbezeichner können schneller erstellt werden, ihre Eindeutigkeit wird jedoch nur während der Laufzeit der aktuellen Sitzung auf der aktuellen Arbeitsstation garantiert. Langfristige Eintragsbezeichner haben eine längere Lebensdauer. Kurzfristige Eintragsbezeichner werden hauptsächlich für Zeilen in Tabellen und Einträgen in Dialogfeldern verwendet, während langfristige Eintragsbezeichner für viele Objekte wie Nachrichten, Ordner und Verteilerlisten verwendet werden.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Anwendungsentwicklung](mapi-application-development.md)

