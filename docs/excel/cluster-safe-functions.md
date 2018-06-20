---
title: Clustersichere Funktionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 787badaf-8782-454d-a016-7eae83bbd8a9
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: f73f49e4d76a8545399eede283b70551ee6569f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790383"
---
# <a name="cluster-safe-functions"></a>Clustersichere Funktionen

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
In Excel 2013 kann Excel benutzerdefinierte Funktion (UDF) Anrufe an einen High Performance computing Cluster über eine dedizierte Cluster Connector-Schnittstelle abnimmt. Compute bereitstellen Cluster Clusterconnectoren. UDF-Autoren können deklarieren ihre UDFs als Cluster sichere und wenn ein Clusterconnector vorhanden ist, sendet Excel Anrufe an diese UDFs klicken Sie dann auf den Clusterconnector für die Verschiebung.
  
Wenn Excel während einer neuberechnung eine UDF clustersichere ermittelt, übergibt sie den Namen der XLL, die aktuell, den Namen des clustersichere UDFs und keine Parameter an dem Konnektor Cluster ausgeführt wird. Der Connector wird den UDF-Aufruf Remote ausgeführt und gibt die Ergebnisse nach Excel zurück. Unabhängige Berechnung weiterhin und nachdem die Clusterconnector die UDF ausgeführt wurde, übergibt die Ergebnisse nach Excel und abhängige Berechnungen fortfahren. Mechanismus für dieses asynchronen Verhalten imitiert ein Mechanismus, mit der asynchronen UDFs mit der Ausnahme, dass die Clusterconnector die asynchronen Aspekte anstelle der UDF-Autor verwaltet wird. In der Regel implementiert ein Clusterconnector eine XLL-Shim um XLLs laden und Ausführen von UDFs auf Compute Cluster-Knoten.
  
Die Abläufe bei der Deklarieren von UDFs als clustersichere ähneln jenen UDFs als sicher für Multithread-neuberechnung zu deklarieren. Da die UDF nicht notwendigerweise auf demselben Computer wie andere UDFs aus der gleichen Excel-Sitzung ausgeführt wird, gibt es jedoch verschiedene Aspekte beim Schreiben von clustersichere UDFs.
  
Um eine UDF als clustersichere registrieren, müssen Sie über die Schnittstelle **Excel12** oder **Excel12v** die Rückruffunktion [XlfRegister (Formular 1)](xlfregister-form-1.md) aufrufen. Weitere Informationen zu diesen Schnittstellen finden Sie unter der [Excel4/Excel12](excel4-excel12.md) und [Excel4v/Excel12v](excel4v-excel12v.md). Registrieren einer UDFs als clustersichere über die Schnittstelle **Excel4** oder **Excel4v** wird nicht unterstützt. 
  
Wenn Sie eine Funktion als clustersichere registrieren, müssen Sie sicherstellen, dass die Funktion in einer Weise clustersichere verhält. Obwohl das genaue Verhalten der Cluster Verbindung implementierungsspezifischen ist, sollten Sie die UDF-Datei in einem verteilten Computersystem ausgeführt und die folgenden Merkmale aufweisen entwerfen:
  
- Eine UDF sollten auf jeden Speicherzustand nicht verlassen. Beispielsweise sollte eine UDF nicht auf einen vorhandenen in-Memory-Cache verlassen.
    
- Eine UDF-Datei sollte nicht Excel Rückrufe ausführen, die der Cluster-Connector-Anbieter nicht unterstützt.
    
Zusätzlich zu clustersichere Verhalten stehen die folgenden technischen Einschränkungen auf clustersichere UDFs:
  
1. Keine XLOPER Argumente (Typen "P", "R").
    
2. Keine XLOPER12 Argumente, die Bereichs-Verweise (Typ "U") unterstützen.
    
3. Keine entsprechende Funktion Makro Blatt zulässig ('#' und '&amp;' kann nicht kombiniert werden).
    
Für UDF-Dateien mit kürzeren Ausführungszeiten der Aufwand für die Verschiebung möglicherweise größer als die Zeit, die die UDF ausgeführt wird, benötigt negieren viele der Vorteile der Verwendung dieser Infrastruktur.
  
> [!NOTE]
> Sie können eine UDF clustersichere als eine asynchrone UDF nicht deklarieren. 
  
Eine UDF kann bestimmen, ob es mit einen Clusterconnector durch Aufrufen von der [XlRunningOnCluster](xlrunningoncluster.md) Callback-Funktion ausgeführt wird. 
  

