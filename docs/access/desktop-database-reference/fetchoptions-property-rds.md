---
title: FetchOptions-Eigenschaft (RDS)
TOCTitle: FetchOptions Property (RDS)
ms:assetid: 0d86c5e4-9abc-5c0e-dc04-4183f4c278cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248856(v=office.15)
ms:contentKeyID: 48543221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3e7251ba50b003b37cdeb0dd70fe4a98821d4c9
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861932"
---
# <a name="fetchoptions-property-rds"></a><span data-ttu-id="062a7-102">FetchOptions-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="062a7-102">FetchOptions Property (RDS)</span></span>


<span data-ttu-id="062a7-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="062a7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="062a7-104">Gibt den Typ für asynchrone Abrufvorgänge an.</span><span class="sxs-lookup"><span data-stu-id="062a7-104">Indicates the type of asynchronous fetching.</span></span>

## <a name="setting-and-return-values"></a><span data-ttu-id="062a7-105">Einstellung und Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="062a7-105">Setting and Return Values</span></span>

<span data-ttu-id="062a7-106">Legt einen der folgenden Werte fest oder gibt ihn zurück.</span><span class="sxs-lookup"><span data-stu-id="062a7-106">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="062a7-107">Konstante</span><span class="sxs-lookup"><span data-stu-id="062a7-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="062a7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="062a7-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="062a7-109"><strong>adcFetchUpFront</strong></span><span class="sxs-lookup"><span data-stu-id="062a7-109"><strong>adcFetchUpFront</strong></span></span></p></td>
<td><p><span data-ttu-id="062a7-p101">Alle Datensätze des <a href="recordset-object-ado.md">Recordsets</a> werden abgerufen, bevor die Steuerung an die Anwendung zurückgeht. Erst nachdem das vollständige <strong>Recordset</strong>-Objekt abgerufen wurde, kann es durch die Anwendung bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="062a7-p101">All the records of the <a href="recordset-object-ado.md">Recordset</a> are fetched before control is returned to the application. The complete <strong>Recordset</strong> is fetched before the application is allowed to do anything with it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="062a7-112"><strong>adcFetchBackground</strong></span><span class="sxs-lookup"><span data-stu-id="062a7-112"><strong>adcFetchBackground</strong></span></span></p></td>
<td><p><span data-ttu-id="062a7-p102">Nachdem der erste Datensatzbatch abgerufen wurde, kann die Steuerung wieder an die Anwendung zurückgehen. Ein anschließender Lesevorgang des <strong>Recordsets</strong>, bei dem versucht wird, auf einen im ersten Batch noch nicht abgerufenen Datensatz zuzugreifen, wird verzögert, bis der gesuchte Datensatz tatsächlich abgerufen wurde. Dann geht die Steuerung wieder an die Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="062a7-p102">Control can return to the application as soon as the first batch of records has been fetched. A subsequent read of the <strong>Recordset</strong> that attempts to access a record not fetched in the first batch will be delayed until the sought record is actually fetched, at which time control returns to the application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="062a7-115"><strong>adcFetchAsync</strong></span><span class="sxs-lookup"><span data-stu-id="062a7-115"><strong>adcFetchAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="062a7-p103">Standard. Die Steuerung geht sofort an die Anwendung zurück, während Datensätze im Hintergrund abgerufen werden. Wenn von der Anwendung versucht wird, einen Datensatz zu lesen, der noch nicht abgerufen wurde, wird der Datensatz gelesen, der dem gesuchten Datensatz am nächsten liegt. Dabei geht die Steuerung sofort an die Anwendung zurück, und es wird angegeben, dass das aktuelle Ende des <strong>Recordsets</strong> erreicht ist. Beispielsweise wird bei einem Aufruf von <a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveLast</a> die aktuelle Datensatzposition zum tatsächlich zuletzt abgerufenen Datensatz verschoben, auch wenn das <strong>Recordset</strong>-Objekt mit weiteren Datensätzen gefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="062a7-p103">Default. Control returns immediately to the application while records are fetched in the background. If the application attempts to read a record that hasn't yet been fetched, the record closest to the sought record will be read and control will return immediately, indicating that the current end of the <strong>Recordset</strong> has been reached. For example, a call to <a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveLast</a> will move the current record position to the last record actually fetched, even though more records will continue to populate the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="062a7-120">Jede mithilfe der clientseitigen ausführbare Datei, die die folgenden Konstanten verwendet, muss Deklarationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="062a7-120">Each client-side executable file that uses these constants must provide declarations for them.</span></span> <span data-ttu-id="062a7-121">Sie können Ausschneiden und Einfügen aus der Datei Datei Adcvbs.inc, befindet sich im Ordner C:\Program Files\Common Dateien\System\MSADC gewünschten Konstantendeklarationen.</span><span class="sxs-lookup"><span data-stu-id="062a7-121">You can cut and paste the constant declarations you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span>



## <a name="remarks"></a><span data-ttu-id="062a7-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="062a7-122">Remarks</span></span>

<span data-ttu-id="062a7-123"><<<<<<< HEAD In a Web Application, Sie werden in der Regel **AdcFetchAsync** (Standardwert) verwenden möchten, da es sich um eine bessere Leistung bietet.</span><span class="sxs-lookup"><span data-stu-id="062a7-123"><<<<<<< HEAD In a Web application, you will usually want to use **adcFetchAsync** (the default value), because it provides better performance.</span></span> <span data-ttu-id="062a7-124">In einer kompilierten Clientanwendung wird meist **adcFetchBackground** verwendet.</span><span class="sxs-lookup"><span data-stu-id="062a7-124">In a compiled client application, you will usually want to use **adcFetchBackground**.</span></span>
<span data-ttu-id="062a7-125">=== In einer Webanwendung werden Sie in der Regel **AdcFetchAsync** (Standardwert) verwenden möchten, da es sich um eine bessere Leistung bietet.</span><span class="sxs-lookup"><span data-stu-id="062a7-125">======= In a web application, you will usually want to use **adcFetchAsync** (the default value), because it provides better performance.</span></span> <span data-ttu-id="062a7-126">In einer kompilierten Clientanwendung wird meist **adcFetchBackground** verwendet.</span><span class="sxs-lookup"><span data-stu-id="062a7-126">In a compiled client application, you will usually want to use **adcFetchBackground**.</span></span>
>>>>>>> <span data-ttu-id="062a7-127">master</span><span class="sxs-lookup"><span data-stu-id="062a7-127">master</span></span>

