---
title: Cluster sichere Funktionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 787badaf-8782-454d-a016-7eae83bbd8a9
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: d32925fcd5c3be7fe3e615ee2290f25c7595911c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310976"
---
# <a name="cluster-safe-functions"></a>Cluster sichere Funktionen

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
In Excel 2013 kann Excel benutzerdefinierte Funktionen (User-Defined Function, UDF)-Aufrufe an einen Hochleistungs-Computing-Cluster über eine dedizierte Cluster-Connector-Schnittstelle Abladen. Compute Cluster vendors stellen Cluster-Konnektoren bereit. UDF-Autoren können Ihre UDFs als Cluster sicher deklarieren, und wenn ein Cluster-Konnektor vorhanden ist, sendet Excel Aufrufe an diese UDFs an den Cluster-Konnektor zur Entlastung.
  
Wenn Excel eine Cluster sichere UDF während der Neuberechnung erkennt, übergibt Sie den Namen der XLL, die derzeit läuft, den Namen des Cluster sicheren UDF und alle Parameter an den Cluster-Konnektor. Der Connector führt den UDF-Aufruf Remote aus und gibt die Ergebnisse an Excel zurück. Die nicht abhängige Berechnung wird fortgesetzt, und wenn der Cluster-Konnektor die UDF-Funktion abgeschlossen hat, werden die Ergebnisse an Excel übergeben, und die abhängigen Berechnungen werden fortgesetzt. Der Mechanismus für dieses asynchrone Verhalten imitiert den Mechanismus, der von asynchronen UDFs verwendet wird, mit der Ausnahme, dass der Cluster-Konnektor die asynchronen Aspekte anstelle des UDF-Autors verwaltet. In der Regel implementiert ein Cluster-Connector einen XLL-Shim zum Laden von XLLs und zum Ausführen von UDFs auf Compute-Clusterknoten.
  
Die Mechanik der Deklaration von UDFs als Cluster sicher ähnelt denen der Deklaration von UDFs als sicher für die Neuberechnung mit mehreren Threads. Da die UDF jedoch nicht unbedingt auf demselben Computer wie andere UDFs aus derselben Excel-Sitzung läuft, gibt es unterschiedliche Aspekte beim Schreiben von Cluster sicheren UDFs.
  
Um eine UDF als Cluster sicher zu registrieren, müssen Sie die [xlfRegister (Form 1)](xlfregister-form-1.md) -Rückruffunktion über die **Excel12** -oder **Excel12v** -Schnittstelle aufrufen. Weitere Informationen zu diesen Schnittstellen finden Sie unter [Excel4/Excel12](excel4-excel12.md) und [Excel4v/Excel12v](excel4v-excel12v.md). Das Registrieren einer UDF als Cluster-Safe über die **Excel4** -oder **Excel4v** -Schnittstelle wird nicht unterstützt. 
  
Wenn Sie eine Funktion als Cluster sicher registrieren, müssen Sie sicherstellen, dass sich die Funktion Cluster sicher verhält. Obwohl das genaue Verhalten des Cluster-Konnektors implementierungsspezifisch ist, sollten Sie die UDF so entwerfen, dass Sie auf einem verteilten Computersystem ausgeführt wird und über die folgenden Merkmale verfügt:
  
- Eine UDF sollte nicht auf einen Speicherstatus angewiesen sein. Eine UDF sollte sich beispielsweise nicht auf einen vorhandenen Cache im Arbeitsspeicher verlassen.
    
- Eine UDF sollte keine Excel-Rückrufe ausführen, die der Cluster-Connector-Anbieter nicht unterstützt.
    
Neben dem Cluster sicheren Verhalten gelten für Cluster sichere UDFs die folgenden technischen Einschränkungen:
  
1. Keine XLOPER-Argumente (Typen ' P ', ' R ').
    
2. Keine XLOPER12-Argumente, die Range-Verweise unterstützen (Typ "U").
    
3. Es kann sich nicht um eine entsprechende Makroblatt Funktion handeln ('&amp;# ' und ' ' kann nicht kombiniert werden).
    
Für UDFs mit kürzeren Ausführungszeiten kann der Aufwand für die Verschiebung größer sein als die Zeit, die die UDF-Ausführung benötigt wird, was viele der Vorteile der Verwendung dieser Infrastruktur negiert.
  
> [!NOTE]
> Sie können keine Cluster sichere UDF als asynchrone UDF deklarieren. 
  
Eine UDF kann bestimmen, ob Sie mit einem Cluster-Konnektor ausgeführt wird, indem Sie die [xlRunningOnCluster](xlrunningoncluster.md) -Rückruffunktion aufrufen. 
  

