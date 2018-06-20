---
title: Sortieren von Tabellen nach dem Festlegen der Spalten und Einschränkungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9e75143cb59e782993b9a7f9937432f0b4894d5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795611"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a>Sortieren von Tabellen nach dem Festlegen der Spalten und Einschränkungen

  
  
**Betrifft**: Outlook 
  
Wenn Sie die Ansicht einer sortierten Tabelle einschränken müssen, stellen Sie die folgenden **IMAPITable** Anrufe immer in der folgenden Reihenfolge: 
  
1. [IMAPITable::SetColumns](imapitable-setcolumns.md) zum Definieren der Spalte festlegen. 
    
2. [Methode IMAPITable:: Restrict](imapitable-restrict.md) auf die Einschränkung zugrunde liegen. 
    
3. [SortTable](imapitable-sorttable.md) , um die Sortierung durchzuführen. 
    
Wenn die sortierte Tabelle kategorisiert wird, rufen Sie [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), falls erforderlich, nach dem Aufruf der **SortTable** . Diese Reihenfolge von Anrufen ist wichtig, da die meisten Dienstanbieter eine Tabelle sortiert werden als die letzte Aufgabe aus, um die beste Leistung zu erzielen. Wenn beispielsweise eine Nachricht Speicheranbieter ein Ordner Inhaltstabelle kategorisieren muss, bevor eine Einschränkung auferlegt werden kann, werden diese Kategorisierung während der Verarbeitung der Einschränkung entfernt. Eine zweite Kategorisierung werden erforderlich. 
  

