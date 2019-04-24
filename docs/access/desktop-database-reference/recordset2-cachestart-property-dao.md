---
title: Recordset2. CacheStart-Eigenschaft (DAO)
TOCTitle: CacheStart Property
ms:assetid: 2e9c2b0d-b382-e4d6-9406-ace0e538a7b7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192239(v=office.15)
ms:contentKeyID: 48543989
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e6f68cc9704d7dafe7a1d779b338294c9d5fc1c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307420"
---
# <a name="recordset2cachestart-property-dao"></a><span data-ttu-id="91779-102">Recordset2. CacheStart-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="91779-102">Recordset2.CacheStart property (DAO)</span></span>


<span data-ttu-id="91779-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="91779-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="91779-104">Legt einen Wert fest, der das Lesezeichen des ersten Datensatzes in einem Recordset-Objekt angibt, das Daten enthält, die lokal von einer ODBC-Datenquelle zwischengespeichert werden sollen, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="91779-104">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="91779-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="91779-105">Syntax</span></span>

<span data-ttu-id="91779-106">*Ausdruck* . CacheStart</span><span class="sxs-lookup"><span data-stu-id="91779-106">*expression* .CacheStart</span></span>

<span data-ttu-id="91779-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="91779-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="91779-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91779-108">Remarks</span></span>

<span data-ttu-id="91779-p101">Wenn Sie Daten von einem Remoteserver mit **Recordset**-Objekten abrufen, kann die Leistung durch eine Zwischenspeicherung gesteigert werden. Ein Zwischenspeicher ist ein Bereich im lokalen Speicher, an dem die zuletzt vom Server abgerufenen Daten gespeichert werden. Dies ist nützlich, wenn Benutzer dieselben Daten während der Ausführung des Programms wiederholt abrufen. Wenn Benutzer Daten abrufen, überprüft die Microsoft Access-Datenbank-Engine, ob die Daten im Zwischenspeicher enthalten sind, anstatt sie vom Server abzurufen. Dies erfordert weniger Zeit. Im Zwischenspeicher werden nur Daten gespeichert, die aus einer ODBC-Datenquelle stammen.</span><span class="sxs-lookup"><span data-stu-id="91779-p101">Data caching improves performance if you use **Recordset** objects to retrieve data from a remote server. A cache is a space in local memory that holds the data most recently retrieved from the server; this is useful if users request the data again while the application is running. When users request data, the Microsoft Access database engine checks the cache for the requested data first rather than retrieving it from the server, which takes more time. The cache only saves data that comes from an ODBC data source.</span></span>

<span data-ttu-id="91779-p102">Jede ODBC-Datenquelle, die mit einer Microsoft Access-Datenbank-Engine verknüpft ist, wie etwa eine verknüpfte Tabelle, kann einen lokalen Zwischenspeicher haben. Zum Erstellen des Zwischenspeichers öffnen Sie ein **Recordset**-Objekt in der Remotedatenquelle und legen die Eigenschaften **CacheSize** und **[CacheStart](recordset2-cachestart-property-dao.md)** fest. Anschließend verwenden Sie die **[FillCache](recordset2-fillcache-method-dao.md)** -Methode oder durchlaufen die Datensätze mit den **Move**-Methoden.</span><span class="sxs-lookup"><span data-stu-id="91779-p102">Any Microsoft Access database engine-connected ODBC data source, such as a linked table, can have a local cache. To create the cache, open a **Recordset** object from the remote data source, set the **CacheSize** and **[CacheStart](recordset2-cachestart-property-dao.md)** properties, and then use the **[FillCache](recordset2-fillcache-method-dao.md)** method, or step through the records by using the **Move** methods.</span></span>

<span data-ttu-id="91779-p103">Der Wert der **CacheStart**-Eigenschaft ist das Lesezeichen des ersten Datensatzes im **Recordset**-Objekt, das zwischengespeichert werden soll. Sie können das Lesezeichen jedes beliebigen Datensatzes verwenden, um die **CacheStart**-Eigenschaft festzulegen. Machen Sie den Datensatz, bei dem der Zwischenspeicher starten soll, zum aktuellen Datensatz, und legen Sie die **CacheStart**-Eigenschaft auf den Wert der **[Bookmark](recordset2-bookmark-property-dao.md)** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="91779-p103">The **CacheStart** property setting is the bookmark of the first record in the **Recordset** object to be cached. You can use the bookmark of any record to set the **CacheStart** property. Make the record you want to start the cache the current record, and set the **CacheStart** property equal to the **[Bookmark](recordset2-bookmark-property-dao.md)** property.</span></span>

<span data-ttu-id="91779-118">Das Microsoft Access-Datenbankmodul fordert Datensätze innerhalb des Cachebereichs aus dem Cache an, und es fordert Datensätze außerhalb des Cachebereichs vom Server an.</span><span class="sxs-lookup"><span data-stu-id="91779-118">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="91779-119">Aus dem Zwischenspeicher abgerufene Datensätze spiegeln die Änderungen, die gleichzeitig von anderen Benutzern vorgenommen wurden, nicht wider.</span><span class="sxs-lookup"><span data-stu-id="91779-119">Records retrieved from the cache don't reflect changes made concurrently to the source data by other users.</span></span>

<span data-ttu-id="91779-120">Sie können die Aktualisierung aller Daten im Zwischenspeicher erzwingen, indem Sie die **CacheSize**-Eigenschaft des **Recordset**-Objekts auf 0 und dann zurück auf die ursprünglich angeforderte Zwischenspeichergröße setzen. Anschließend verwenden Sie die **FillCache**-Methode.</span><span class="sxs-lookup"><span data-stu-id="91779-120">To force an update of all the cached data, set the **CacheSize** property of the **Recordset** object to 0, re-set it to the size of the cache you originally requested, and then use the **FillCache** method.</span></span>

