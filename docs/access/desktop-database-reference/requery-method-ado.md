---
title: ReQuery-Methode (ADO)
TOCTitle: Requery method (ADO)
ms:assetid: 1062d907-979f-020a-b2ed-94e11c0e7d08
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248871(v=office.15)
ms:contentKeyID: 48543292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 249dc236d730cf773ec38fe5dd903cb64ca9b594
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306713"
---
# <a name="requery-method-ado"></a><span data-ttu-id="0a8b9-102">ReQuery-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="0a8b9-102">Requery method (ADO)</span></span>

<span data-ttu-id="0a8b9-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0a8b9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0a8b9-104">Die Daten in einem [Recordset](recordset-object-ado.md)-Objekt werden aktualisiert durch erneutes Ausführen der Abfrage, auf der das Objekt basiert.</span><span class="sxs-lookup"><span data-stu-id="0a8b9-104">Updates the data in a [Recordset](recordset-object-ado.md) object by re-executing the query on which the object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a8b9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a8b9-105">Syntax</span></span>

<span data-ttu-id="0a8b9-106">*Recordset*. ReQuery- *Optionen*</span><span class="sxs-lookup"><span data-stu-id="0a8b9-106">*recordset*.Requery *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="0a8b9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a8b9-107">Parameters</span></span>

|<span data-ttu-id="0a8b9-108">Name</span><span class="sxs-lookup"><span data-stu-id="0a8b9-108">Name</span></span> |<span data-ttu-id="0a8b9-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a8b9-109">Description</span></span>|
|:----|:----------|
|<span data-ttu-id="0a8b9-110">*Options*</span><span class="sxs-lookup"><span data-stu-id="0a8b9-110">*Options*</span></span> |<span data-ttu-id="0a8b9-p101">Optional. Eine Bitmaske, die die Werte [ExecuteOptionEnum](executeoptionenum.md) und [CommandTypeEnum](commandtypeenum.md) enthält, die sich auf diese Operation auswirken.</span><span class="sxs-lookup"><span data-stu-id="0a8b9-p101">Optional. A bitmask that contains [ExecuteOptionEnum](executeoptionenum.md) and [CommandTypeEnum](commandtypeenum.md) values affecting this operation.</span></span>|

> [!NOTE]
> <span data-ttu-id="0a8b9-113">Wenn *options* auf **adAsyncExecute**festgelegt ist, wird dieser Vorgang asynchron ausgeführt, und es wird ein [RecordsetChangeComplete](willchangerecordset-and-recordsetchangecomplete-events-ado.md) -Ereignis ausgegeben, wenn es beendet wird.</span><span class="sxs-lookup"><span data-stu-id="0a8b9-113">If *Options* is set to **adAsyncExecute**, this operation will execute asynchronously and a [RecordsetChangeComplete](willchangerecordset-and-recordsetchangecomplete-events-ado.md) event will be issued when it concludes.</span></span>

<span data-ttu-id="0a8b9-114">Die **ExecuteOpenEnum**-Werte von **adExecuteNoRecords** oder **adExecuteStream** sollten nicht mit **Requery** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0a8b9-114">The **ExecuteOpenEnum** values of **adExecuteNoRecords** or **adExecuteStream** should not be used with **Requery**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a8b9-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0a8b9-115">Remarks</span></span>

<span data-ttu-id="0a8b9-p102">Verwenden Sie die **Requery**-Methode zum Aktualisieren des gesamten Inhalts eines **Recordset**-Objekts über die Datenquelle, indem Sie den ursprünglichen Befehl erneut ausgeben und die Daten ein zweites Mal abrufen. Das Aufrufen dieser Methode entspricht dem aufeinander folgenden Aufrufen der Methoden [Close](close-method-ado.md) und [Open](open-method-ado-recordset.md). Wenn Sie den aktuellen Datensatz bearbeiten oder einen neuen Datensatz hinzufügen, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="0a8b9-p102">Use the **Requery** method to refresh the entire contents of a **Recordset** object from the data source by reissuing the original command and retrieving the data a second time. Calling this method is equivalent to calling the [Close](close-method-ado.md) and [Open](open-method-ado-recordset.md) methods in succession. If you are editing the current record or adding a new record, an error occurs.</span></span>

<span data-ttu-id="0a8b9-p103">Während das **Recordset**-Objekt geöffnet ist, sind die Eigenschaften, durch die der Cursor ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md) usw.) definiert wird, schreibgeschützt. Daher kann durch die **Requery**-Methode nur der aktuelle Cursor aktualisiert werden. Zum Ändern der Cursoreigenschaften und zum Anzeigen der Ergebnisse müssen Sie die [Close](close-method-ado.md)-Methode verwenden, damit wieder der Lese- und Schreibzugriff auf die Eigenschaften möglich ist. Dann können Sie die Eigenschaftseinstellungen ändern und die [Open](open-method-ado-recordset.md)-Methode aufrufen, um den Cursor erneut zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0a8b9-p103">While the **Recordset** object is open, the properties that define the nature of the cursor ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md), and so forth) are read-only. Thus, the **Requery** method can only refresh the current cursor. To change any of the cursor properties and view the results, you must use the [Close](close-method-ado.md) method so that the properties become read/write again. You can then change the property settings and call the [Open](open-method-ado-recordset.md) method to reopen the cursor.</span></span>

