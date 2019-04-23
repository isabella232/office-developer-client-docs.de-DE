---
title: MoveRecord-Methode (ADO)
TOCTitle: MoveRecord method (ADO)
ms:assetid: efc341a2-0e08-a838-5925-8d4c46377e48
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250217(v=office.15)
ms:contentKeyID: 48548588
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c9937f0ab32c5dba0e4435fdc0ba7e111f5651dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288679"
---
# <a name="moverecord-method-ado"></a><span data-ttu-id="64734-102">MoveRecord-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="64734-102">MoveRecord method (ADO)</span></span>

<span data-ttu-id="64734-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="64734-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="64734-104">Verschiebt die durch einen [Record](record-object-ado.md) dargestellte Entität an einen anderen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="64734-104">Moves the entity represent by a [Record](record-object-ado.md) to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="64734-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="64734-105">Syntax</span></span>

<span data-ttu-id="64734-106">*Record*. MoveRecord (*Quelle*, *Ziel*, *Benutzername*, *Kennwort*, *Optionen*, *Async*)</span><span class="sxs-lookup"><span data-stu-id="64734-106">*Record*.MoveRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="64734-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="64734-107">Parameters</span></span>

|<span data-ttu-id="64734-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="64734-108">Parameter</span></span>|<span data-ttu-id="64734-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64734-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="64734-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="64734-110">*Source*</span></span> |<span data-ttu-id="64734-p101">Optional. Ein **String**-Wert mit einer URL, die den zu verschiebenden **Record** identifiziert. Wenn *Source* nicht angegeben ist oder eine leere Zeichenfolge angibt, wird das durch diesen **Record** dargestellte Objekt verschoben. Stellt **Record** beispielsweise eine Datei dar, wird der Inhalt der Datei an den durch *Destination* angegebenen Speicherort verschoben.</span><span class="sxs-lookup"><span data-stu-id="64734-p101">Optional. A **String** value that contains a URL identifying the **Record** to be moved. If *Source* is omitted or specifies an empty string, the object represented by this **Record** is moved. For example, if the **Record** represents a file, the contents of the file are moved to the location specified by *Destination*.</span></span>|
|<span data-ttu-id="64734-115">*Destination*</span><span class="sxs-lookup"><span data-stu-id="64734-115">*Destination*</span></span> |<span data-ttu-id="64734-116">Optional.</span><span class="sxs-lookup"><span data-stu-id="64734-116">Optional.</span></span> <span data-ttu-id="64734-117">Ein **String**-Wert mit einer URL, die den Speicherort angibt, an den *Source* verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="64734-117">A **String** value that contains a URL specifying the location where *Source* will be moved.</span></span>|
|<span data-ttu-id="64734-118">*UserName*</span><span class="sxs-lookup"><span data-stu-id="64734-118">*UserName*</span></span> |<span data-ttu-id="64734-119">Optional.</span><span class="sxs-lookup"><span data-stu-id="64734-119">Optional.</span></span> <span data-ttu-id="64734-120">Ein **String**-Wert mit der Benutzer-ID, die bei Bedarf Zugriff auf die *Destination* gewährt.</span><span class="sxs-lookup"><span data-stu-id="64734-120">A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>|
|<span data-ttu-id="64734-121">*Password*</span><span class="sxs-lookup"><span data-stu-id="64734-121">*Password*</span></span> |<span data-ttu-id="64734-122">Optional.</span><span class="sxs-lookup"><span data-stu-id="64734-122">Optional.</span></span> <span data-ttu-id="64734-123">Ein **String**-Wert, der das Kennwort enthält, das bei Bedarf den *UserName* bestätigt.</span><span class="sxs-lookup"><span data-stu-id="64734-123">A **String** that contains the password that, if needed, verifies *UserName*.</span></span>|
|<span data-ttu-id="64734-124">*Options*</span><span class="sxs-lookup"><span data-stu-id="64734-124">*Options*</span></span> |<span data-ttu-id="64734-p105">Optional. Ein [MoveRecordOptionsEnum](moverecordoptionsenum.md)-Wert, dessen Standardwert **adMoveUnspecified** lautet. Gibt das Verhalten dieser Methode an.</span><span class="sxs-lookup"><span data-stu-id="64734-p105">Optional. A [MoveRecordOptionsEnum](moverecordoptionsenum.md) value whose default value is **adMoveUnspecified**. Specifies the behavior of this method.</span></span>|
|<span data-ttu-id="64734-128">*Async*</span><span class="sxs-lookup"><span data-stu-id="64734-128">*Async*</span></span> |<span data-ttu-id="64734-129">Optional.</span><span class="sxs-lookup"><span data-stu-id="64734-129">Optional.</span></span> <span data-ttu-id="64734-130">Ein **boolescher** Wert, der bei **true**angibt, dass dieser Vorgang asynchron sein soll.</span><span class="sxs-lookup"><span data-stu-id="64734-130">A **Boolean** value that, when **True**, specifies this operation should be asynchronous.</span></span>|

## <a name="return-value"></a><span data-ttu-id="64734-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64734-131">Return value</span></span>

<span data-ttu-id="64734-132">Ein **String**-Wert.</span><span class="sxs-lookup"><span data-stu-id="64734-132">A **String** value.</span></span> <span data-ttu-id="64734-133">In der Regel wird der Wert für *Destination* zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="64734-133">Typically, the value of *Destination* is returned.</span></span> <span data-ttu-id="64734-134">Der genaue Wert, der zurückgegeben wird, ist jedoch vom Anbieter abhängig.</span><span class="sxs-lookup"><span data-stu-id="64734-134">However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="64734-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64734-135">Remarks</span></span>

<span data-ttu-id="64734-p108">Die Werte für *Source* und *Destination* dürfen nicht identisch sein, andernfalls tritt ein Laufzeitfehler auf. Mindestens der Server-, Pfad- und Ressourcenname müssen unterschiedlich sein.</span><span class="sxs-lookup"><span data-stu-id="64734-p108">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs. At least the server, path, and resource names must differ.</span></span>

<span data-ttu-id="64734-p109">Bei Dateien, die mithilfe des Anbieters für Internet Publishing verschoben wurden, aktualisiert diese Methode alle Hypertextlinks in den zu verschiebenden Dateien, sofern keine andere Angabe durch *Options* erfolgt ist. Diese Methode schlägt fehl, wenn *Destination* ein vorhandenes Objekt (z. B. eine Datei oder ein Verzeichnis) identifiziert. Dies gilt nicht, wenn **adMoveOverWrite** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="64734-p109">For files moved using the Internet Publishing Provider, this method updates all hypertext links in files being moved unless otherwise specified by *Options*. This method fails if *Destination* identifies an existing object (for example, a file or directory), unless **adMoveOverWrite** is specified.</span></span>

> [!NOTE]
> <span data-ttu-id="64734-p110">Verwenden Sie die Option **adMoveOverWrite** nur nach sorgfältiger Überlegung. Wenn Sie diese Option beispielsweise beim Verschieben einer Datei in ein Verzeichnis angeben, wird das Verzeichnis gelöscht und durch die Datei ersetzt.</span><span class="sxs-lookup"><span data-stu-id="64734-p110">Use the **adMoveOverWrite** option judiciously. For example, specifying this option when moving a file to a directory will delete the directory and replace it with the file.</span></span>

<span data-ttu-id="64734-p111">Bestimmte Attribute des **Record** -Objekts (z. B. die [ParentURL](parenturl-property-ado.md)-Eigenschaft) werden nicht aktualisiert, nachdem dieser Vorgang abgeschlossen ist. Aktualisieren Sie die Eigenschaften des **Record** -Objekts, indem Sie den **Record** schließen und anschließend mit der URL des Speicherorts, an den die Datei oder das Verzeichnis verschoben wurde, erneut öffnen.</span><span class="sxs-lookup"><span data-stu-id="64734-p111">Certain attributes of the **Record** object, such as the [ParentURL](parenturl-property-ado.md) property, will not be updated after this operation completes. Refresh the **Record** object's properties by closing the **Record**, then re-opening it with the URL of the location where the file or directory was moved.</span></span>

<span data-ttu-id="64734-p112">Wurde dieser **Record** aus einem [Recordset](recordset-object-ado.md)-Objekt abgerufen, wird der neue Speicherort der verschobenen Datei oder des verschobenen Verzeichnisses nicht unmittelbar im **Recordset** -Objekt wiedergegeben. Aktualisieren Sie das **Recordset** -Objekt, indem Sie es schließen und erneut öffnen.</span><span class="sxs-lookup"><span data-stu-id="64734-p112">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), the new location of the moved file or directory will not be reflected immediately in the **Recordset**. Refresh the **Recordset** by closing and re-opening it.</span></span>

> [!NOTE]
> <span data-ttu-id="64734-146">Bei URLs, die das HTTP-Schema verwenden, wird automatisch der [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="64734-146">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="64734-147">Weitere Informationen finden Sie unter [absolute und relative URLs](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="64734-147">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


