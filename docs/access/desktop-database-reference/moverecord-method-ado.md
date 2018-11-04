---
title: MoveRecord-Methode (ADO)
TOCTitle: MoveRecord method (ADO)
ms:assetid: efc341a2-0e08-a838-5925-8d4c46377e48
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250217(v=office.15)
ms:contentKeyID: 48548588
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 296232b05041c1e059b5134fdde11fceac4e3d43
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949894"
---
# <a name="moverecord-method-ado"></a><span data-ttu-id="75b12-102">MoveRecord-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="75b12-102">MoveRecord method (ADO)</span></span>

<span data-ttu-id="75b12-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="75b12-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="75b12-104">Verschiebt die durch einen [Record](record-object-ado.md) dargestellte Entität an einen anderen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="75b12-104">Moves the entity represent by a [Record](record-object-ado.md) to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="75b12-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="75b12-105">Syntax</span></span>

<span data-ttu-id="75b12-106">*Datensatz*. MoveRecord (*Quelle*, *Ziel*, *Benutzername*, *Kennwort*, *Optionen*, *Async*)</span><span class="sxs-lookup"><span data-stu-id="75b12-106">*Record*.MoveRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="75b12-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="75b12-107">Parameters</span></span>

|<span data-ttu-id="75b12-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="75b12-108">Parameter</span></span>|<span data-ttu-id="75b12-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75b12-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="75b12-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="75b12-110">*Source*</span></span> |<span data-ttu-id="75b12-p101">Optional. Ein **String**-Wert mit einer URL, die den zu verschiebenden **Record** identifiziert. Wenn *Source* nicht angegeben ist oder eine leere Zeichenfolge angibt, wird das durch diesen **Record** dargestellte Objekt verschoben. Stellt **Record** beispielsweise eine Datei dar, wird der Inhalt der Datei an den durch *Destination* angegebenen Speicherort verschoben.</span><span class="sxs-lookup"><span data-stu-id="75b12-p101">Optional. A **String** value that contains a URL identifying the **Record** to be moved. If *Source* is omitted or specifies an empty string, the object represented by this **Record** is moved. For example, if the **Record** represents a file, the contents of the file are moved to the location specified by *Destination*.</span></span>|
|<span data-ttu-id="75b12-115">*Destination*</span><span class="sxs-lookup"><span data-stu-id="75b12-115">*Destination*</span></span> |<span data-ttu-id="75b12-116">Optional.</span><span class="sxs-lookup"><span data-stu-id="75b12-116">Optional.</span></span> <span data-ttu-id="75b12-117">Ein **String** -Wert, der enthält eine URL des Speicherorts, in dem *Quelle* verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="75b12-117">A **String** value that contains a URL specifying the location where *Source* will be moved.</span></span>|
|<span data-ttu-id="75b12-118">*UserName*</span><span class="sxs-lookup"><span data-stu-id="75b12-118">*UserName*</span></span> |<span data-ttu-id="75b12-p103">Optional. Ein **String**-Wert mit der Benutzer-ID, die bei Bedarf Zugriff auf die *Destination* gewährt.</span><span class="sxs-lookup"><span data-stu-id="75b12-p103">Optional. A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>|
|<span data-ttu-id="75b12-121">*Password*</span><span class="sxs-lookup"><span data-stu-id="75b12-121">*Password*</span></span> |<span data-ttu-id="75b12-p104">Optional. Ein **String**-Wert, der das Kennwort enthält, das bei Bedarf den *UserName* bestätigt.</span><span class="sxs-lookup"><span data-stu-id="75b12-p104">Optional. A **String** that contains the password that, if needed, verifies *UserName*.</span></span>|
|<span data-ttu-id="75b12-124">*Options*</span><span class="sxs-lookup"><span data-stu-id="75b12-124">*Options*</span></span> |<span data-ttu-id="75b12-p105">Optional. Ein [MoveRecordOptionsEnum](moverecordoptionsenum.md)-Wert, dessen Standardwert **adMoveUnspecified** lautet. Gibt das Verhalten dieser Methode an.</span><span class="sxs-lookup"><span data-stu-id="75b12-p105">Optional. A [MoveRecordOptionsEnum](moverecordoptionsenum.md) value whose default value is **adMoveUnspecified**. Specifies the behavior of this method.</span></span>|
|<span data-ttu-id="75b12-128">*Async*</span><span class="sxs-lookup"><span data-stu-id="75b12-128">*Async*</span></span> |<span data-ttu-id="75b12-129">Optional.</span><span class="sxs-lookup"><span data-stu-id="75b12-129">Optional.</span></span> <span data-ttu-id="75b12-130">**Boolean** -Wert, der im Wenn **True**, gibt an, dass diese Operation asynchron sein sollte.</span><span class="sxs-lookup"><span data-stu-id="75b12-130">A **Boolean** value that, when **True**, specifies this operation should be asynchronous.</span></span>|

## <a name="return-value"></a><span data-ttu-id="75b12-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75b12-131">Return value</span></span>

<span data-ttu-id="75b12-132">Ein **String** -Wert.</span><span class="sxs-lookup"><span data-stu-id="75b12-132">A **String** value.</span></span> <span data-ttu-id="75b12-133">In der Regel wird der Wert des *Ziels* zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="75b12-133">Typically, the value of *Destination* is returned.</span></span> <span data-ttu-id="75b12-134">Der genaue Wert, der zurückgegeben wird, ist jedoch vom Anbieter abhängig.</span><span class="sxs-lookup"><span data-stu-id="75b12-134">However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="75b12-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="75b12-135">Remarks</span></span>

<span data-ttu-id="75b12-136">Die Werte der *Quell-* und *Zielserver* dürfen nicht identisch sein; andernfalls tritt ein Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="75b12-136">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="75b12-137">Mindestens der Server-, Pfad- und Ressourcenname müssen unterschiedlich sein.</span><span class="sxs-lookup"><span data-stu-id="75b12-137">At least the server, path, and resource names must differ.</span></span>

<span data-ttu-id="75b12-p109">Bei Dateien, die mithilfe des Anbieters für Internet Publishing verschoben wurden, aktualisiert diese Methode alle Hypertextlinks in den zu verschiebenden Dateien, sofern keine andere Angabe durch *Options* erfolgt ist. Diese Methode schlägt fehl, wenn *Destination* ein vorhandenes Objekt (z. B. eine Datei oder ein Verzeichnis) identifiziert. Dies gilt nicht, wenn **adMoveOverWrite** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="75b12-p109">For files moved using the Internet Publishing Provider, this method updates all hypertext links in files being moved unless otherwise specified by *Options*. This method fails if *Destination* identifies an existing object (for example, a file or directory), unless **adMoveOverWrite** is specified.</span></span>


> [!NOTE]
> <P><span data-ttu-id="75b12-p110">[!HINWEIS] Verwenden Sie die Option <STRONG>adMoveOverWrite</STRONG> nur nach sorgfältiger Überlegung. Wenn Sie diese Option beispielsweise beim Verschieben einer Datei in ein Verzeichnis angeben, wird das Verzeichnis gelöscht und durch die Datei ersetzt.</span><span class="sxs-lookup"><span data-stu-id="75b12-p110">Use the <STRONG>adMoveOverWrite</STRONG> option judiciously. For example, specifying this option when moving a file to a directory will delete the directory and replace it with the file.</span></span></P>



<span data-ttu-id="75b12-p111">Bestimmte Attribute des **Record** -Objekts (z. B. die [ParentURL](parenturl-property-ado.md)-Eigenschaft) werden nicht aktualisiert, nachdem dieser Vorgang abgeschlossen ist. Aktualisieren Sie die Eigenschaften des **Record** -Objekts, indem Sie den **Record** schließen und anschließend mit der URL des Speicherorts, an den die Datei oder das Verzeichnis verschoben wurde, erneut öffnen.</span><span class="sxs-lookup"><span data-stu-id="75b12-p111">Certain attributes of the **Record** object, such as the [ParentURL](parenturl-property-ado.md) property, will not be updated after this operation completes. Refresh the **Record** object's properties by closing the **Record**, then re-opening it with the URL of the location where the file or directory was moved.</span></span>

<span data-ttu-id="75b12-p112">Wurde dieser **Record** aus einem [Recordset](recordset-object-ado.md)-Objekt abgerufen, wird der neue Speicherort der verschobenen Datei oder des verschobenen Verzeichnisses nicht unmittelbar im **Recordset** -Objekt wiedergegeben. Aktualisieren Sie das **Recordset** -Objekt, indem Sie es schließen und erneut öffnen.</span><span class="sxs-lookup"><span data-stu-id="75b12-p112">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), the new location of the moved file or directory will not be reflected immediately in the **Recordset**. Refresh the **Recordset** by closing and re-opening it.</span></span>


> [!NOTE]
> <span data-ttu-id="75b12-146">[!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird der [Microsoft OLE DB Provider für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) automatisch aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="75b12-146">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="75b12-147">Weitere Informationen finden Sie unter [Absolute und relative URLs](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="75b12-147">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


