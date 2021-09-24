---
title: Sortieren von Tabellen nach dem Festlegen von Spalten und Einschränkungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ad28db9be13b18b71b57e0cdae82529f3d4483ea
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549896"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a>Sortieren von Tabellen nach dem Festlegen von Spalten und Einschränkungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie die Ansicht einer sortierten Tabelle einschränken müssen, führen Sie immer die folgenden **IMAPITable-Aufrufe** in der folgenden Reihenfolge aus: 
  
1. [IMAPITable::SetColumns](imapitable-setcolumns.md) zum Definieren des Spaltensatzes. 
    
2. [IMAPITable::Restrict](imapitable-restrict.md) to impose the restriction. 
    
3. [IMAPITable::SortTable](imapitable-sorttable.md) zum Ausführen der Sortierung. 
    
Wenn die sortierte Tabelle kategorisiert ist, rufen Sie nach dem **SortTable-Aufruf** ggf. [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)auf. Diese Reihenfolge von Anrufen ist wichtig, da die meisten Dienstanbieter eine Tabelle als letzte Aufgabe sortieren, um die beste Leistung zu erzielen. Wenn beispielsweise ein Nachrichtenspeicheranbieter ein Ordnerinhaltsverzeichnis kategorisieren muss, bevor eine Einschränkung erzwungen werden kann, wird diese Kategorisierung während der Verarbeitung der Einschränkung entfernt. Eine zweite Kategorisierung ist erforderlich. 
  

