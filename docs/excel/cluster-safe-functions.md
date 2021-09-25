---
title: Clustersichere Funktionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 787badaf-8782-454d-a016-7eae83bbd8a9
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 178076fecedbe2eb2a254dcd10932e4f4f4ae60d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601414"
---
# <a name="cluster-safe-functions"></a>Clustersichere Funktionen

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
In Excel 2013 können Excel User-Defined Function (UDF)-Aufrufe an einen Hochleistungscomputingcluster über eine dedizierte Clusterconnectorschnittstelle auslagern. Computeclusteranbieter stellen Clusterconnectors bereit. UDF-Autoren können ihre UDFs als clustersicher deklarieren und dann, wenn ein Clusterkonnektor vorhanden ist, Excel Aufrufe an diese UDFs zum Offloading an den Clusterconnector senden.
  
Wenn Excel während der Neuberechnung eine clustersichere UDF ermittelt, werden der Name der aktuell ausgeführten XLL, der Name der clustersicheren UDF und alle Parameter an den Clusterconnector übergeben. Der Connector führt den UDF-Aufruf remote aus und gibt die Ergebnisse an Excel zurück. Die nicht abhängige Berechnung wird fortgesetzt, und wenn der Clusterconnector die Ausführung der UDF abgeschlossen hat, werden die Ergebnisse an Excel übergeben, und abhängige Berechnungen werden fortgesetzt. Der Mechanismus für dieses asynchrone Verhalten imitiert den Mechanismus, der von asynchronen UDFs verwendet wird, mit der Ausnahme, dass der Clusterconnector die asynchronen Aspekte anstelle des UDF-Autors verwaltet. In der Regel implementiert ein Clusterconnector einen XLL-Shim, um XLLs zu laden und UDFs auf Computeclusterknoten auszuführen.
  
Die Funktionsweise des Deklarierens von UDFs als clustersicher ähnelt denen der Deklaration von UDFs als sicher für Multithread-Neuberechnungen. Da die UDF jedoch nicht notwendigerweise auf demselben Computer wie andere UDFs aus derselben Excel Sitzung ausgeführt wird, gibt es unterschiedliche Überlegungen beim Schreiben clustersicherer UDFs.
  
Um eine UDF als clustersicher zu registrieren, müssen Sie die [xlfRegister-Rückruffunktion (Formular 1)](xlfregister-form-1.md) über die **Excel12-** oder **Excel12v-Schnittstelle** aufrufen. Weitere Informationen zu diesen Schnittstellen finden Sie unter [Excel4/Excel12](excel4-excel12.md) und [Excel4v/Excel12v.](excel4v-excel12v.md) Das Registrieren einer UDF als clustersicher über die **Excel4-** oder **Excel4v-Schnittstelle** wird nicht unterstützt. 
  
Wenn Sie eine Funktion als clustersicher registrieren, müssen Sie sicherstellen, dass sich die Funktion clustersicher verhält. Obwohl das genaue Verhalten des Clusterconnectors implementierungsspezifisch ist, sollten Sie Ihre UDF so entwerfen, dass sie auf einem verteilten Computersystem ausgeführt wird und die folgenden Merkmale aufweist:
  
- Eine UDF sollte sich nicht auf einen Speicherstatus verlassen. Beispielsweise sollte eine UDF nicht auf einem vorhandenen Speichercache basieren.
    
- A UDF should not perform Excel callbacks that the cluster connector provider does not support.
    
Zusätzlich zum clustersicheren Verhalten gelten die folgenden technischen Einschränkungen für clustersichere UDFs:
  
1. Keine XLOPER-Argumente (Typen 'P', 'R').
    
2. Keine XLOPER12-Argumente, die Bereichsverweise unterstützen (Typ "U").
    
3. Kann keine Makroblatt-Äquivalentfunktion sein ('#' und ' &amp; ' kann nicht kombiniert werden).
    
Bei UDFs mit kürzeren Ausführungszeiten kann der Mehraufwand für das Offloading größer sein als die Zeit, die die UDF für die Ausführung benötigt, was viele der Vorteile der Verwendung dieser Infrastruktur zunichte macht.
  
> [!NOTE]
> Sie können eine clustersichere UDF nicht als asynchrone UDF deklarieren. 
  
Eine UDF kann ermitteln, ob sie mithilfe eines Clusterconnectors ausgeführt wird, indem sie die [xlRunningOnCluster-Rückruffunktion](xlrunningoncluster.md) aufruft. 
  

