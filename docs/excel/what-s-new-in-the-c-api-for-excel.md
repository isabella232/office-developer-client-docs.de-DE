---
title: Neues in der C-API für Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c api [excel 2007], was neu ist
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 64e3933ec25f0771db5bd36bbf57f3f259cdc8a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439688"
---
# <a name="whats-new-in-the-c-api-for-excel"></a>Neues in der C-API für Excel

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
In Verbindung mit Microsoft Excel 2013 bietet das Microsoft Excel 2013 XLL Software Development Kit (SDK) Unterstützung für die folgenden Features.
  
- **Neue Funktionen**
    
    Das Microsoft Excel 2013 XLL SDK unterstützt das Aufrufen aller neuen Arbeitsblattfunktionen in Excel 2013. Weitere Informationen zum Aufrufen Excel 2013-Funktionen finden Sie unter [Calling into Excel from the DLL or XLL](calling-into-excel-from-the-dll-or-xll.md).
    
- **Asynchrone benutzerdefinierte Funktionen**
    
    Excel 2013 unterstützt das asynchrone Aufrufen von benutzerdefinierten Funktionen (USERF), wodurch die Leistung verbessert werden kann, indem mehrere Berechnungen gleichzeitig ausgeführt werden können. Weitere Informationen zu asynchronen UDFs finden Sie unter [Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md).
    
- **Clusterconnectors**
    
    Mit Clusterconnectors können UDFs auf Hochleistungs-Computeclustern ausgeführt werden. Weitere Informationen zum Erstellen von Clusterconnectors finden Sie unter [Developing Excel Cluster Connectors](developing-excel-cluster-connectors.md).
    
    > [!NOTE]
    > XLL-Add-Ins, die Sie auf Computeclustern ausführen möchten, müssen nur clustersichere Funktionen aufrufen. Weitere Informationen zu den Funktionen, die Sie verwenden können, finden Sie [unter Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md) und Cluster Safe [Functions](cluster-safe-functions.md). 
  
- **64-Bit-Unterstützung**
    
    Sie können jetzt sowohl 32-Bit- als auch 64-Bit-XLLs kompilieren und verknüpfen. Weitere Informationen finden Sie unter [Creating XLLs](creating-xlls.md).
    
## <a name="see-also"></a>Siehe auch



[Entwickeln von XLLs für Excel](developing-excel-xlls.md)
  
[Programmieren mit der C-API in Excel](programming-with-the-c-api-in-excel.md)
  
[Multithreading und Speicherkonflikte in Excel](multithreading-and-memory-contention-in-excel.md)


[Erste Schritte mit dem Excel XLL SDK](getting-started-with-the-excel-xll-sdk.md)

