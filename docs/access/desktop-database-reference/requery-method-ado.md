---
title: Requery-Methode (ADO)
TOCTitle: Requery method (ADO)
ms:assetid: 1062d907-979f-020a-b2ed-94e11c0e7d08
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248871(v=office.15)
ms:contentKeyID: 48543292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 588f99d495716ca3c40376ce323d7c1557da9319
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925800"
---
# <a name="requery-method-ado"></a><span data-ttu-id="1f7ed-102">Requery-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="1f7ed-102">Requery method (ADO)</span></span>


<span data-ttu-id="1f7ed-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f7ed-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="1f7ed-104">Die Daten in einem [Recordset](recordset-object-ado.md)-Objekt werden aktualisiert durch erneutes Ausführen der Abfrage, auf der das Objekt basiert.</span><span class="sxs-lookup"><span data-stu-id="1f7ed-104">Updates the data in a [Recordset](recordset-object-ado.md) object by re-executing the query on which the object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f7ed-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f7ed-105">Syntax</span></span>

<span data-ttu-id="1f7ed-106">*Recordset-Objekt*. AktualisierenDaten- *Optionen*</span><span class="sxs-lookup"><span data-stu-id="1f7ed-106">*recordset*.Requery *Options*</span></span>

## <a name="parameter"></a><span data-ttu-id="1f7ed-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f7ed-107">Parameter</span></span>

  - <span data-ttu-id="1f7ed-108">*Options*</span><span class="sxs-lookup"><span data-stu-id="1f7ed-108">*Options*</span></span>

  - <span data-ttu-id="1f7ed-p101">Optional. Eine Bitmaske, die die Werte [ExecuteOptionEnum](executeoptionenum.md) und [CommandTypeEnum](commandtypeenum.md) enthält, die sich auf diese Operation auswirken.</span><span class="sxs-lookup"><span data-stu-id="1f7ed-p101">Optional. A bitmask that contains [ExecuteOptionEnum](executeoptionenum.md) and [CommandTypeEnum](commandtypeenum.md) values affecting this operation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="1f7ed-111">Wenn <EM>Optionen</EM> auf <STRONG>AdAsyncExecute</STRONG>festgelegt ist, wird diese Operation asynchron ausgeführt wird, und ein <A href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</A> -Ereignis wird ausgegeben, wenn er abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="1f7ed-111">If <EM>Options</EM> is set to <STRONG>adAsyncExecute</STRONG>, this operation will execute asynchronously and a <A href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</A> event will be issued when it concludes.</span></span></P>



<span data-ttu-id="1f7ed-112">Die **ExecuteOpenEnum** -Werte von **adExecuteNoRecords** oder **adExecuteStream** sollten nicht mit **Requery** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1f7ed-112">The **ExecuteOpenEnum** values of **adExecuteNoRecords** or **adExecuteStream** should not be used with **Requery**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f7ed-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1f7ed-113">Remarks</span></span>

<span data-ttu-id="1f7ed-p102">Verwenden Sie die **Requery** -Methode zum Aktualisieren des gesamten Inhalts eines **Recordset** -Objekts über die Datenquelle, indem Sie den ursprünglichen Befehl erneut ausgeben und die Daten ein zweites Mal abrufen. Das Aufrufen dieser Methode entspricht dem aufeinander folgenden Aufrufen der Methoden [Close](close-method-ado.md) und [Open](open-method-ado-recordset.md). Wenn Sie den aktuellen Datensatz bearbeiten oder einen neuen Datensatz hinzufügen, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="1f7ed-p102">Use the **Requery** method to refresh the entire contents of a **Recordset** object from the data source by reissuing the original command and retrieving the data a second time. Calling this method is equivalent to calling the [Close](close-method-ado.md) and [Open](open-method-ado-recordset.md) methods in succession. If you are editing the current record or adding a new record, an error occurs.</span></span>

<span data-ttu-id="1f7ed-p103">Während das **Recordset**-Objekt geöffnet ist, sind die Eigenschaften, durch die der Cursor ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md) usw.) definiert wird, schreibgeschützt. Daher kann durch die **Requery**-Methode nur der aktuelle Cursor aktualisiert werden. Zum Ändern der Cursoreigenschaften und zum Anzeigen der Ergebnisse müssen Sie die [Close](close-method-ado.md)-Methode verwenden, damit wieder der Lese- und Schreibzugriff auf die Eigenschaften möglich ist. Dann können Sie die Eigenschaftseinstellungen ändern und die [Open](open-method-ado-recordset.md)-Methode aufrufen, um den Cursor erneut zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1f7ed-p103">While the **Recordset** object is open, the properties that define the nature of the cursor ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md), and so forth) are read-only. Thus, the **Requery** method can only refresh the current cursor. To change any of the cursor properties and view the results, you must use the [Close](close-method-ado.md) method so that the properties become read/write again. You can then change the property settings and call the [Open](open-method-ado-recordset.md) method to reopen the cursor.</span></span>

