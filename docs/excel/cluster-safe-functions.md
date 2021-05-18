---
title: Clustersichere Funktionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 787badaf-8782-454d-a016-7eae83bbd8a9
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d32925fcd5c3be7fe3e615ee2290f25c7595911c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409300"
---
# <a name="cluster-safe-functions"></a>Clustersichere Funktionen

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
In Excel 2013 können Excel aufrufe von User-Defined (UDF) über eine dedizierte Clusterconnectorschnittstelle an einen Hochleistungscomputercluster ausladen. Computeclusteranbieter stellen Clusterconnectors zur Verfügung. UDF-Autoren können ihre UDFs als clustersicher deklarieren und dann, wenn ein Clusterconnector vorhanden ist, Excel Aufrufe an diese UDFs zum Offloading an den Clusterconnector senden.
  
Wenn Excel bei der Neuberechnung eine clustersichere UDF ermittelt, übergibt sie den Namen der aktuell ausgeführten XLL, den Namen der clustersicheren UDF und alle Parameter an den Clusterconnector. Der Connector führt den UDF-Aufruf remote aus und gibt die Ergebnisse an Excel. Die nicht abhängige Berechnung wird fortgesetzt, und wenn der Clusterconnector die Ausführung der UDF beendet hat, werden die Ergebnisse an Excel und abhängige Berechnungen fortgesetzt. Der Mechanismus für dieses asynchrone Verhalten imitiert den mechanismus, der von asynchronen UDFs verwendet wird, mit der Ausnahme, dass der Clusterconnector die asynchronen Aspekte anstelle des UDF-Autors verwaltet. In der Regel implementiert ein Clusterconnector einen XLL-Shim zum Laden von XLLs und Ausführen von UDFs auf Computeclusterknoten.
  
Die Mechanik der Deklarierung von UDFs als clustersicher ähnelt denen der Deklarierung von UDFs als sicher für die Neuberechnung mit mehreren Threads. Da die UDF jedoch nicht unbedingt auf demselben Computer wie andere UDFs aus derselben Excel-Sitzung ausgeführt wird, gibt es beim Schreiben clustersicherer UDFs unterschiedliche Überlegungen.
  
Um eine UDF als clustersicher zu registrieren, müssen Sie die [xlfRegister (Form 1)-Rückruffunktion](xlfregister-form-1.md) über die **Excel12-** oder **Excel12v-Schnittstelle** aufrufen. Weitere Informationen zu diesen Schnittstellen finden Sie unter [Excel4/Excel12](excel4-excel12.md) und [Excel4v/Excel12v](excel4v-excel12v.md). Die Registrierung einer UDF als clustersicher über die **Excel4-** oder **Excel4v-Schnittstelle** wird nicht unterstützt. 
  
Wenn Sie eine Funktion als clustersicher registrieren, müssen Sie sicherstellen, dass sich die Funktion clustersicher verhält. Obwohl das genaue Verhalten des Clusterconnector implementierungsspezifisch ist, sollten Sie Ihre UDF so entwerfen, dass sie auf einem verteilten Computersystem ausgeführt wird und die folgenden Merkmale aufweist:
  
- Ein UDF sollte sich nicht auf einen Speicherstatus verlassen. Beispielsweise sollte sich ein UDF nicht auf einen vorhandenen Speichercache verlassen.
    
- Ein UDF sollte keine Excel ausführen, die vom Clusterconnectoranbieter nicht unterstützt werden.
    
Neben dem clustersicheren Verhalten gibt es die folgenden technischen Einschränkungen für clustersichere UDFs:
  
1. Keine XLOPER-Argumente (Typen 'P', 'R').
    
2. Keine XLOPER12-Argumente, die Bereichsverweise unterstützen (Typ 'U').
    
3. Es kann sich nicht um eine makroblattäquivalente Funktion ('#' und &amp; ' ' kann nicht kombiniert werden).
    
Bei UDFs mit kürzeren Ausführungszeiten kann der Aufwand für das Offloading größer sein als die Ausführungszeit der UDF, was viele vorteile der Verwendung dieser Infrastruktur negiert.
  
> [!NOTE]
> Sie können eine clustersichere UDF nicht als asynchrones UDF deklarieren. 
  
Eine UDF kann ermitteln, ob sie mit einem Clusterconnector ausgeführt wird, indem sie die [xlRunningOnCluster-Rückruffunktion](xlrunningoncluster.md) aufruft. 
  

