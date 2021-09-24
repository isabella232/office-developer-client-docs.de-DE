---
title: Tabellenpositionierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a0cbbc93-8074-4e86-b660-ee7bab910587
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fe261b96e18d320d3caafe6aa0afcd85abb721d9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549860"
---
# <a name="table-positioning"></a>Tabellenpositionierung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die aktuelle Position innerhalb einer Tabelle wird immer durch einen Cursor angegeben. Es gibt einen Cursor für jede Ansicht einer Tabelle. Der Wert wird vom Implementierer der Tabelle festgelegt. Wenn ein Client oder Dienstanbieter, der die Tabelle verwendet, aufruft, um die Position der Tabelle zu ändern, wird der Wert des Cursors zurückgesetzt. Die Position einer Tabelle kann wie folgt geändert werden:
  
- Textmarke.
    
- Ein Bruchwert.
    
- Einen Filter.
    

