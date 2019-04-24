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
ms.openlocfilehash: 59196f136c422be912ac2460cbbd25d8bc2e3330
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329701"
---
# <a name="using-a-table-to-work-with-properties"></a>Verwenden einer Tabelle zum Arbeiten mit Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Viele Eigenschaften sind sowohl von den Objekten, die Sie unterstützen, als auch von Spalten in Tabellen verfügbar. Rufen Sie diese Eigenschaften nach Möglichkeit über die Tabelle ab.
  
Rufen Sie [IMAPITable::](imapitable-setcolumns.md) SetColumns auf, um alle Eigenschaften einzuschließen, die der Client benötigt, und [IMAPITable:: QueryRows](imapitable-queryrows.md) , um alle Zeilen der Tabelle abzurufen. 
  
Diese beiden Aufrufe sind in der Regel ausreichend, um genügend Informationen abzurufen, die für einen Benutzer angezeigt werden sollen, und Sie sind häufig für die erforderliche interne Verarbeitung **** ausreichend, wodurch ein Aufruf von OpenEntry zum Öffnen des Objekts erforderlich ist. 
  
Es gibt nur zwei Ausnahmen:
  
- Wenn die Eigenschaft über 255 Byte ist. Die * * IMAPITable * *-Schnittstelle gibt möglicherweise nicht den gesamten Eigenschaftswert zurück und schneidet Sie stattdessen mit 255 Byte ab. Denken Sie jedoch an diesen Kompromiss. Wenn Sie diese Daten dem Benutzer anzeigen, können 255 Byte für ein Textfeld wie einen Kommentar ausreichen. 
    
- Wenn Sie eine bestimmte Eigenschaft aus einer einzelnen Zeile in einer Tabelle benötigen. In diesem Fall ist es nicht erforderlich, eine Tabelle mit Eigenschaften zu erstellen, die nie verwendet werden. In den meisten Fällen benötigen Sie die gleichen Eigenschaften für alle Zeilen.
    

