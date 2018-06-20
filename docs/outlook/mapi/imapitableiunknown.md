---
title: IMAPITable IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable
api_type:
- COM
ms.assetid: f25be2b1-0f94-4a0c-b29d-d2201dc70ab7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0ffaf5909c978059343067c93a2b30f5969327e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792475"
---
# <a name="imapitable--iunknown"></a>IMAPITable: IUnknown

  
  
**Betrifft**: Outlook 
  
Stellt eine schreibgeschützte Ansicht einer Tabelle. **IMAPITable** wird von Clients und -Dienstanbieter verwendet, um die Möglichkeit zu bearbeiten, die eine Tabelle angezeigt wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Table-Objekte  <br/> |
|Implementiert von:  <br/> |Dienstanbieter und MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter-Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPITable  <br/> |
|Zeigertyp:  <br/> |LPMAPITABLE  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetLastError](imapitable-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur mit Informationen über den vorherigen Fehler in der Tabelle zurück.  <br/> |
|[Beraten](imapitable-advise.md) <br/> |Um die Benachrichtigung der Auswirkungen auf die Tabelle angegebenen Ereignisse registriert.  <br/> |
|[Heben Sie diesen Vorgang](imapitable-unadvise.md) <br/> |Bricht ab, das Senden von Benachrichtigungen, die zuvor mit einem Aufruf der Methode **IMAPITable::Advise** eingerichtet.  <br/> |
|[GetStatus](imapitable-getstatus.md) <br/> |Status und Typ der Tabelle zurückgegeben.  <br/> |
|[SetColumns](imapitable-setcolumns.md) <br/> |Definiert die jeweiligen Eigenschaften und die Reihenfolge der Eigenschaften als Spalten in der Tabelle angezeigt werden.  <br/> |
|[QueryColumns](imapitable-querycolumns.md) <br/> |Gibt eine Liste mit Spalten für die Tabelle zurück.  <br/> |
|[GetRowCount](imapitable-getrowcount.md) <br/> |Gibt die Gesamtzahl der Zeilen in der Tabelle zurück.  <br/> |
|[SeekRow](imapitable-seekrow.md) <br/> |Verschiebt den Cursor an eine bestimmte Position in der Tabelle an.  <br/> |
|[SeekRowApprox](imapitable-seekrowapprox.md) <br/> |Verschiebt den Cursor an eine ungefähre Bruch Position in der Tabelle an.  <br/> |
|[QueryPosition](imapitable-queryposition.md) <br/> |Ruft die aktuelle Tabelle Zeilenposition des Cursors, basierend auf einem Bruch Wert.  <br/> |
|[FindRow](imapitable-findrow.md) <br/> |Findet die nächste Zeile in einer Tabelle, die bestimmte Suchkriterien entspricht.  <br/> |
|[Einschränken](imapitable-restrict.md) <br/> |Wendet einen Filter auf eine Tabelle, reduzieren die Zeile festgelegt, um nur die Zeilen, die den angegebenen Kriterien entsprechen.  <br/> |
|[CreateBookmark](imapitable-createbookmark.md) <br/> |Markiert die aktuelle Position der Tabelle.  <br/> |
|[FreeBookmark](imapitable-freebookmark.md) <br/> |Gibt ein Lesezeichen zugeordneten Arbeitsspeicher frei.  <br/> |
|[SortTable](imapitable-sorttable.md) <br/> |Sortiert die Zeilen der Tabelle basierend auf Sortierkriterien.  <br/> |
|[QuerySortOrder](imapitable-querysortorder.md) <br/> |Ruft die aktuelle Sortierreihenfolge für eine Tabelle an.  <br/> |
|[QueryRows](imapitable-queryrows.md) <br/> |Gibt eine oder mehrere Zeilen aus einer Tabelle, beginnend bei der aktuellen Cursorposition zurück.  <br/> |
|[Abbruch](imapitable-abort.md) <br/> |Beendet die asynchrone Vorgänge derzeit in Arbeit für die Tabelle.  <br/> |
|[ExpandRow](imapitable-expandrow.md) <br/> |Erweitert eine reduzierte Tabellenkategorie, der Kategorie zur Tabellenansicht Endknoten Zeilen hinzufügen.  <br/> |
|[CollapseRow](imapitable-collapserow.md) <br/> |Blendet eine Tabellenkategorie für erweiterte, entfernen die Endknoten Zeilen aus der Tabellenansicht für die Kategorie gehören.  <br/> |
|[WaitForCompletion](imapitable-waitforcompletion.md) <br/> |Unterbricht die Verarbeitung, bis eine oder mehrere asynchrone Vorgänge in Bearbeitung in der Tabelle abgeschlossen haben.  <br/> |
|[GetCollapseState](imapitable-getcollapsestate.md) <br/> |Gibt die Daten, die erforderlich sind, um die aktuelle neu erstellen erweitert oder reduziert Zustand einer kategorisierten Tabelle.  <br/> |
|[SetCollapseState](imapitable-setcollapsestate.md) <br/> |Erstellt den aktuellen erweiterten oder reduzierten den Status einer kategorisierten Tabelle mit Daten, die durch einen vorherigen Aufruf der **IMAPITable::GetCollapseState** -Methode gespeichert wurde neu.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

