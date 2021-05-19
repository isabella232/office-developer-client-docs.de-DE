---
title: Multithreading und Speicherverwaltung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f387d5ddb184c681ab5e005a6eb24058f6f52f9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414466"
---
# <a name="multithreading-and-memory-management"></a>Multithreading und Speicherverwaltung

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Die ordnungsgemäße Behandlung des Arbeitsspeichers ist für die Erstellung zuverlässiger XLL-Add-Ins für die Microsoft Excel. Wenn keine geeigneten Speicherpuffer zugewiesen und frei werden, wenn sie nicht mehr benötigt werden, wird die Leistung reduziert, Ressourcenstritte erstellt und Excel.
  
Ab Microsoft Office Excel 2007 können Sie Excel so konfigurieren, dass bei der Neuberechnung bis zu 1.024 gleichzeitige Threads verwendet werden. In einigen Fällen, insbesondere wenn mehrere Prozessoren verfügbar sind oder benutzerdefinierte Funktionen auf Clusterservern ausgeführt werden, kann Multithreading die Leistung verbessern.
  
In den folgenden Themen wird das Verwalten von Arbeitsspeicher und Threads in XLLs beschrieben:
  
- [Speicherverwaltung in Excel](memory-management-in-excel.md)
    
- [Multithreading und Speicherkonflikte in Excel](multithreading-and-memory-contention-in-excel.md)
    
- [Multithread-Neuberechnung in Excel](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a>Siehe auch



[Entwickeln von XLLs für Excel](developing-excel-xlls.md)

