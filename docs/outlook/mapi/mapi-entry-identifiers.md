---
title: MAPI-Eintrags-IDs
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
# <a name="mapi-entry-identifiers"></a>MAPI-Eintrags-IDs

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eintrags-IDs sind in einer Eintrags- [](entryid.md) ID gespeicherte Binärdaten, die zum eindeutigen identifizieren und Öffnen eines MAPI-Objekts verwendet werden. Die meisten MAPI-Objekte besitzen Eingabe-IDs. Eintragsbezeichner für Objekte sind analog zu Dateinamen für Dateien. Sie sind jedoch nicht übertragbar und können nicht auf anderen Systemen als dem System verwendet werden, auf dem Sie Ihren Ursprung hatten. 
  
## <a name="entry-identifiers"></a>EintragsBezeichner

Nachrichtenspeicher Anbieter weisen Nachrichten speichern, Ordnern und Nachrichten Eingabe Bezeichner zu. Adressbuchanbieter weisen Adressbuchcontainer, Verteilerlisten und Messagingbenutzer zu. Eintrags-IDs werden auch verwendet, um ein Objekt zu öffnen, das durch eine Zeile in einer Tabelle dargestellt wird, beispielsweise ein Status-Objekt in der Statustabelle. Objekte speichern Ihre Eintrags-IDs in Ihrer **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft. 
  
Während Dienstanbieter Eintrags-IDs erstellen, zuweisen und untersuchen, verwenden Clientanwendungen diese nur als Tools zum Öffnen von Objekten. Für Clients sind Eingabe-IDs undurchsichtige Teile von Binärdaten und haben nichts mit dem zugrunde liegenden Messagingsystem zu tun. 
  
Clients rufen die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode eines Objekts auf, um die **PR_ENTRYID** -Eigenschaft oder die [IMAPITable:: QueryColumns](imapitable-querycolumns.md) -Methode einer Tabelle abzurufen, um die Spalte abzurufen, die die **PR_ENTRYID** -Eigenschaft enthält. 
  
Eintrags-IDs werden als Parameter an **** die OpenEntry-und **CompareEntryIDs** -Methoden übergeben. Mehrere MAPI-Objekte implementieren **** die OpenEntry-und die **CompareEntryIDs** -Methode. Mit **OpenEntry**können Clients ein Objekt öffnen. Mit **CompareEntryIDs**können Clients zwei Eintragsbezeichner vergleichen, um zu bestimmen, ob Sie auf dasselbe Objekt verweisen. Da Eintrags-IDs nicht unbedingt Binär vergleichbar sind, müssen Clients Sie mit der **CompareEntryIDs** -Methode vergleichen. 
  
Clients sollten in ihren Aufrufen an Dienstanbieter immer natürlich ausgerichtete Eintrags-IDs weiterleiten, da Dienstanbieter, die Eingabe-IDs, die willkürlich ausgerichtet werden, behandeln sollten, dies ist jedoch nicht immer der Fall. Eine natürlich ausgerichtete Speicheradresse ermöglicht es dem Computer, auf einen beliebigen Datentyp zuzugreifen, der an dieser Adresse unterstützt wird, ohne einen Ausrichtungsfehler zu generieren. Der natürliche Ausrichtungs Faktor ist in der Regel derselbe Ausrichtungs Faktor, der von der systemspeicherzuweisung verwendet wird und in der Regel 8 Bytes beträgt.
  
Eintrags-IDs gibt es in zwei Arten: kurz-und langfristig. Kurzfristige Eintragsbezeichner sind schneller zu konstruieren, ihre Eindeutigkeit wird jedoch nur über die Lebensdauer der aktuellen Sitzung auf der aktuellen Arbeitsstation gewährleistet. Langfristige Eintrags-IDs haben eine längere Lebensdauer. Kurzfristige Eintragsbezeichner werden hauptsächlich für Zeilen in Tabellen und Einträgen in Dialogfeldern verwendet, während langfristige Eintragsbezeichner für viele Objekte wie Nachrichten, Ordner und Verteilerlisten verwendet werden.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Anwendungsentwicklung](mapi-application-development.md)

