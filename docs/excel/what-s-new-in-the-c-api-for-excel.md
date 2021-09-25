---
title: Neuigkeiten in der C-API für Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c api [excel 2007], what's new
ms.localizationpriority: medium
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 99a4bc3c1a88dd4b812ced2c7578f61a7d1274a8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621374"
---
# <a name="whats-new-in-the-c-api-for-excel"></a>Neuigkeiten in der C-API für Excel

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
In Verbindung mit Microsoft Excel 2013 bietet das Microsoft Excel 2013 XLL Software Development Kit (SDK) Unterstützung für die folgenden Features.
  
- **Neue Funktionen**
    
    Das Microsoft Excel 2013 XLL SDK unterstützt das Aufrufen aller neuen Arbeitsblattfunktionen in Excel 2013. Weitere Informationen zum Aufrufen Excel 2013-Funktionen finden Sie unter [Aufrufen von Excel über die DLL oder XLL.](calling-into-excel-from-the-dll-or-xll.md)
    
- **Asynchrone benutzerdefinierte Funktionen**
    
    Excel 2013 unterstützt das asynchrone Aufrufen von benutzerdefinierten Funktionen (User-Defined Functions, UDF), wodurch die Leistung verbessert werden kann, indem mehrere Berechnungen gleichzeitig ausgeführt werden können. Weitere Informationen zu asynchronen UDFs finden Sie unter ["Asynchrone User-Defined Funktionen".](asynchronous-user-defined-functions.md)
    
- **Clusterconnectors**
    
    Clusterconnectors ermöglichen UDFs die Ausführung auf Hochleistungs-Computeclustern. Weitere Informationen zum Erstellen von Clusterconnectors finden Sie unter [Developing Excel Cluster Connectors](developing-excel-cluster-connectors.md).
    
    > [!NOTE]
    > XLL-Add-Ins, die Sie auf Computeclustern ausführen möchten, müssen nur clustersichere Funktionen aufrufen. Weitere Informationen zu den Funktionen, die Sie verwenden können, finden Sie unter [Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md) and Cluster Tresor [Functions.](cluster-safe-functions.md) 
  
- **64-Bit-Unterstützung**
    
    Sie können jetzt sowohl 32-Bit- als auch 64-Bit-XLLs kompilieren und verknüpfen. Weitere Informationen finden Sie unter [Erstellen von XLLs](creating-xlls.md).
    
## <a name="see-also"></a>Siehe auch



[Entwickeln von XLLs für Excel](developing-excel-xlls.md)
  
[Programmieren mit der C-API in Excel](programming-with-the-c-api-in-excel.md)
  
[Multithreading und Speicherkonflikte in Excel](multithreading-and-memory-contention-in-excel.md)


[Erste Schritte mit dem Excel XLL SDK](getting-started-with-the-excel-xll-sdk.md)

