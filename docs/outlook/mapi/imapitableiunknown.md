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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d6a13799da4ef9315f9c23317fa18853d71c72f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420115"
---
# <a name="imapitable--iunknown"></a>IMAPITable : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bietet eine schreibgeschützte Ansicht einer Tabelle. **IMAPITable** wird von Clients und Dienstanbietern verwendet, um die Art und Weise zu ändern, wie eine Tabelle angezeigt wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Tabellenobjekte  <br/> |
|Implementiert von:  <br/> |Dienstanbieter und MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen, Dienstanbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPITable  <br/> |
|Zeigertyp:  <br/> |LPMAPITABLE  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetLastError](imapitable-getlasterror.md) <br/> |Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler in der Tabelle enthält.  <br/> |
|[Raten](imapitable-advise.md) <br/> |Registriert, um Benachrichtigungen über angegebene Ereignisse zu erhalten, die sich auf die Tabelle ausdingen.  <br/> |
|[Unadvise](imapitable-unadvise.md) <br/> |Bricht das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der **IMAPITable::Advise-Methode eingerichtet** wurden.  <br/> |
|[GetStatus](imapitable-getstatus.md) <br/> |Gibt den Status und Typ der Tabelle zurück.  <br/> |
|[SetColumns](imapitable-setcolumns.md) <br/> |Definiert die bestimmten Eigenschaften und die Reihenfolge der Eigenschaften, die in der Tabelle als Spalten angezeigt werden sollen.  <br/> |
|[QueryColumns](imapitable-querycolumns.md) <br/> |Gibt eine Liste der Spalten für die Tabelle zurück.  <br/> |
|[GetRowCount](imapitable-getrowcount.md) <br/> |Gibt die Gesamtanzahl der Zeilen in der Tabelle zurück.  <br/> |
|[SeekRow](imapitable-seekrow.md) <br/> |Verschiebt den Cursor an eine bestimmte Position in der Tabelle.  <br/> |
|[SeekRowApprox](imapitable-seekrowapprox.md) <br/> |Verschiebt den Cursor an eine ungefähre Bruchposition in der Tabelle.  <br/> |
|[QueryPosition](imapitable-queryposition.md) <br/> |Ruft die aktuelle Tabellenzeile des Cursors basierend auf einem Bruchwert ab.  <br/> |
|[FindRow](imapitable-findrow.md) <br/> |Sucht die nächste Zeile in einer Tabelle, die bestimmten Suchkriterien entspricht.  <br/> |
|[Restrict](imapitable-restrict.md) <br/> |Wendet einen Filter auf eine Tabelle an, wodurch der Zeilensatz auf nur die Zeilen reduziert wird, die den angegebenen Kriterien entsprechen.  <br/> |
|[CreateBookmark](imapitable-createbookmark.md) <br/> |Markiert die aktuelle Position der Tabelle.  <br/> |
|[FreeBookmark](imapitable-freebookmark.md) <br/> |Gibt den Speicher frei, der einer Textmarke zugeordnet ist.  <br/> |
|[SortTable](imapitable-sorttable.md) <br/> |Ordnet die Zeilen der Tabelle basierend auf Sortierkriterien an.  <br/> |
|[QuerySortOrder](imapitable-querysortorder.md) <br/> |Ruft die aktuelle Sortierreihenfolge für eine Tabelle ab.  <br/> |
|[QueryRows](imapitable-queryrows.md) <br/> |Gibt eine oder mehrere Zeilen aus einer Tabelle zurück, beginnend an der aktuellen Cursorposition.  <br/> |
|[Abbruch](imapitable-abort.md) <br/> |Beendet alle asynchronen Vorgänge, die derzeit für die Tabelle ausgeführt werden.  <br/> |
|[ExpandRow](imapitable-expandrow.md) <br/> |Erweitert eine reduzierte Tabellenkategorie und fügt der Tabellenansicht die Blattzeilen hinzu, die zu der Kategorie gehören.  <br/> |
|[CollapseRow](imapitable-collapserow.md) <br/> |Reduziert eine erweiterte Tabellenkategorie und entfernt die Blattzeilen, die zur Kategorie gehören, aus der Tabellenansicht.  <br/> |
|[WaitForCompletion](imapitable-waitforcompletion.md) <br/> |Die Verarbeitung wird angehalten, bis ein oder mehrere asynchrone Vorgänge in der Tabelle abgeschlossen sind.  <br/> |
|[GetCollapseState](imapitable-getcollapsestate.md) <br/> |Gibt die Daten zurück, die zum Neuerstellen des aktuellen reduzierten oder erweiterten Zustands einer kategorisierten Tabelle erforderlich sind.  <br/> |
|[SetCollapseState](imapitable-setcollapsestate.md) <br/> |Erstellt den aktuellen erweiterten oder reduzierten Zustand einer kategorisierten Tabelle mithilfe von Daten, die durch einen vorherigen Aufruf der **IMAPITable::GetCollapseState-Methode gespeichert** wurden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

