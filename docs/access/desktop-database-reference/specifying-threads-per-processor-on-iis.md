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
# <a name="specifying-threads-per-processor-on-iis"></a><span data-ttu-id="bf5fb-102">Angeben der Threads pro Prozessor in IIS</span><span class="sxs-lookup"><span data-stu-id="bf5fb-102">Specifying Threads Per Processor on IIS</span></span>


<span data-ttu-id="bf5fb-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bf5fb-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bf5fb-104"><<<<<<< HEAD beim Verwenden von RDS mit Internetinformationsdienste (IIS) 4.0 oder höher, kann die Anzahl der Threads pro Prozessor durch Bearbeiten der Registrierung auf dem Webserver gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="bf5fb-104"><<<<<<< HEAD When using RDS with Internet Information Services 4.0 or later, the number of threads created per processor can be controlled by manipulating the registry on the Web server.</span></span> <span data-ttu-id="bf5fb-105">Die Anzahl von Threads pro Prozessor kann sich auf die Leistung bei hohem Datenverkehr oder bei niedrigem Datenverkehr mit umfangreichen Abfragen auswirken.</span><span class="sxs-lookup"><span data-stu-id="bf5fb-105">The number of threads per processor can affect performance in a high traffic situation, or in low traffic situations with large query sizes.</span></span> <span data-ttu-id="bf5fb-106">Testen Sie verschiedene Werte, um die besten Ergebnisse zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="bf5fb-106">The user should experiment for best results.</span></span>
<span data-ttu-id="bf5fb-107">=== Beim Verwenden von RDS mit Internetinformationsdienste (IIS) 4.0 oder höher, kann die Anzahl der Threads pro Prozessor durch Bearbeiten der Registrierung auf dem Webserver gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="bf5fb-107">======= When using RDS with Internet Information Services 4.0 or later, the number of threads created per processor can be controlled by manipulating the registry on the web server.</span></span> <span data-ttu-id="bf5fb-108">Die Anzahl von Threads pro Prozessor kann sich auf die Leistung bei hohem Datenverkehr oder bei niedrigem Datenverkehr mit umfangreichen Abfragen auswirken.</span><span class="sxs-lookup"><span data-stu-id="bf5fb-108">The number of threads per processor can affect performance in a high traffic situation, or in low traffic situations with large query sizes.</span></span> <span data-ttu-id="bf5fb-109">Testen Sie verschiedene Werte, um die besten Ergebnisse zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="bf5fb-109">The user should experiment for best results.</span></span>
>>>>>>> <span data-ttu-id="bf5fb-110">master</span><span class="sxs-lookup"><span data-stu-id="bf5fb-110">master</span></span>

<span data-ttu-id="bf5fb-111">Die zum Ermitteln und Ändern des Standardwerts dieser Einstellung verwendete Methode hängt von der Konfiguration des Servers mit IIS 4.0 ab.</span><span class="sxs-lookup"><span data-stu-id="bf5fb-111">The method used to determine and change the default value for this setting depends upon the configuration of the IIS 4.0 server.</span></span>

<span data-ttu-id="bf5fb-p102">Wenn MDAC 2.1.2.4202.3 (GA) oder höher auf dem IIS-Server installiert ist, verwendet RDS denselben Threadpool der Komponentendienste (oder von Microsoft Transaction Server bei Verwendung von Windows NT) wie ASP-Skripts. Der Standardwert für die Anzahl von Threads pro Prozessor ist 10. Wenn Sie den Standardwert ändern möchten, müssen Sie der Serverregistrierung den folgenden Schlüssel hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="bf5fb-p102">With MDAC 2.1.2.4202.3 (GA) or later installed on the IIS server, RDS uses the same Component Services (or Microsoft Transaction Services, if you are using Windows NT) thread pool as ASP scripts use. The default value for the number of threads per processor is 10. To change the default, you must add the following key to the server registry:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

<span data-ttu-id="bf5fb-115">wobei *MaxPoolThreads* ist eine REG\_DWORD-Wert.</span><span class="sxs-lookup"><span data-stu-id="bf5fb-115">where *MaxPoolThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="bf5fb-116">*MaxPoolThreads* wird nicht in der Registrierung angezeigt, es sei denn, es ausdrücklich hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="bf5fb-116">*MaxPoolThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="bf5fb-117">Die gültigen Werte liegen zwischen 5 und dem empfohlenen Maximum von 20.</span><span class="sxs-lookup"><span data-stu-id="bf5fb-117">Valid values range from 5 to a recommended maximum of 20.</span></span> <span data-ttu-id="bf5fb-118">Wenn der durch den Registrierungsschlüssel angegebene Wert größer als der Wert des Schlüssels *PoolThreadLimit* (befindet sich unter dem gleichen Pfad) ist, wird *PoolThreadLimit* Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="bf5fb-118">If the value specified by the registry key is greater than the value of the *PoolThreadLimit* key (located under the same path), then *PoolThreadLimit* value is used.</span></span>

<span data-ttu-id="bf5fb-p104">Ist hingegen MDAC 2.1 2.1.1.3711.11 (GA) oder nieder auf dem IIS-Server installiert, ist 6 der Standardwert für die Anzahl von Threads pro Prozessor. Wenn Sie den Standardwert ändern möchten, müssen Sie der Serverregistrierung den folgenden Schlüssel hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="bf5fb-p104">Alternatively, if MDAC 2.1 2.1.1.3711.11 (GA) or earlier is installed on the IIS server, the default value for the number of threads per processor is 6. To change the default, you must add the following key to the registry on the IIS server:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

<span data-ttu-id="bf5fb-121">wobei *ADCThreads* ist eine REG\_DWORD-Wert.</span><span class="sxs-lookup"><span data-stu-id="bf5fb-121">where *ADCThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="bf5fb-122">*ADCThreads* wird nicht in der Registrierung angezeigt, es sei denn, es ausdrücklich hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="bf5fb-122">*ADCThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="bf5fb-123">Die gültigen Werte liegen zwischen 1 und 50.</span><span class="sxs-lookup"><span data-stu-id="bf5fb-123">The range of valid values is 1 to 50.</span></span> <span data-ttu-id="bf5fb-124">Ist der im Registrierungsschlüssel angegebene Wert größer als 50, wird der Maximalwert verwendet (50).</span><span class="sxs-lookup"><span data-stu-id="bf5fb-124">If the value specified by the registry key is greater than 50, then the maximum value is used (50).</span></span>

