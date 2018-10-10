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
# <a name="specifying-threads-per-processor-on-iis"></a><span data-ttu-id="16955-102">Angeben der Threads pro Prozessor in IIS</span><span class="sxs-lookup"><span data-stu-id="16955-102">Specifying Threads Per Processor on IIS</span></span>


<span data-ttu-id="16955-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="16955-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="16955-p101">Wenn Sie RDS mit Internetinformationsdienste (IIS) 4.0 oder höher verwenden, können Sie die pro Prozessor verwendete Anzahl von Threads steuern, indem Sie die Registrierung auf dem Webserver bearbeiten. Die Anzahl von Threads pro Prozessor kann sich auf die Leistung bei hohem Datenverkehr oder bei niedrigem Datenverkehr mit umfangreichen Abfragen auswirken. Testen Sie verschiedene Werte, um die besten Ergebnisse zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="16955-p101">When using RDS with Internet Information Services 4.0 or later, the number of threads created per processor can be controlled by manipulating the registry on the Web server. The number of threads per processor can affect performance in a high traffic situation, or in low traffic situations with large query sizes. The user should experiment for best results.</span></span>

<span data-ttu-id="16955-107">Die zum Ermitteln und Ändern des Standardwerts dieser Einstellung verwendete Methode hängt von der Konfiguration des Servers mit IIS 4.0 ab.</span><span class="sxs-lookup"><span data-stu-id="16955-107">The method used to determine and change the default value for this setting depends upon the configuration of the IIS 4.0 server.</span></span>

<span data-ttu-id="16955-p102">Wenn MDAC 2.1.2.4202.3 (GA) oder höher auf dem IIS-Server installiert ist, verwendet RDS denselben Threadpool der Komponentendienste (oder von Microsoft Transaction Server bei Verwendung von Windows NT) wie ASP-Skripts. Der Standardwert für die Anzahl von Threads pro Prozessor ist 10. Wenn Sie den Standardwert ändern möchten, müssen Sie der Serverregistrierung den folgenden Schlüssel hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="16955-p102">With MDAC 2.1.2.4202.3 (GA) or later installed on the IIS server, RDS uses the same Component Services (or Microsoft Transaction Services, if you are using Windows NT) thread pool as ASP scripts use. The default value for the number of threads per processor is 10. To change the default, you must add the following key to the server registry:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

<span data-ttu-id="16955-111">wobei *MaxPoolThreads* ist eine REG\_DWORD-Wert.</span><span class="sxs-lookup"><span data-stu-id="16955-111">where *MaxPoolThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="16955-112">*MaxPoolThreads* wird nicht in der Registrierung angezeigt, es sei denn, es ausdrücklich hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="16955-112">*MaxPoolThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="16955-113">Die gültigen Werte liegen zwischen 5 und dem empfohlenen Maximum von 20.</span><span class="sxs-lookup"><span data-stu-id="16955-113">Valid values range from 5 to a recommended maximum of 20.</span></span> <span data-ttu-id="16955-114">Wenn der durch den Registrierungsschlüssel angegebene Wert größer als der Wert des Schlüssels *PoolThreadLimit* (befindet sich unter dem gleichen Pfad) ist, wird *PoolThreadLimit* Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="16955-114">If the value specified by the registry key is greater than the value of the *PoolThreadLimit* key (located under the same path), then *PoolThreadLimit* value is used.</span></span>

<span data-ttu-id="16955-p104">Ist hingegen MDAC 2.1 2.1.1.3711.11 (GA) oder nieder auf dem IIS-Server installiert, ist 6 der Standardwert für die Anzahl von Threads pro Prozessor. Wenn Sie den Standardwert ändern möchten, müssen Sie der Serverregistrierung den folgenden Schlüssel hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="16955-p104">Alternatively, if MDAC 2.1 2.1.1.3711.11 (GA) or earlier is installed on the IIS server, the default value for the number of threads per processor is 6. To change the default, you must add the following key to the registry on the IIS server:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

<span data-ttu-id="16955-117">wobei *ADCThreads* ist eine REG\_DWORD-Wert.</span><span class="sxs-lookup"><span data-stu-id="16955-117">where *ADCThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="16955-118">*ADCThreads* wird nicht in der Registrierung angezeigt, es sei denn, es ausdrücklich hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="16955-118">*ADCThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="16955-119">Die gültigen Werte liegen zwischen 1 und 50.</span><span class="sxs-lookup"><span data-stu-id="16955-119">The range of valid values is 1 to 50.</span></span> <span data-ttu-id="16955-120">Ist der im Registrierungsschlüssel angegebene Wert größer als 50, wird der Maximalwert verwendet (50).</span><span class="sxs-lookup"><span data-stu-id="16955-120">If the value specified by the registry key is greater than 50, then the maximum value is used (50).</span></span>

