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
ms.openlocfilehash: d6a13799da4ef9315f9c23317fa18853d71c72f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328798"
---
# <a name="imapitable--iunknown"></a>IMAPITable : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt eine schreibgeschützte Ansicht einer Tabelle bereit. **IMAPITable** wird von Clients und Dienstanbietern verwendet, um die Art und Weise zu manipulieren, in der eine Tabelle angezeigt wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Verf�gbar gemacht von:  <br/> |Tabellenobjekte  <br/> |
|Implementiert von:  <br/> |Dienstanbieter und MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen, Dienstanbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPITable  <br/> |
|Zeigertyp:  <br/> |LPMAPITABLE  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Getlasterroraufzurufen](imapitable-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur mit Informationen über den vorherigen Fehler in der Tabelle zurück.  <br/> |
|[Beraten](imapitable-advise.md) <br/> |Registriert die Benachrichtigung über angegebene Ereignisse, die sich auf die Tabelle auswirken.  <br/> |
|[Unadvise](imapitable-unadvise.md) <br/> |Bricht das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der **IMAPITable:: Advise** -Methode eingerichtet wurden.  <br/> |
|[GetStatus](imapitable-getstatus.md) <br/> |Gibt den Status und den Typ der Tabelle zurück.  <br/> |
|[SetColumns](imapitable-setcolumns.md) <br/> |Definiert die Eigenschaften und die Reihenfolge der Eigenschaften, die als Spalten in der Tabelle angezeigt werden sollen.  <br/> |
|[QueryColumns](imapitable-querycolumns.md) <br/> |Gibt eine Liste der Spalten für die Tabelle zurück.  <br/> |
|[GetRowCount](imapitable-getrowcount.md) <br/> |Gibt die Gesamtanzahl der Zeilen in der Tabelle zurück.  <br/> |
|[SeekRow](imapitable-seekrow.md) <br/> |Verschiebt den Cursor an eine bestimmte Position in der Tabelle.  <br/> |
|[SeekRowApprox](imapitable-seekrowapprox.md) <br/> |Verschiebt den Cursor an eine ungefähre Bruchposition in der Tabelle.  <br/> |
|[QueryPosition](imapitable-queryposition.md) <br/> |Ruft die aktuelle Tabellenzeilen Position des Cursors basierend auf einem Dezimalwert ab.  <br/> |
|[FindRow](imapitable-findrow.md) <br/> |Sucht die nächste Zeile in einer Tabelle, die bestimmten Suchkriterien entspricht.  <br/> |
|[Restrict](imapitable-restrict.md) <br/> |Wendet einen Filter auf eine Tabelle an, wobei der Zeilensatz nur auf die Zeilen reduziert wird, die den angegebenen Kriterien entsprechen.  <br/> |
|[CreateBookmark](imapitable-createbookmark.md) <br/> |Markiert die aktuelle Position der Tabelle.  <br/> |
|[FreeBookmark](imapitable-freebookmark.md) <br/> |Gibt den mit einer Textmarke verknüpften Arbeitsspeicher frei.  <br/> |
|[SortTable](imapitable-sorttable.md) <br/> |Sortiert die Zeilen der Tabelle basierend auf Sortierkriterien.  <br/> |
|[QuerySortOrder](imapitable-querysortorder.md) <br/> |Ruft die aktuelle Sortierreihenfolge für eine Tabelle ab.  <br/> |
|[QueryRows](imapitable-queryrows.md) <br/> |Gibt eine oder mehrere Zeilen aus einer Tabelle zurück, die an der aktuellen Cursorposition beginnen.  <br/> |
|[Abbruch](imapitable-abort.md) <br/> |Beendet alle asynchronen Vorgänge, die derzeit für die Tabelle ausgeführt werden.  <br/> |
|[ExpandRow](imapitable-expandrow.md) <br/> |Erweitert eine reduzierte Tabellen Kategorie, indem Sie der Tabellenansicht die Blattzeilen hinzufügt, die der Kategorie angehören.  <br/> |
|[CollapseRow](imapitable-collapserow.md) <br/> |Reduziert eine erweiterte Tabellen Kategorie und entfernt die Blattzeilen der Kategorie aus der Tabellenansicht.  <br/> |
|[WaitForCompletion](imapitable-waitforcompletion.md) <br/> |Hält die Verarbeitung an, bis mindestens ein asynchroner Vorgang abgeschlossen ist, der in der Tabelle ausgeführt wurde.  <br/> |
|[GetCollapseState](imapitable-getcollapsestate.md) <br/> |Gibt die Daten zurück, die zum Neuaufbau des aktuellen reduzierten oder erweiterten Status einer kategorisierten Tabelle erforderlich sind.  <br/> |
|[SetCollapseState](imapitable-setcollapsestate.md) <br/> |Erstellt den aktuellen erweiterten oder reduzierten Status einer kategorisierten Tabelle mithilfe von Daten, die durch einen vorherigen Aufruf der **IMAPITable:: GetCollapseState** -Methode gespeichert wurden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

