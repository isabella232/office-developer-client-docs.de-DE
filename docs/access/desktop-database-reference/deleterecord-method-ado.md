---
title: DeleteRecord-Methode (ADO)
TOCTitle: DeleteRecord method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8d6ecd408bc2141ef9ff4bec8f6469a70e09bbe1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293994"
---
# <a name="deleterecord-method-ado"></a><span data-ttu-id="ee9e6-102">DeleteRecord-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="ee9e6-102">DeleteRecord method (ADO)</span></span>

<span data-ttu-id="ee9e6-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee9e6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ee9e6-104">Löscht eine durch [Record](record-object-ado.md) dargestellte Entität.</span><span class="sxs-lookup"><span data-stu-id="ee9e6-104">Deletes a the entity represented by a [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ee9e6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee9e6-105">Syntax</span></span>

<span data-ttu-id="ee9e6-106">*Record*. \**DeleteRecord \* \* \* Quelle*, *Async*</span><span class="sxs-lookup"><span data-stu-id="ee9e6-106">*Record*.\**DeleteRecord\*\*\*Source*, *Async*</span></span>

## <a name="parameters"></a><span data-ttu-id="ee9e6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee9e6-107">Parameters</span></span>

|<span data-ttu-id="ee9e6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee9e6-108">Parameter</span></span>|<span data-ttu-id="ee9e6-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee9e6-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ee9e6-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="ee9e6-110">*Source*</span></span> |<span data-ttu-id="ee9e6-111">Optional.</span><span class="sxs-lookup"><span data-stu-id="ee9e6-111">Optional.</span></span> <span data-ttu-id="ee9e6-112">A **String** value that contains a URL identifying the entity (for example, the file or directory) to be deleted.</span><span class="sxs-lookup"><span data-stu-id="ee9e6-112">A **String** value that contains a URL identifying the entity (for example, the file or directory) to be deleted.</span></span> <span data-ttu-id="ee9e6-113">Wenn *Source* nicht angegeben wird oder eine leere Zeichenfolge angibt, wird die vom aktuellen [Datensatz](record-object-ado.md) dargestellte Entität gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ee9e6-113">If *Source* is omitted or specifies an empty string, the entity represented by the current [Record](record-object-ado.md) is deleted.</span></span> <span data-ttu-id="ee9e6-114">Wenn es sich bei dem Datensatz um einen[](recordtype-property-ado.md) Auflistungs Daten Satz handelt (RecordType of **adCollectionRecord**, beispielsweise ein Verzeichnis), werden auch alle untergeordneten Elemente (beispielsweise Unterverzeichnisse) gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ee9e6-114">If the Record is a collection record ([RecordType](recordtype-property-ado.md) of **adCollectionRecord**, such as a directory) all children (for example, subdirectories) will also be deleted.</span></span>|
|<span data-ttu-id="ee9e6-115">*Async*</span><span class="sxs-lookup"><span data-stu-id="ee9e6-115">*Async*</span></span> |<span data-ttu-id="ee9e6-p102">Optional. Ein **Boolean** -Wert, der im Fall von **True** angibt, dass der Löschvorgang asynchron ist.</span><span class="sxs-lookup"><span data-stu-id="ee9e6-p102">Optional. A **Boolean** value that, when **True**, specifies that the delete operation is asynchronous.</span></span>|

## <a name="remarks"></a><span data-ttu-id="ee9e6-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee9e6-118">Remarks</span></span>

<span data-ttu-id="ee9e6-p103">Vorgänge in Bezug auf das durch diesen **Record** dargestellte Objekt schlagen möglicherweise fehl, nachdem das Ausführen dieser Methode beendet wurde. Nach dem Aufrufen von **DeleteRecord** sollte **Record** geschlossen werden, da das Verhalten von **Record** in Abhängigkeit davon, wann der Anbieter den **Record** mit der Datenquelle aktualisiert, möglicherweise unvorhersehbar wird.</span><span class="sxs-lookup"><span data-stu-id="ee9e6-p103">Operations on the object represented by this **Record** may fail after this method completes. After calling **DeleteRecord**, the **Record** should be closed because the behavior of the **Record** may become unpredictable depending upon when the provider updates the **Record** with the data source.</span></span>

<span data-ttu-id="ee9e6-121">Wurde dieser **Record** aus einem [Recordset](recordset-object-ado.md)-Objekt abgerufen, werden die Ergebnisse dieses Vorgangs nicht unmittelbar im **Recordset** -Objekt wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="ee9e6-121">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), then the results of this operation will not be reflected immediately in the **Recordset**.</span></span> <span data-ttu-id="ee9e6-122">Aktualisieren Sie das **Recordset** -Objekt, indem Sie es schließen und erneut öffnen, oder indem Sie die **Recordset** [Requery](requery-method-ado.md)-oder [Update](update-method-ado.md) -und Resync-Methoden ausführen. [](resync-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="ee9e6-122">Refresh the **Recordset** by closing and re-opening it, or by executing the **Recordset** [Requery](requery-method-ado.md), or [Update](update-method-ado.md) and [Resync](resync-method-ado.md) methods.</span></span>

> [!NOTE]
> <span data-ttu-id="ee9e6-123">Bei URLs, die das HTTP-Schema verwenden, wird automatisch der [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ee9e6-123">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="ee9e6-124">Weitere Informationen finden Sie unter [absolute und relative URLs](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="ee9e6-124">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


