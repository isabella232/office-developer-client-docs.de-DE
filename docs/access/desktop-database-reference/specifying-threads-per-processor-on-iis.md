---
title: Angeben der Threads pro Prozessor in IIS
TOCTitle: Specifying Threads Per Processor on IIS
ms:assetid: 12889d7b-5415-8077-2ca0-1c3a96fb89ec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248898(v=office.15)
ms:contentKeyID: 48543344
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de3c8c99c7f615928ea0a0f1e15171cc90b25f3d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473233"
---
# <a name="specifying-threads-per-processor-on-iis"></a>Angeben der Threads pro Prozessor in IIS


**Betrifft**: Access 2013 | Office 2013

Wenn Sie RDS mit Internetinformationsdienste (IIS) 4.0 oder höher verwenden, können Sie die pro Prozessor verwendete Anzahl von Threads steuern, indem Sie die Registrierung auf dem Webserver bearbeiten. Die Anzahl von Threads pro Prozessor kann sich auf die Leistung bei hohem Datenverkehr oder bei niedrigem Datenverkehr mit umfangreichen Abfragen auswirken. Testen Sie verschiedene Werte, um die besten Ergebnisse zu erzielen.

Die zum Ermitteln und Ändern des Standardwerts dieser Einstellung verwendete Methode hängt von der Konfiguration des Servers mit IIS 4.0 ab.

Wenn MDAC 2.1.2.4202.3 (GA) oder höher auf dem IIS-Server installiert ist, verwendet RDS denselben Threadpool der Komponentendienste (oder von Microsoft Transaction Server bei Verwendung von Windows NT) wie ASP-Skripts. Der Standardwert für die Anzahl von Threads pro Prozessor ist 10. Wenn Sie den Standardwert ändern möchten, müssen Sie der Serverregistrierung den folgenden Schlüssel hinzufügen:

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

wobei *MaxPoolThreads* ist eine REG\_DWORD-Wert. *MaxPoolThreads* wird nicht in der Registrierung angezeigt, es sei denn, es ausdrücklich hinzugefügt wird. Die gültigen Werte liegen zwischen 5 und dem empfohlenen Maximum von 20. Wenn der durch den Registrierungsschlüssel angegebene Wert größer als der Wert des Schlüssels *PoolThreadLimit* (befindet sich unter dem gleichen Pfad) ist, wird *PoolThreadLimit* Wert verwendet.

Ist hingegen MDAC 2.1 2.1.1.3711.11 (GA) oder nieder auf dem IIS-Server installiert, ist 6 der Standardwert für die Anzahl von Threads pro Prozessor. Wenn Sie den Standardwert ändern möchten, müssen Sie der Serverregistrierung den folgenden Schlüssel hinzufügen:

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

wobei *ADCThreads* ist eine REG\_DWORD-Wert. *ADCThreads* wird nicht in der Registrierung angezeigt, es sei denn, es ausdrücklich hinzugefügt wird. Die gültigen Werte liegen zwischen 1 und 50. Ist der im Registrierungsschlüssel angegebene Wert größer als 50, wird der Maximalwert verwendet (50).

