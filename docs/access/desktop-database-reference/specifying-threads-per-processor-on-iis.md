---
title: Angeben von Threads pro Prozessor auf IIS
TOCTitle: Specifying threads per processor on IIS
ms:assetid: 12889d7b-5415-8077-2ca0-1c3a96fb89ec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248898(v=office.15)
ms:contentKeyID: 48543344
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 57e4b6228588af7f0d58caf53d3e093e824c7854
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308589"
---
# <a name="specifying-threads-per-processor-on-iis"></a>Angeben von Threads pro Prozessor auf IIS


**Gilt für**: Access 2013, Office 2013

Bei Verwendung von RDS mit Internet Informationsdienste 4,0 oder höher kann die Anzahl der pro Prozessor erstellten Threads gesteuert werden, indem die Registrierung auf dem Webserver manipuliert wird. Die Anzahl von Threads pro Prozessor kann sich auf die Leistung bei hohem Datenverkehr oder bei niedrigem Datenverkehr mit umfangreichen Abfragen auswirken. Testen Sie verschiedene Werte, um die besten Ergebnisse zu erzielen.

Die zum Ermitteln und Ändern des Standardwerts dieser Einstellung verwendete Methode hängt von der Konfiguration des Servers mit IIS 4.0 ab.

Wenn MDAC 2.1.2.4202.3 (GA) oder höher auf dem IIS-Server installiert ist, verwendet RDS denselben Threadpool der Komponentendienste (oder von Microsoft Transaction Server bei Verwendung von Windows NT) wie ASP-Skripts. Der Standardwert für die Anzahl von Threads pro Prozessor ist 10. Wenn Sie den Standardwert ändern möchten, müssen Sie der Serverregistrierung den folgenden Schlüssel hinzufügen:

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

Dabei ist *MaxPoolThreads* ein reg\_-DWORD. Der Schlüssel *MaxPoolThreads* ist erst in der Registrierung enthalten, wenn er ausdrücklich hinzugefügt wird. Die gültigen Werte liegen zwischen 5 und dem empfohlenen Maximum von 20. Wenn der im Registrierungsschlüssel angegebene Wert höher ist als der Wert des Schlüssels *PoolThreadLimit* (in demselben Pfad), wird der Wert von *PoolThreadLimit* verwendet.

Ist hingegen MDAC 2.1 2.1.1.3711.11 (GA) oder nieder auf dem IIS-Server installiert, ist 6 der Standardwert für die Anzahl von Threads pro Prozessor. Wenn Sie den Standardwert ändern möchten, müssen Sie der Serverregistrierung den folgenden Schlüssel hinzufügen:

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

Dabei ist *ADCThreads* ein reg\_-DWORD. Der Schlüssel *ADCThreads* ist erst in der Registrierung enthalten, wenn er ausdrücklich hinzugefügt wird. Die gültigen Werte liegen zwischen 1 und 50. Ist der im Registrierungsschlüssel angegebene Wert größer als 50, wird der Maximalwert verwendet (50).

