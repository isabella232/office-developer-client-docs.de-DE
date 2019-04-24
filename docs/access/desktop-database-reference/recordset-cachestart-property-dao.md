---
title: Recordset. CacheStart-Eigenschaft (DAO)
TOCTitle: CacheStart Property
ms:assetid: 03814312-660a-d8e9-8a7b-bc14d66e05ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844802(v=office.15)
ms:contentKeyID: 48542986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053171
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 514f109f0eed902287e519bcd7a729397e70eaa5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300616"
---
# <a name="recordsetcachestart-property-dao"></a><span data-ttu-id="bc7ca-102">Recordset. CacheStart-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="bc7ca-102">Recordset.CacheStart property (DAO)</span></span>


<span data-ttu-id="bc7ca-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bc7ca-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bc7ca-104">Legt einen Wert fest, der das Lesezeichen des ersten Datensatzes in einem Recordset-Objekt angibt, das Daten enthält, die lokal von einer ODBC-Datenquelle zwischengespeichert werden sollen, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="bc7ca-104">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="bc7ca-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc7ca-105">Syntax</span></span>

<span data-ttu-id="bc7ca-106">*Ausdruck* . CacheStart</span><span class="sxs-lookup"><span data-stu-id="bc7ca-106">*expression* .CacheStart</span></span>

<span data-ttu-id="bc7ca-107">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="bc7ca-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc7ca-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc7ca-108">Remarks</span></span>

<span data-ttu-id="bc7ca-p101">Wenn Sie Daten von einem Remoteserver mit **Recordset**-Objekten abrufen, kann die Leistung durch eine Zwischenspeicherung gesteigert werden. Ein Zwischenspeicher ist ein Bereich im lokalen Speicher, an dem die zuletzt vom Server abgerufenen Daten gespeichert werden. Dies ist nützlich, wenn Benutzer dieselben Daten während der Ausführung des Programms wiederholt abrufen. Wenn Benutzer Daten abrufen, überprüft die Microsoft Access-Datenbank-Engine, ob die Daten im Zwischenspeicher enthalten sind, anstatt sie vom Server abzurufen. Dies erfordert weniger Zeit. Im Zwischenspeicher werden nur Daten gespeichert, die aus einer ODBC-Datenquelle stammen.</span><span class="sxs-lookup"><span data-stu-id="bc7ca-p101">Data caching improves performance if you use **Recordset** objects to retrieve data from a remote server. A cache is a space in local memory that holds the data most recently retrieved from the server; this is useful if users request the data again while the application is running. When users request data, the Microsoft Access database engine checks the cache for the requested data first rather than retrieving it from the server, which takes more time. The cache only saves data that comes from an ODBC data source.</span></span>

<span data-ttu-id="bc7ca-p102">Jede ODBC-Datenquelle, die mit einer Microsoft Access-Datenbank-Engine verknüpft ist, wie etwa eine verknüpfte Tabelle, kann einen lokalen Zwischenspeicher haben. Zum Erstellen des Zwischenspeichers öffnen Sie ein **Recordset**-Objekt in der Remotedatenquelle und legen die Eigenschaften **CacheSize** und **[CacheStart](recordset-cachestart-property-dao.md)** fest. Anschließend verwenden Sie die **[FillCache](recordset-fillcache-method-dao.md)** -Methode oder durchlaufen die Datensätze mit den **Move**-Methoden.</span><span class="sxs-lookup"><span data-stu-id="bc7ca-p102">Any Microsoft Access database engine-connected ODBC data source, such as a linked table, can have a local cache. To create the cache, open a **Recordset** object from the remote data source, set the **CacheSize** and **[CacheStart](recordset-cachestart-property-dao.md)** properties, and then use the **[FillCache](recordset-fillcache-method-dao.md)** method, or step through the records by using the **Move** methods.</span></span>

<span data-ttu-id="bc7ca-p103">Der Wert der **CacheStart**-Eigenschaft ist das Lesezeichen des ersten Datensatzes im **Recordset**-Objekt, das zwischengespeichert werden soll. Sie können das Lesezeichen jedes beliebigen Datensatzes verwenden, um die **CacheStart**-Eigenschaft festzulegen. Machen Sie den Datensatz, bei dem der Zwischenspeicher starten soll, zum aktuellen Datensatz, und legen Sie die **CacheStart**-Eigenschaft auf den Wert der **[Bookmark](recordset-bookmark-property-dao.md)** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="bc7ca-p103">The **CacheStart** property setting is the bookmark of the first record in the **Recordset** object to be cached. You can use the bookmark of any record to set the **CacheStart** property. Make the record you want to start the cache the current record, and set the **CacheStart** property equal to the **[Bookmark](recordset-bookmark-property-dao.md)** property.</span></span>

<span data-ttu-id="bc7ca-118">Das Microsoft Access-Datenbankmodul fordert Datensätze innerhalb des Cachebereichs aus dem Cache an, und es fordert Datensätze außerhalb des Cachebereichs vom Server an.</span><span class="sxs-lookup"><span data-stu-id="bc7ca-118">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="bc7ca-119">Aus dem Zwischenspeicher abgerufene Datensätze spiegeln die Änderungen, die gleichzeitig von anderen Benutzern vorgenommen wurden, nicht wider.</span><span class="sxs-lookup"><span data-stu-id="bc7ca-119">Records retrieved from the cache don't reflect changes made concurrently to the source data by other users.</span></span>

<span data-ttu-id="bc7ca-120">Sie können die Aktualisierung aller Daten im Zwischenspeicher erzwingen, indem Sie die **CacheSize**-Eigenschaft des **Recordset**-Objekts auf 0 und dann zurück auf die ursprünglich angeforderte Zwischenspeichergröße setzen. Anschließend verwenden Sie die **FillCache**-Methode.</span><span class="sxs-lookup"><span data-stu-id="bc7ca-120">To force an update of all the cached data, set the **CacheSize** property of the **Recordset** object to 0, re-set it to the size of the cache you originally requested, and then use the **FillCache** method.</span></span>

