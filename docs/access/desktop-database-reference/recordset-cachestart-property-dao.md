---
title: Recordset.CacheStart-Eigenschaft (DAO)
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
ms.openlocfilehash: c73a12803a65f84d11ab62955d80ccda3d0825fb
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919178"
---
# <a name="recordsetcachestart-property-dao"></a><span data-ttu-id="33ffc-102">Recordset.CacheStart-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="33ffc-102">Recordset.CacheStart property (DAO)</span></span>


<span data-ttu-id="33ffc-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="33ffc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="33ffc-104">Legt einen Wert fest, der das Lesezeichen des ersten Datensatzes in einem Recordset-Objekt angibt, das Daten enthält, die lokal von einer ODBC-Datenquelle zwischengespeichert werden sollen, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="33ffc-104">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="33ffc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="33ffc-105">Syntax</span></span>

<span data-ttu-id="33ffc-106">*Ausdruck* . CacheStart</span><span class="sxs-lookup"><span data-stu-id="33ffc-106">*expression* .CacheStart</span></span>

<span data-ttu-id="33ffc-107">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="33ffc-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="33ffc-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33ffc-108">Remarks</span></span>

<span data-ttu-id="33ffc-p101">Das Zwischenspeichern von Daten erhöht die Leistung, wenn Sie **Recordset**-Objekte zum Abrufen von Daten eines Remoteservers verwenden. Ein Cache ist ein Bereich im lokalen Arbeitsspeicher, in dem die zuletzt vom Server abgerufenen Daten aufbewahrt werden. Das ist praktisch, wenn die Daten während der Ausführung der Anwendung erneut vom Benutzer abgerufen werden. Fordern Benutzer Daten an, sucht das Microsoft Access-Datenbankmodul zuerst im Cache nach den angeforderten Daten, bevor es sie vom Server abruft, was länger dauert. Im Cache werden nur von ODBC-Datenquellen stammende Daten gespeichert.</span><span class="sxs-lookup"><span data-stu-id="33ffc-p101">Data caching improves performance if you use **Recordset** objects to retrieve data from a remote server. A cache is a space in local memory that holds the data most recently retrieved from the server; this is useful if users request the data again while the application is running. When users request data, the Microsoft Access database engine checks the cache for the requested data first rather than retrieving it from the server, which takes more time. The cache only saves data that comes from an ODBC data source.</span></span>

<span data-ttu-id="33ffc-p102">Jede mit dem Microsoft Access-Datenbankmodul verbundene ODBC-Datenquelle (wie z. B. eine verknüpfte Tabelle) kann einen lokalen Cache besitzen. Öffnen Sie zum Erstellen eines Caches ein **Recordset**-Objekt in der Remotedatenquelle, legen Sie die Eigenschaften **CacheSize** und **[CacheStart](recordset-cachestart-property-dao.md)** fest, und verwenden Sie dann die **[FillCache](recordset-fillcache-method-dao.md)** -Methode, oder wechseln Sie mit den **Move**-Methoden durch die Datensätze.</span><span class="sxs-lookup"><span data-stu-id="33ffc-p102">Any Microsoft Access database engine-connected ODBC data source, such as a linked table, can have a local cache. To create the cache, open a **Recordset** object from the remote data source, set the **CacheSize** and **[CacheStart](recordset-cachestart-property-dao.md)** properties, and then use the **[FillCache](recordset-fillcache-method-dao.md)** method, or step through the records by using the **Move** methods.</span></span>

<span data-ttu-id="33ffc-p103">Die Einstellung der **CacheStart**-Eigenschaft ist die Textmarke des ersten Datensatzes im zwischenzuspeichernden **Recordset**-Objekt. Sie können die Textmarke jedes beliebigen Datensatzes zum Festlegen der **CacheStart**-Eigenschaft verwenden. Machen Sie den Datensatz, mit dem Sie den Cache beginnen möchten, zum aktuellen Datensatz, und legen Sie die **CacheStart**-Eigenschaft auf den gleichen Wert wie die **[Bookmark](recordset-bookmark-property-dao.md)** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="33ffc-p103">The **CacheStart** property setting is the bookmark of the first record in the **Recordset** object to be cached. You can use the bookmark of any record to set the **CacheStart** property. Make the record you want to start the cache the current record, and set the **CacheStart** property equal to the **[Bookmark](recordset-bookmark-property-dao.md)** property.</span></span>

<span data-ttu-id="33ffc-118">Das Microsoft Access-Datenbankmodul fordert Datensätze innerhalb des Cachebereichs aus dem Cache an, und es fordert Datensätze außerhalb des Cachebereichs vom Server an.</span><span class="sxs-lookup"><span data-stu-id="33ffc-118">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="33ffc-119">Aus dem Cache abgerufene Datensätze enthalten keine Änderungen, die andere Benutzer gleichzeitig an den Quelldaten vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="33ffc-119">Records retrieved from the cache don't reflect changes made concurrently to the source data by other users.</span></span>

<span data-ttu-id="33ffc-120">Sie können die Aktualisierung aller Daten im Zwischenspeicher erzwingen, indem Sie die **CacheSize**-Eigenschaft des **Recordset**-Objekts auf 0 und dann zurück auf die ursprünglich angeforderte Zwischenspeichergröße setzen. Anschließend verwenden Sie die **FillCache**-Methode.</span><span class="sxs-lookup"><span data-stu-id="33ffc-120">To force an update of all the cached data, set the **CacheSize** property of the **Recordset** object to 0, re-set it to the size of the cache you originally requested, and then use the **FillCache** method.</span></span>

