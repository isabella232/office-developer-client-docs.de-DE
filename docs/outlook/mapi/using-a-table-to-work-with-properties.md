---
title: Verwenden einer Tabelle zum Arbeiten mit Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e4e7ecda40f3f3fcb05700ba3e8b79ab21cbe35b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795812"
---
# <a name="using-a-table-to-work-with-properties"></a>Verwenden einer Tabelle zum Arbeiten mit Eigenschaften

  
  
**Betrifft**: Outlook 
  
Viele Eigenschaften sind sowohl auf die Objekte, die sie unterstützen und als Spalten in Tabellen zur Verfügung. Wenn möglich, rufen Sie diese Eigenschaften über die Tabelle ab.
  
Rufen Sie [IMAPITable::SetColumns](imapitable-setcolumns.md) alle Eigenschaften enthalten, die der Client muss und [IMAPITable::QueryRows](imapitable-queryrows.md) alle Zeilen der Tabelle abrufen. 
  
Diese beiden Aufrufe in der Regel ausreichend zum Abrufen von genügend Informationen, die ein Benutzer angezeigt werden und sind häufig ausreichend für alle erforderlichen interner Aufrufen **OpenEntry** zum Öffnen des Objekts nicht erforderlich. 
  
Es gibt nur zwei Ausnahmen:
  
- Wenn die Eigenschaft mehr als 255 Byte ist. Die ** IMAPITable ** Schnittstelle möglicherweise nicht zurück, die den gesamte Eigenschaftswert stattdessen auf 255 Byte abgeschnitten. Überlegen Sie jedoch dieser Kompromiss. Wenn Sie diese Daten an den Benutzer anzeigen, möglicherweise 255 Byte genug für eine textbezogene dar, wie ein Kommentar. 
    
- Wenn Sie eine bestimmte Eigenschaft aus einer einzelnen Zeile in einer Tabelle benötigen. In diesem Fall ist es nicht erforderlich, eine Tabelle mit den Eigenschaften zu erstellen, die noch nie verwendet werden. In den meisten Fällen benötigen die gleichen Eigenschaften Sie für alle Zeilen.
    

