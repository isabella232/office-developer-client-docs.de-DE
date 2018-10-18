---
title: Angeben der Threads pro Prozessor in IIS
TOCTitle: Specifying Threads Per Processor on IIS
ms:assetid: 12889d7b-5415-8077-2ca0-1c3a96fb89ec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248898(v=office.15)
ms:contentKeyID: 48543344
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5041eb32397fc9a234d0e4a0fff622f31b56a0a5
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603357"
---
# <a name="specifying-threads-per-processor-on-iis"></a>Angeben der Threads pro Prozessor in IIS


**Betrifft**: Access 2013 | Office 2013

<<<<<<< HEAD beim Verwenden von RDS mit Internetinformationsdienste (IIS) 4.0 oder höher, kann die Anzahl der Threads pro Prozessor durch Bearbeiten der Registrierung auf dem Webserver gesteuert werden. Die Anzahl von Threads pro Prozessor kann sich auf die Leistung bei hohem Datenverkehr oder bei niedrigem Datenverkehr mit umfangreichen Abfragen auswirken. Testen Sie verschiedene Werte, um die besten Ergebnisse zu erzielen.
=== Beim Verwenden von RDS mit Internetinformationsdienste (IIS) 4.0 oder höher, kann die Anzahl der Threads pro Prozessor durch Bearbeiten der Registrierung auf dem Webserver gesteuert werden. Die Anzahl von Threads pro Prozessor kann sich auf die Leistung bei hohem Datenverkehr oder bei niedrigem Datenverkehr mit umfangreichen Abfragen auswirken. Testen Sie verschiedene Werte, um die besten Ergebnisse zu erzielen.
>>>>>>> master

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

