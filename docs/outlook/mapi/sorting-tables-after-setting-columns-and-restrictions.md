---
title: Sortieren von Tabellen nach dem Festlegen von Spalten und Einschränkungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 62220794f325165e67db5397da2795d49959ef60
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409881"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a>Sortieren von Tabellen nach dem Festlegen von Spalten und Einschränkungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie die Ansicht einer sortierten Tabelle einschränken müssen, nehmen Sie immer die folgenden **IMAPITable-Aufrufe** in der folgenden Reihenfolge vor: 
  
1. [IMAPITable::SetColumns,](imapitable-setcolumns.md) um den Spaltensatz zu definieren. 
    
2. [IMAPITable::Restrict,](imapitable-restrict.md) um die Einschränkung zu verhängen. 
    
3. [IMAPITable::SortTable,](imapitable-sorttable.md) um die Sortierung durchzuführen. 
    
Wenn die sortierte Tabelle kategorisiert ist, rufen Sie [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)auf, falls erforderlich, nach dem **SortTable-Aufruf.** Diese Reihenfolge der Anrufe ist wichtig, da die meisten Dienstanbieter eine Tabelle als letzte Aufgabe sortieren, um die beste Leistung zu erzielen. Wenn beispielsweise ein Nachrichtenspeicheranbieter eine Ordnerinhaltstabelle kategorisieren muss, bevor eine Einschränkung auferlegt werden kann, wird diese Kategorisierung während der Verarbeitung der Einschränkung entfernt. Eine zweite Kategorisierung ist erforderlich. 
  

