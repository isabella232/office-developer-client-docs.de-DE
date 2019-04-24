---
title: Multithreading und Speicherverwaltung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: f387d5ddb184c681ab5e005a6eb24058f6f52f9a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310388"
---
# <a name="multithreading-and-memory-management"></a>Multithreading und Speicherverwaltung

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Die OrdnungsGemäße Handhabung des Arbeitsspeichers ist unerlässlich, um zuverlässige XLL-Add-Ins für Microsoft Excel zu erstellen. Wenn Sie keine geeigneten Arbeitsspeicherpuffer zuweisen und freigeben, wenn Sie nicht mehr benötigt werden, wird die Leistung reduziert, Ressourcenkonflikte erstellt und Excel destabilisiert.
  
Beginnend mit Microsoft Office Excel 2007 können Sie Excel so konfigurieren, dass bis zu 1.024 gleichzeitige Threads bei der Neuberechnung verwendet werden. In einigen Fällen kann das Multithreading die Leistung verbessern, insbesondere, wenn mehrere Prozessoren verfügbar sind oder benutzerdefinierte Funktionen auf gruppierten Servern ausgeführt werden.
  
In den folgenden Themen wird beschrieben, wie Sie Arbeitsspeicher und Threads in XLLs verwalten:
  
- [Speicherverwaltung in Excel](memory-management-in-excel.md)
    
- [Multithreading und Speicherkonflikte in Excel](multithreading-and-memory-contention-in-excel.md)
    
- [Multithread-Neuberechnung in Excel](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a>Siehe auch



[Entwickeln von XLLs für Excel](developing-excel-xlls.md)

