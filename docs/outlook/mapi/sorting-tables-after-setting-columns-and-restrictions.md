---
title: Sortieren von Tabellen nach dem Festlegen der Spalten und Einschränkungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9f975ed1b9036bce5ed225b2a9020262260f4f57
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572144"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a>Sortieren von Tabellen nach dem Festlegen der Spalten und Einschränkungen

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Wenn Sie die Ansicht einer sortierten Tabelle einschränken müssen, stellen Sie die folgenden **IMAPITable** Anrufe immer in der folgenden Reihenfolge: 
  
1. [IMAPITable::SetColumns](imapitable-setcolumns.md) zum Definieren der Spalte festlegen. 
    
2. [Methode IMAPITable:: Restrict](imapitable-restrict.md) auf die Einschränkung zugrunde liegen. 
    
3. [SortTable](imapitable-sorttable.md) , um die Sortierung durchzuführen. 
    
Wenn die sortierte Tabelle kategorisiert wird, rufen Sie [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), falls erforderlich, nach dem Aufruf der **SortTable** . Diese Reihenfolge von Anrufen ist wichtig, da die meisten Dienstanbieter eine Tabelle sortiert werden als die letzte Aufgabe aus, um die beste Leistung zu erzielen. Wenn beispielsweise eine Nachricht Speicheranbieter ein Ordner Inhaltstabelle kategorisieren muss, bevor eine Einschränkung auferlegt werden kann, werden diese Kategorisierung während der Verarbeitung der Einschränkung entfernt. Eine zweite Kategorisierung werden erforderlich. 
  

