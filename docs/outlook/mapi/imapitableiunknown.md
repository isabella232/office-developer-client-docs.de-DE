---
title: IMAPITable IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable
api_type:
- COM
ms.assetid: f25be2b1-0f94-4a0c-b29d-d2201dc70ab7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8a7e5e2d599f64eeb8c9a33c45ba91e8820e2210
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556477"
---
# <a name="imapitable--iunknown"></a>IMAPITable : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt eine schreibgeschützte Ansicht einer Tabelle bereit. **IMAPITable** wird von Clients und Dienstanbietern verwendet, um die Darstellung einer Tabelle zu bearbeiten. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Table-Objekte  <br/> |
|Implementiert von:  <br/> |Dienstanbieter und MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen, Dienstanbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPITable  <br/> |
|Zeigertyp:  <br/> |LPMAPITABLE  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[Getlasterror](imapitable-getlasterror.md) <br/> |Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler in der Tabelle enthält.  <br/> |
|[Beraten](imapitable-advise.md) <br/> |Registriert sich, um Benachrichtigungen über angegebene Ereignisse zu erhalten, die sich auf die Tabelle auswirken.  <br/> |
|[Unadvise](imapitable-unadvise.md) <br/> |Bricht das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der **IMAPITable::Advise-Methode** eingerichtet wurden.  <br/> |
|[Getstatus](imapitable-getstatus.md) <br/> |Gibt den Status und Typ der Tabelle zurück.  <br/> |
|[SetColumns](imapitable-setcolumns.md) <br/> |Definiert die bestimmten Eigenschaften und die Reihenfolge der Eigenschaften, die als Spalten in der Tabelle angezeigt werden sollen.  <br/> |
|[QueryColumns](imapitable-querycolumns.md) <br/> |Gibt eine Liste der Spalten für die Tabelle zurück.  <br/> |
|[GetRowCount](imapitable-getrowcount.md) <br/> |Gibt die Gesamtzahl der Zeilen in der Tabelle zurück.  <br/> |
|[SeekRow](imapitable-seekrow.md) <br/> |Verschiebt den Cursor an eine bestimmte Position in der Tabelle.  <br/> |
|[SeekRowApprox](imapitable-seekrowapprox.md) <br/> |Verschiebt den Cursor an eine ungefähre Bruchposition in der Tabelle.  <br/> |
|[QueryPosition](imapitable-queryposition.md) <br/> |Ruft die aktuelle Tabellenzeilenposition des Cursors basierend auf einem Bruchwert ab.  <br/> |
|[FindRow](imapitable-findrow.md) <br/> |Sucht die nächste Zeile in einer Tabelle, die bestimmten Suchkriterien entspricht.  <br/> |
|[Restrict](imapitable-restrict.md) <br/> |Wendet einen Filter auf eine Tabelle an, wodurch der Zeilensatz auf die Zeilen reduziert wird, die den angegebenen Kriterien entsprechen.  <br/> |
|[CreateBookmark](imapitable-createbookmark.md) <br/> |Markiert die aktuelle Position der Tabelle.  <br/> |
|[FreeBookmark](imapitable-freebookmark.md) <br/> |Gibt den Speicher frei, der einer Textmarke zugeordnet ist.  <br/> |
|[SortTable](imapitable-sorttable.md) <br/> |Sortiert die Zeilen der Tabelle anhand von Sortierkriterien.  <br/> |
|[QuerySortOrder](imapitable-querysortorder.md) <br/> |Ruft die aktuelle Sortierreihenfolge für eine Tabelle ab.  <br/> |
|[QueryRows](imapitable-queryrows.md) <br/> |Gibt eine oder mehrere Zeilen aus einer Tabelle zurück, beginnend an der aktuellen Cursorposition.  <br/> |
|[Abbruch](imapitable-abort.md) <br/> |Beendet alle asynchronen Vorgänge, die derzeit für die Tabelle ausgeführt werden.  <br/> |
|[ExpandRow](imapitable-expandrow.md) <br/> |Erweitert eine reduzierte Tabellenkategorie und fügt der Tabellenansicht die blattförmigen Zeilen hinzu, die zur Kategorie gehören.  <br/> |
|[CollapseRow](imapitable-collapserow.md) <br/> |Reduziert eine erweiterte Tabellenkategorie und entfernt die zur Kategorie gehörenden Blattzeilen aus der Tabellenansicht.  <br/> |
|[WaitForCompletion](imapitable-waitforcompletion.md) <br/> |Suspends processing until one or more asynchronous operations in progress on the table have completed.  <br/> |
|[GetCollapseState](imapitable-getcollapsestate.md) <br/> |Gibt die Daten zurück, die zum Neuerstellen des aktuellen reduzierten oder erweiterten Zustands einer kategorisierten Tabelle erforderlich sind.  <br/> |
|[SetCollapseState](imapitable-setcollapsestate.md) <br/> |Erstellt den aktuellen erweiterten oder reduzierten Status einer kategorisierten Tabelle mithilfe von Daten neu, die durch einen vorherigen Aufruf der **IMAPITable::GetCollapseState-Methode** gespeichert wurden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

