---
title: DeleteRecord-Methode (ADO)
TOCTitle: DeleteRecord Method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d850234faf18a2bd6f3278ee4feade3aa3bb561
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472831"
---
# <a name="deleterecord-method-ado"></a><span data-ttu-id="e9b44-102">DeleteRecord-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="e9b44-102">DeleteRecord Method (ADO)</span></span>


<span data-ttu-id="e9b44-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e9b44-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="e9b44-104">Löscht eine durch [Record](record-object-ado.md) dargestellte Entität.</span><span class="sxs-lookup"><span data-stu-id="e9b44-104">Deletes a the entity represented by a [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e9b44-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9b44-105">Syntax</span></span>

<span data-ttu-id="e9b44-106">*Datensatz*. \**DeleteRecord \*\*\* Quelle*, *Async*</span><span class="sxs-lookup"><span data-stu-id="e9b44-106">*Record*.\**DeleteRecord\*\*\*Source*, *Async*</span></span>

## <a name="parameters"></a><span data-ttu-id="e9b44-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9b44-107">Parameters</span></span>

  - <span data-ttu-id="e9b44-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="e9b44-108">*Source*</span></span>

  - <span data-ttu-id="e9b44-p101">Optional. Ein String-Wert mit einer URL, die die zu löschende Entität (z. B. eine Datei oder ein Verzeichnis) identifiziert. Wenn Source nicht angeben ist oder eine leere Zeichenfolge angibt, wird die durch den aktuellen Record dargestellte Entität gelöscht. Wenn es sich bei Record um einen Datensatz einer Auflistung (RecordType von adCollectionRecord, z. B. einem Verzeichnis) handelt, werden alle untergeordneten Ebenen (z. B. Unterverzeichnisse) ebenso gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e9b44-p101">Optional. A **String** value that contains a URL identifying the entity (for example, the file or directory) to be deleted. If *Source* is omitted or specifies an empty string, the entity represented by the current [Record](record-object-ado.md) is deleted. If the Record is a collection record ([RecordType](recordtype-property-ado.md) of **adCollectionRecord**, such as a directory) all children (for example, subdirectories) will also be deleted.</span></span>

  - <span data-ttu-id="e9b44-113">*Async*</span><span class="sxs-lookup"><span data-stu-id="e9b44-113">*Async*</span></span>

  - <span data-ttu-id="e9b44-p102">Optional. Ein **Boolean** -Wert, der im Fall von **True** angibt, dass der Löschvorgang asynchron ist.</span><span class="sxs-lookup"><span data-stu-id="e9b44-p102">Optional. A **Boolean** value that, when **True**, specifies that the delete operation is asynchronous.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9b44-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e9b44-116">Remarks</span></span>

<span data-ttu-id="e9b44-p103">Vorgänge in Bezug auf das durch diesen **Record** dargestellte Objekt schlagen möglicherweise fehl, nachdem das Ausführen dieser Methode beendet wurde. Nach dem Aufrufen von **DeleteRecord** sollte **Record** geschlossen werden, da das Verhalten von **Record** in Abhängigkeit davon, wann der Anbieter den **Record** mit der Datenquelle aktualisiert, möglicherweise unvorhersehbar wird.</span><span class="sxs-lookup"><span data-stu-id="e9b44-p103">Operations on the object represented by this **Record** may fail after this method completes. After calling **DeleteRecord**, the **Record** should be closed because the behavior of the **Record** may become unpredictable depending upon when the provider updates the **Record** with the data source.</span></span>

<span data-ttu-id="e9b44-119">Wurde dieser **Record** aus einem [Recordset](recordset-object-ado.md)-Objekt abgerufen, werden die Ergebnisse dieses Vorgangs nicht unmittelbar im **Recordset** -Objekt wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="e9b44-119">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), then the results of this operation will not be reflected immediately in the **Recordset**.</span></span> <span data-ttu-id="e9b44-120">Aktualisieren Sie das **Recordset** , indem schließen und erneut öffnen, oder durch Ausführen der **Recordset** [erneut abzufragen](requery-method-ado.md), oder [Update](update-method-ado.md) und [Resync](resync-method-ado.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="e9b44-120">Refresh the **Recordset** by closing and re-opening it, or by executing the **Recordset** [Requery](requery-method-ado.md), or [Update](update-method-ado.md) and [Resync](resync-method-ado.md) methods.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e9b44-p105">[!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird der <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider für Internet Publishing</A> automatisch aufgerufen. Weitere Informationen erhalten Sie unter <A href="absolute-and-relative-urls.md">Absolute und relative URLs</A>.</span><span class="sxs-lookup"><span data-stu-id="e9b44-p105">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>


