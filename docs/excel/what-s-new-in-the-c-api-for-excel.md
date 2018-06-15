---
title: Was ist neu in der C-API für Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- C-api [excel 2007], was ist neu
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e80b667296af59f4d3f18238cd498830fcdc35a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19790571"
---
# <a name="whats-new-in-the-c-api-for-excel"></a>Was ist neu in der C-API für Excel

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
In Verbindung mit Microsoft Excel 2013 unterstützt der Microsoft Excel 2013 XLL Software Development Kit (SDK) für die folgenden Features.
  
- **Neue Funktionen**
    
    Microsoft Excel 2013 XLL SDK unterstützt Rückrufen aller der neuer Excel-Arbeitsblattfunktionen in Excel 2013. Weitere Informationen zu Excel 2013-Funktionen aufrufen finden Sie unter [in Excel aus der DLL oder XLL aufgerufen](calling-into-excel-from-the-dll-or-xll.md).
    
- **Asynchrone benutzerdefinierte Funktionen**
    
    Excel 2013 unterstützt das Aufrufen von benutzerdefinierten Funktionen (UDF) asynchron die kann die Leistung verbessern, indem mehrere Berechnungen zur selben Zeit ausführen aktivieren. Weitere Informationen zu asynchronen UDFs finden Sie unter [Asynchronous User-Defined-Funktionen](asynchronous-user-defined-functions.md).
    
- **Clusterconnectoren**
    
    Clusterconnectors Aktivieren von UDFs auf High Performance Computecluster ausführen. Weitere Informationen zum Erstellen von clusterconnectoren finden Sie unter [Entwickeln von Excel-Clusterconnectoren](developing-excel-cluster-connectors.md).
    
    > [!NOTE]
    > XLL-add-ins, die Sie auf Computecluster ausführen möchten, müssen nur clustersichere Funktionen aufrufen. Weitere Informationen zu den Funktionen, die Sie verwenden können, finden Sie unter [Excel XLL SDK-API-Funktionsreferenz](excel-xll-sdk-api-function-reference.md) und [Clustersichere Funktionen](cluster-safe-functions.md). 
  
- **64-Bit-Unterstützung**
    
    Sie können jetzt kompilieren und Verknüpfen von 32-Bit- und 64-Bit-XLLs. Weitere Informationen finden Sie unter [Erstellen von XLLs](creating-xlls.md).
    
## <a name="see-also"></a>Siehe auch



[Entwickeln von Excel-XLLs](developing-excel-xlls.md)
  
[Programmieren mit der C-API in Excel](programming-with-the-c-api-in-excel.md)
  
[Multithreading und Arbeitsspeicher Konflikte in Excel](multithreading-and-memory-contention-in-excel.md)


[Erste Schritte mit Excel XLL SDK](getting-started-with-the-excel-xll-sdk.md)

