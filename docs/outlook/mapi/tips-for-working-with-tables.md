---
title: Tipps zum Arbeiten mit Tabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: adb4d589-7e03-4222-8717-898ef397c6b6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8f310c6331df941d3093b276b6dec47f740412e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439737"
---
# <a name="tips-for-working-with-tables"></a>Tipps zum Arbeiten mit Tabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Arbeiten mit einer MAPI-Tabelle ist ein wenig wie die Arbeit mit einer relationalen Datenbanktabelle. Ein Benutzer kann die Anzahl der Zeilen und Spalten in der Ansicht einschränken und seine Reihenfolge angeben. Zeilen können gleichzeitig oder in Gruppen abgerufen werden. Ein Cursor, der die aktuelle Position nachverfolgt, kann an eine bestimmte Stelle in der Tabelle verschoben werden. 
  
Zum Arbeiten mit Tabellen verwenden Clients die schreibgeschützte Schnittstelle [IMAPITable : IUnknown](imapitableiunknown.md), während Dienstanbieter je nachdem, ob sie die Daten besitzen, auf der die Tabelle basiert, **entweder IMAPITable** oder [ITableData : IUnknown](itabledataiunknown.md)verwenden können. Die in diesen Schnittstellen definierten Vorgänge können als Vorgänge kategorisiert werden, die alle Benutzer von Tabellen entweder tun oder aufrufen können, und Vorgänge, die nicht so häufig verwendet werden, weil sie fortgeschrittener sind. Einige der erweiterten Vorgänge sind komplexer zu implementieren. Andere sind nicht komplexer, aber für eine kleine Minderheit von MAPI-Komponenten von Interesse. 
  
Die gängigen Vorgänge sind:
  
- Spaltenvorgänge, die sich auf einzelne Spalten auswirken. Dazu gehören das Angeben der Eigenschaften, die in den Spaltensatz eingeschlossen werden sollen, und die Reihenfolge, in der sie eingeschlossen werden sollen.
    
- Zeilenvorgänge, die sich auf einzelne Zeilen auswirken. Dazu gehören der Datenabruf und die Wartungsvorgänge: Hinzufügen, Löschen und Ändern einer einzelnen Zeile oder Zeile.
    
- Globale Vorgänge, die sich auf die gesamte Tabelle auswirken. Dazu gehören Ereignisbenachrichtigungen, Suchen und Sortieren.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

