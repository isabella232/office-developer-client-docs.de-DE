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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344485"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a>Sortieren von Tabellen nach dem Festlegen von Spalten und Einschränkungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie die Ansicht einer sortierten Tabelle einschränken müssen, führen Sie die folgenden **IMAPITable** -Aufrufe in der folgenden Reihenfolge aus: 
  
1. [IMAPITable::](imapitable-setcolumns.md) SetColumns zum Definieren des Spaltensatzes. 
    
2. [IMAPITable:: einschränken](imapitable-restrict.md) , um die Einschränkung aufzuerlegen. 
    
3. [IMAPITable:: sortable](imapitable-sorttable.md) , um die Sortierung durchzuführen. 
    
Wenn die sortierte Tabelle kategorisiert wird, führen Sie einen Aufruf von [IMAPITable:: SetCollapseState](imapitable-setcollapsestate.md), falls erforderlich, nach dem **sortable** -Aufruf aus. Diese Reihenfolge von anrufen ist wichtig, da die meisten Dienstanbieter eine Tabelle als letzte Aufgabe sortieren, um eine optimale Leistung zu erzielen. Wenn beispielsweise ein Nachrichtenspeicher Anbieter eine Ordnerinhaltstabelle kategorisieren muss, bevor eine Einschränkung auferlegt werden kann, wird diese Kategorisierung während der Verarbeitung der Einschränkung entfernt. Eine zweite Kategorisierung ist erforderlich. 
  

