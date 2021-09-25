---
title: Tipps zum Arbeiten mit Tabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: adb4d589-7e03-4222-8717-898ef397c6b6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cc66fd24da4e98c428453b82a03ed65844af5aaa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609341"
---
# <a name="tips-for-working-with-tables"></a>Tipps zum Arbeiten mit Tabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Arbeiten mit einer MAPI-Tabelle ähnelt dem Arbeiten mit einer relationalen Datenbanktabelle. Ein Benutzer kann die Anzahl der Zeilen und Spalten in der Ansicht einschränken und seine Reihenfolge angeben. Zeilen können einzeln oder in Gruppen abgerufen werden. Ein Cursor, der die aktuelle Position verfolgt, kann an eine bestimmte Stelle in der Tabelle verschoben werden. 
  
Zum Arbeiten mit Tabellen verwenden Clients die schreibgeschützte Schnittstelle [IMAPITable : IUnknown,](imapitableiunknown.md)während Dienstanbieter, je nachdem, ob sie die Daten besitzen, auf denen die Tabelle basiert, **ENTWEDER IMAPITable** oder [ITableData verwenden können: IUnknown](itabledataiunknown.md). Die in diesen Schnittstellen definierten Vorgänge können als Vorgänge kategorisiert werden, die alle Benutzer von Tabellen ausführen oder aufrufen können, und als Vorgänge, die nicht so häufig verwendet werden, da sie fortgeschrittener sind. Einige der erweiterten Vorgänge sind komplexer zu implementieren. andere sind nicht komplexer, sind aber für einen kleinen Teil der MAPI-Komponenten von Interesse. 
  
Die gängigeren Vorgänge sind:
  
- Spaltenvorgänge, die sich auf einzelne Spalten auswirken. Dazu gehören das Angeben der Eigenschaften, die in den Spaltensatz aufgenommen werden sollen, und die Reihenfolge, in der sie enthalten sein sollen.
    
- Zeilenvorgänge, die sich auf einzelne Zeilen auswirken. Dazu gehören der Datenabruf und die Wartungsvorgänge: Hinzufügen, Löschen und Ändern einer einzelnen Zeile oder Zeilen.
    
- Globale Vorgänge, die sich auf die gesamte Tabelle auswirken. Dazu gehören Ereignisbenachrichtigung, Suche und Sortierung.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

