---
title: Verwenden einer Tabelle zum Arbeiten mit Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: abef70e2d5e9fc2eef1ae07f33552c84ecbe9e23
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609208"
---
# <a name="using-a-table-to-work-with-properties"></a>Verwenden einer Tabelle zum Arbeiten mit Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Viele Eigenschaften stehen sowohl von den Objekten, die sie unterstützen, als auch als Spalten in Tabellen zur Verfügung. Rufen Sie diese Eigenschaften nach Möglichkeit über die Tabelle ab.
  
Rufen Sie [IMAPITable::SetColumns](imapitable-setcolumns.md) auf, um alle Eigenschaften einzuschließen, die ihr Client benötigt, und [IMAPITable::QueryRows,](imapitable-queryrows.md) um alle Zeilen der Tabelle abzurufen. 
  
Diese beiden Aufrufe sind in der Regel ausreichend, um genügend Informationen abzurufen, um einem Benutzer angezeigt zu werden, und sind häufig für alle erforderlichen internen Verarbeitungen ausreichend, sodass **openEntry** aufgerufen wird, um das Objekt nicht zu öffnen. 
  
Es gibt nur zwei Ausnahmen:
  
- Wenn die Eigenschaft mehr als 255 Bytes beträgt. Die ** IMAPITable ** -Schnittstelle gibt möglicherweise nicht den gesamten Eigenschaftswert zurück, sondern abgeschnitten bei 255 Bytes. Denken Sie jedoch an diesen Kompromiss. Wenn Sie diese Daten für den Benutzer anzeigen, sind möglicherweise 255 Bytes für ein Textfeld wie einen Kommentar ausreichend. 
    
- Wenn Sie eine bestimmte Eigenschaft aus einer einzelnen Zeile in einer Tabelle benötigen. In diesem Fall ist es nicht erforderlich, eine Tabelle mit Eigenschaften zu erstellen, die nie verwendet werden. In den meisten Jahren benötigen Sie dieselben Eigenschaften für alle Zeilen.
    

