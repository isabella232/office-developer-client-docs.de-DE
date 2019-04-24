---
title: Neuerungen in der C-API für Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c-API [Excel 2007], What es New
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 64e3933ec25f0771db5bd36bbf57f3f259cdc8a1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310269"
---
# <a name="whats-new-in-the-c-api-for-excel"></a>Neuerungen in der C-API für Excel

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
In Verbindung mit Microsoft Excel 2013 enthält das Microsoft Excel 2013 XLL Software Development Kit (SDK) Unterstützung für die folgenden Features.
  
- **Neue Funktionen**
    
    Das Microsoft Excel 2013 XLL-SDK unterstützt das Aufrufen von zurück zu allen neuen Arbeitsblattfunktionen in Excel 2013. Weitere Informationen zum Aufrufen von Excel 2013-Funktionen finden Sie unter [Aufrufen von Excel aus der DLL oder XLL](calling-into-excel-from-the-dll-or-xll.md).
    
- **Asynchrone benutzerdefinierte Funktionen**
    
    Excel 2013 unterstützt das Aufrufen von benutzerdefinierten Funktionen (UDF) asynchron, wodurch die Leistung verbessert werden kann, da mehrere Berechnungen gleichzeitig ausgeführt werden können. Weitere Informationen zu asynchronen UDFs finden Sie unter [asynchrone benutzerdefinierte Funktionen](asynchronous-user-defined-functions.md).
    
- **Cluster-Konnektoren**
    
    Cluster-Konnektoren ermöglichen UDFs die Ausführung auf Hochleistungs-Compute-Clustern. Weitere Informationen zum Erstellen von Cluster-Konnektoren finden Sie unter [developIng Excel Cluster Connectors](developing-excel-cluster-connectors.md).
    
    > [!NOTE]
    > XLL-Add-Ins, die Sie in Compute-Clustern ausführen möchten, müssen nur Cluster sichere Funktionen aufrufen. Weitere Informationen zu den Funktionen, die Sie verwenden können, finden Sie unter [Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md) und [Cluster Safe Functions](cluster-safe-functions.md). 
  
- **64-Bit-Unterstützung**
    
    Sie können nun sowohl 32-Bit-als auch 64-Bit-XLLs kompilieren und verknüpfen. Weitere Informationen finden Sie unter [Creating XLLs](creating-xlls.md).
    
## <a name="see-also"></a>Siehe auch



[Entwickeln von XLLs für Excel](developing-excel-xlls.md)
  
[Programmieren mit der C-API in Excel](programming-with-the-c-api-in-excel.md)
  
[Multithreading und Speicherkonflikte in Excel](multithreading-and-memory-contention-in-excel.md)


[Erste Schritte mit dem Excel XLL SDK](getting-started-with-the-excel-xll-sdk.md)

