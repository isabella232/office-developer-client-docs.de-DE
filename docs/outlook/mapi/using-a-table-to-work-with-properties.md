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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439912"
---
# <a name="using-a-table-to-work-with-properties"></a>Verwenden einer Tabelle zum Arbeiten mit Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Viele Eigenschaften sind sowohl für die Objekte verfügbar, die sie unterstützen, als auch als Spalten in Tabellen. Rufen Sie diese Eigenschaften nach Möglichkeit über die Tabelle ab.
  
Rufen [Sie IMAPITable::SetColumns](imapitable-setcolumns.md) auf, um alle Eigenschaften, die Ihr Client benötigt, und [IMAPITable::QueryRows](imapitable-queryrows.md) zum Abrufen aller Zeilen der Tabelle zu verwenden. 
  
Diese beiden Aufrufe sind in der Regel ausreichend, um genügend Informationen zum Anzeigen für einen Benutzer zu erhalten, und sind häufig ausreichend für die erforderliche interne Verarbeitung, wodurch ein Aufruf von **OpenEntry** erfolgt, um das Objekt unnötig zu öffnen. 
  
Es gibt nur zwei Ausnahmen:
  
- Wenn die Eigenschaft über 255 Byte ist. Die ** IMAPITable **-Schnittstelle gibt möglicherweise nicht den gesamten Eigenschaftswert zurück, sondern 255 Byte. Denken Sie jedoch an diesen Tradeoff. Wenn Sie diese Daten dem Benutzer anzeigen, reichen möglicherweise 255 Byte für ein Textfeld wie einen Kommentar aus. 
    
- Wenn Sie eine bestimmte Eigenschaft aus einer einzelnen Zeile in einer Tabelle benötigen. In diesem Fall ist es nicht erforderlich, eine Tabelle mit Eigenschaften zu erstellen, die niemals verwendet werden. Meistens benötigen Sie die gleichen Eigenschaften für alle Zeilen.
    

