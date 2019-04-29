---
title: Tipps für das Arbeiten mit Tabellen
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
# <a name="tips-for-working-with-tables"></a>Tipps für das Arbeiten mit Tabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Arbeiten mit einer MAPI-Tabelle ähnelt dem Arbeiten mit einer relationalen Datenbanktabelle. Ein Benutzer kann die Anzahl der Zeilen und Spalten in der Ansicht begrenzen und deren Reihenfolge angeben. Zeilen können einzeln oder in Gruppen abgerufen werden. Ein Cursor, der die aktuelle Position verfolgt, kann an eine bestimmte Stelle in der Tabelle verschoben werden. 
  
Zum Arbeiten mit Tabellen verwenden Clients die schreibgeschützte Schnittstelle [IMAPITable: IUnknown](imapitableiunknown.md), wohingegen Dienstanbieter, je nachdem, ob Sie die Daten besitzen, auf denen die Tabelle basiert, entweder **IMAPITable** oder [ITableData: IUnknown](itabledataiunknown.md)verwenden können. Die in diesen Schnittstellen definierten Vorgänge können als Vorgänge kategorisiert werden, die von allen Benutzern von Tabellen ausgeführt oder aufgerufen werden können, und Vorgänge, die nicht so häufig verwendet werden, da Sie weiter fortgeschritten sind. Einige der erweiterten Vorgänge sind komplexer zu implementieren; andere sind nicht komplexer, sondern interessieren sich für eine kleine Gruppe von MAPI-Komponenten. 
  
Die gängigeren Vorgänge sind:
  
- Spalten Vorgänge, die sich auf einzelne Spalten auswirken. Dazu gehören das Angeben der Eigenschaften, die in den Spaltensatz eingeschlossen werden sollen, und die Reihenfolge, in der Sie eingeschlossen werden sollen.
    
- Zeilenvorgänge, die sich auf einzelne Zeilen auswirken. Hierzu gehört der Datenabruf und die Wartungsvorgänge: Hinzufügen, löschen und Ändern einer einzelnen Zeile oder Zeilen.
    
- Globale Vorgänge, die sich auf die gesamte Tabelle auswirken. Dazu gehört die Ereignisbenachrichtigung, das Suchen und sortieren.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

