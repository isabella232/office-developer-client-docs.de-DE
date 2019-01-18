---
title: Recordset2.CacheStart-Eigenschaft (DAO)
TOCTitle: CacheStart Property
ms:assetid: 2e9c2b0d-b382-e4d6-9406-ace0e538a7b7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192239(v=office.15)
ms:contentKeyID: 48543989
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e6f68cc9704d7dafe7a1d779b338294c9d5fc1c8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718798"
---
# <a name="recordset2cachestart-property-dao"></a><span data-ttu-id="b451d-102">Recordset2.CacheStart-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="b451d-102">Recordset2.CacheStart property (DAO)</span></span>


<span data-ttu-id="b451d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b451d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b451d-104">Legt einen Wert fest, der das Lesezeichen des ersten Datensatzes in einem Recordset-Objekt angibt, das Daten enthält, die lokal von einer ODBC-Datenquelle zwischengespeichert werden sollen, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="b451d-104">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="b451d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b451d-105">Syntax</span></span>

<span data-ttu-id="b451d-106">*Ausdruck* . CacheStart</span><span class="sxs-lookup"><span data-stu-id="b451d-106">*expression* .CacheStart</span></span>

<span data-ttu-id="b451d-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="b451d-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b451d-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b451d-108">Remarks</span></span>

<span data-ttu-id="b451d-p101">Das Zwischenspeichern von Daten erhöht die Leistung, wenn Sie **Recordset**-Objekte zum Abrufen von Daten eines Remoteservers verwenden. Ein Cache ist ein Bereich im lokalen Arbeitsspeicher, in dem die zuletzt vom Server abgerufenen Daten aufbewahrt werden. Das ist praktisch, wenn die Daten während der Ausführung der Anwendung erneut vom Benutzer abgerufen werden. Fordern Benutzer Daten an, sucht das Microsoft Access-Datenbankmodul zuerst im Cache nach den angeforderten Daten, bevor es sie vom Server abruft, was länger dauert. Im Cache werden nur von ODBC-Datenquellen stammende Daten gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b451d-p101">Data caching improves performance if you use **Recordset** objects to retrieve data from a remote server. A cache is a space in local memory that holds the data most recently retrieved from the server; this is useful if users request the data again while the application is running. When users request data, the Microsoft Access database engine checks the cache for the requested data first rather than retrieving it from the server, which takes more time. The cache only saves data that comes from an ODBC data source.</span></span>

<span data-ttu-id="b451d-p102">Jede mit dem Microsoft Access-Datenbankmodul verbundene ODBC-Datenquelle (wie z. B. eine verknüpfte Tabelle) kann einen lokalen Cache besitzen. Öffnen Sie zum Erstellen eines Caches ein **Recordset**-Objekt in der Remotedatenquelle, legen Sie die Eigenschaften **CacheSize** und **[CacheStart](recordset2-cachestart-property-dao.md)** fest, und verwenden Sie dann die **[FillCache](recordset2-fillcache-method-dao.md)** -Methode, oder wechseln Sie mit den **Move**-Methoden durch die Datensätze.</span><span class="sxs-lookup"><span data-stu-id="b451d-p102">Any Microsoft Access database engine-connected ODBC data source, such as a linked table, can have a local cache. To create the cache, open a **Recordset** object from the remote data source, set the **CacheSize** and **[CacheStart](recordset2-cachestart-property-dao.md)** properties, and then use the **[FillCache](recordset2-fillcache-method-dao.md)** method, or step through the records by using the **Move** methods.</span></span>

<span data-ttu-id="b451d-p103">Die Einstellung der **CacheStart**-Eigenschaft ist die Textmarke des ersten Datensatzes im zwischenzuspeichernden **Recordset**-Objekt. Sie können die Textmarke jedes beliebigen Datensatzes zum Festlegen der **CacheStart**-Eigenschaft verwenden. Machen Sie den Datensatz, mit dem Sie den Cache beginnen möchten, zum aktuellen Datensatz, und legen Sie die **CacheStart**-Eigenschaft auf den gleichen Wert wie die **[Bookmark](recordset2-bookmark-property-dao.md)** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="b451d-p103">The **CacheStart** property setting is the bookmark of the first record in the **Recordset** object to be cached. You can use the bookmark of any record to set the **CacheStart** property. Make the record you want to start the cache the current record, and set the **CacheStart** property equal to the **[Bookmark](recordset2-bookmark-property-dao.md)** property.</span></span>

<span data-ttu-id="b451d-118">Das Microsoft Access-Datenbankmodul fordert Datensätze innerhalb des Cachebereichs aus dem Cache an, und es fordert Datensätze außerhalb des Cachebereichs vom Server an.</span><span class="sxs-lookup"><span data-stu-id="b451d-118">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="b451d-119">Aus dem Cache abgerufene Datensätze enthalten keine Änderungen, die andere Benutzer gleichzeitig an den Quelldaten vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="b451d-119">Records retrieved from the cache don't reflect changes made concurrently to the source data by other users.</span></span>

<span data-ttu-id="b451d-120">Sie können die Aktualisierung aller Daten im Zwischenspeicher erzwingen, indem Sie die **CacheSize**-Eigenschaft des **Recordset**-Objekts auf 0 und dann zurück auf die ursprünglich angeforderte Zwischenspeichergröße setzen. Anschließend verwenden Sie die **FillCache**-Methode.</span><span class="sxs-lookup"><span data-stu-id="b451d-120">To force an update of all the cached data, set the **CacheSize** property of the **Recordset** object to 0, re-set it to the size of the cache you originally requested, and then use the **FillCache** method.</span></span>

