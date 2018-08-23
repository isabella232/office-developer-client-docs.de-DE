---
title: Verwenden einer Tabelle zum Arbeiten mit Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9f02da9eb1920f55acf65dfb6a503e42d4c3daf2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585423"
---
# <a name="using-a-table-to-work-with-properties"></a>Verwenden einer Tabelle zum Arbeiten mit Eigenschaften

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Viele Eigenschaften sind sowohl auf die Objekte, die sie unterstützen und als Spalten in Tabellen zur Verfügung. Wenn möglich, rufen Sie diese Eigenschaften über die Tabelle ab.
  
Rufen Sie [IMAPITable::SetColumns](imapitable-setcolumns.md) alle Eigenschaften enthalten, die der Client muss und [IMAPITable::QueryRows](imapitable-queryrows.md) alle Zeilen der Tabelle abrufen. 
  
Diese beiden Aufrufe in der Regel ausreichend zum Abrufen von genügend Informationen, die ein Benutzer angezeigt werden und sind häufig ausreichend für alle erforderlichen interner Aufrufen **OpenEntry** zum Öffnen des Objekts nicht erforderlich. 
  
Es gibt nur zwei Ausnahmen:
  
- Wenn die Eigenschaft mehr als 255 Byte ist. Die ** IMAPITable ** Schnittstelle möglicherweise nicht zurück, die den gesamte Eigenschaftswert stattdessen auf 255 Byte abgeschnitten. Überlegen Sie jedoch dieser Kompromiss. Wenn Sie diese Daten an den Benutzer anzeigen, möglicherweise 255 Byte genug für eine textbezogene dar, wie ein Kommentar. 
    
- Wenn Sie eine bestimmte Eigenschaft aus einer einzelnen Zeile in einer Tabelle benötigen. In diesem Fall ist es nicht erforderlich, eine Tabelle mit den Eigenschaften zu erstellen, die noch nie verwendet werden. In den meisten Fällen benötigen die gleichen Eigenschaften Sie für alle Zeilen.
    

