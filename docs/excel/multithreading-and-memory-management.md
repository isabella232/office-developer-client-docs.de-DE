---
title: Multithreading und Speicherverwaltung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9e233d6db482c4671ee25cfb046e730a3d0e2376
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576716"
---
# <a name="multithreading-and-memory-management"></a>Multithreading und Speicherverwaltung

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Die ordnungsgemäße Handhabung des Arbeitsspeichers ist entscheidend für die Erstellung zuverlässiger XLL-Add-Ins für Microsoft Excel. Wenn keine geeigneten Speicherpuffer zugeordnet und freigegeben werden, wenn sie nicht mehr benötigt werden, wird die Leistung verringert, Ressourcenkonflikte erstellt und Excel destabilisiert.
  
Ab Microsoft Office Excel 2007 können Sie Excel so konfigurieren, dass bei der Neuberechnung bis zu 1.024 gleichzeitige Threads verwendet werden. In einigen Fällen, insbesondere wenn mehrere Prozessoren verfügbar sind oder benutzerdefinierte Funktionen auf Clusterservern ausgeführt werden, kann Multithreading die Leistung verbessern.
  
In den folgenden Themen wird beschrieben, wie Speicher und Threads in XLLs verwaltet werden:
  
- [Speicherverwaltung in Excel](memory-management-in-excel.md)
    
- [Multithreading und Speicherkonflikte in Excel](multithreading-and-memory-contention-in-excel.md)
    
- [Multithread-Neuberechnung in Excel](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a>Siehe auch



[Entwickeln von XLLs für Excel](developing-excel-xlls.md)

