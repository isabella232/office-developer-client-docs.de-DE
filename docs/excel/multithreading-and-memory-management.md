---
title: Multithreading und Speicherverwaltung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 4f5495648c9012b0e028358037090f7e10ef5219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790554"
---
# <a name="multithreading-and-memory-management"></a>Multithreading und Speicherverwaltung

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Korrekte Handhabung von Arbeitsspeicher ist entscheidend für zuverlässige XLL-add-ins für Microsoft Excel erstellen. Fehler beim Zuweisen der entsprechenden Speicherpuffern und diese frei, wenn sie nicht mehr benötigt werden reduziert die Leistung, Ressourcenkonflikte erstellt und Excel Dienstausfall.
  
Beginnen mit Microsoft Office Excel 2007, können Sie Excel, um bis zu 1.024 gleichzeitigen Threads verwenden, wenn Neuberechnen konfigurieren. In einigen Fällen können insbesondere dann, wenn mehrere Prozessoren verfügbar sind oder mit benutzerdefinierten Funktionen unter Servercluster multithreading Leistung verbessern.
  
In den folgenden Themen wird beschrieben, wie Arbeitsspeicher und Threads im XLLs verwalten:
  
- [Speicherverwaltung in Excel](memory-management-in-excel.md)
    
- [Multithreading und Arbeitsspeicher Konflikte in Excel](multithreading-and-memory-contention-in-excel.md)
    
- [Multithread-Neuberechnung in Excel](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a>Siehe auch



[Entwickeln von Excel-XLLs](developing-excel-xlls.md)

