---
title: Open-Methode (ADO-Record)
TOCTitle: Open Method (ADO Record)
ms:assetid: ba71c5c7-326e-d3b6-0e74-e8343ee6896f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249896(v=office.15)
ms:contentKeyID: 48547371
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f29f707f02ed8adbf2b1881b0721ce912b278353
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605828"
---
# <a name="open-method-ado-record"></a><span data-ttu-id="8a3b5-102">Open-Methode (ADO-Record)</span><span class="sxs-lookup"><span data-stu-id="8a3b5-102">Open Method (ADO Record)</span></span>


<span data-ttu-id="8a3b5-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8a3b5-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="8a3b5-104">Öffnet ein vorhandenes [Record](record-object-ado.md)-Objekt oder erstellt ein neues durch den **Record** dargestelltes Element (z. B. eine Datei oder ein Verzeichnis).</span><span class="sxs-lookup"><span data-stu-id="8a3b5-104">Opens an existing [Record](record-object-ado.md) object, or creates a new item represented by the **Record** (such as a file or directory).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a3b5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a3b5-105">Syntax</span></span>

<span data-ttu-id="8a3b5-106">Öffnen Sie *Source*, *ActiveConnection*, *Modus*, *CreateOptions*, *Optionen*, *Benutzername*, *Kennwort*</span><span class="sxs-lookup"><span data-stu-id="8a3b5-106">Open *Source*, *ActiveConnection*, *Mode*, *CreateOptions*, *Options*, *UserName*, *Password*</span></span>

## <a name="parameters"></a><span data-ttu-id="8a3b5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a3b5-107">Parameters</span></span>

  - <span data-ttu-id="8a3b5-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="8a3b5-108">*Source*</span></span>

  - <span data-ttu-id="8a3b5-p101">Optional. Ein **Variant** -Wert, der Folgendes darstellt: die URL der durch dieses **Record** -Objekt darzustellenden Entität, einen **Command**, ein offenes [Recordset](recordset-object-ado.md)-Objekt oder ein anderes **Record** -Objekt, eine Zeichenfolge mit einer SQL SELECT-Anweisung oder einen Tabellennamen.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-p101">Optional. A **Variant** that may represent the URL of the entity to be represented by this **Record** object, a **Command**, an open [Recordset](recordset-object-ado.md) or another **Record** object, a string containing a SQL SELECT statement or a table name.</span></span>

  - <span data-ttu-id="8a3b5-111">*ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="8a3b5-111">*ActiveConnection*</span></span>

  - <span data-ttu-id="8a3b5-p102">Optional. Ein **Variant** -Wert, der die Verbindungszeichenfolge oder das offene [Connection](connection-object-ado.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-p102">Optional. A **Variant** that represents the connect string or open [Connection](connection-object-ado.md) object.</span></span>

  - <span data-ttu-id="8a3b5-114">*Mode*</span><span class="sxs-lookup"><span data-stu-id="8a3b5-114">*Mode*</span></span>

  - <span data-ttu-id="8a3b5-p103">Optional. Ein [ConnectModeEnum](connectmodeenum.md)-Wert, dessen Standardwert **adModeUnknown** ist und der den Zugriffsmodus für das resultierende **Record** -Objekt angibt.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-p103">Optional. A [ConnectModeEnum](connectmodeenum.md) value, whose default value is **adModeUnknown**, that specifies the access mode for the resultant **Record** object.</span></span>

  - <span data-ttu-id="8a3b5-117">*CreateOptions*</span><span class="sxs-lookup"><span data-stu-id="8a3b5-117">*CreateOptions*</span></span>

  - <span data-ttu-id="8a3b5-118">Optional.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-118">Optional.</span></span> <span data-ttu-id="8a3b5-119">Ein [RecordCreateOptionsEnum](recordcreateoptionsenum.md) -Wert, dessen Standardwert **AdFailIfNotExists**,, der angibt ist, ob eine vorhandene Datei oder ein Verzeichnis geöffnet werden soll, oder eine neue Datei oder ein Verzeichnis sollte erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-119">A [RecordCreateOptionsEnum](recordcreateoptionsenum.md) value, whose default value is **adFailIfNotExists**, that specifies whether an existing file or directory should be opened, or a new file or directory should be created.</span></span> <span data-ttu-id="8a3b5-120">Wenn die [Mode](mode-property-ado.md) -Eigenschaft auf den Standardwert der Zugriffsmodus Set abgerufen.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-120">If set to the default value, the access mode is obtained from the [Mode](mode-property-ado.md) property.</span></span> <span data-ttu-id="8a3b5-121">Dieser Parameter wird ignoriert, wenn der *Source* -Parameter keine URL enthält.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-121">This parameter is ignored when the *Source* parameter doesnt contain a URL.</span></span>

  - <span data-ttu-id="8a3b5-122">*Options*</span><span class="sxs-lookup"><span data-stu-id="8a3b5-122">*Options*</span></span>

  - <span data-ttu-id="8a3b5-p105">Optional. Ein [RecordOpenOptionsEnum](recordopenoptionsenum.md)-Wert, dessen Standardwert **adOpenRecordUnspecified** lautet und der Optionen zum Öffnen des **Record** angibt. Diese Werte können kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-p105">Optional. A [RecordOpenOptionsEnum](recordopenoptionsenum.md) value, whose default value is **adOpenRecordUnspecified**, that specifies options for opening the **Record**. These values may be combined.</span></span>

  - <span data-ttu-id="8a3b5-126">*UserName*</span><span class="sxs-lookup"><span data-stu-id="8a3b5-126">*UserName*</span></span>

  - <span data-ttu-id="8a3b5-p106">Optional. Ein **String**-Wert mit der Benutzer-ID, die bei Bedarf Zugriff auf die *Source* gewährt.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-p106">Optional. A **String** value that contains the user ID that, if needed, authorizes access to *Source*.</span></span>

  - <span data-ttu-id="8a3b5-129">*Password*</span><span class="sxs-lookup"><span data-stu-id="8a3b5-129">*Password*</span></span>

  - <span data-ttu-id="8a3b5-p107">Optional. Ein **String**-Wert, der das Kennwort enthält, das bei Bedarf den *UserName* bestätigt.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-p107">Optional. A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a3b5-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8a3b5-132">Remarks</span></span>

<span data-ttu-id="8a3b5-133">*Quelle* kann sein:</span><span class="sxs-lookup"><span data-stu-id="8a3b5-133">*Source* may be:</span></span>

  - <span data-ttu-id="8a3b5-134">Eine URL.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-134">A URL.</span></span> <span data-ttu-id="8a3b5-135">Wenn das Protokoll für die URL http festgelegt ist, wird standardmäßig der Internetanbieter aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-135">If the protocol for the URL is http, then the Internet Provider will be invoked by default.</span></span> <span data-ttu-id="8a3b5-136">Wenn die URL auf einen Knoten verweist, die ein ausführbares Skript enthält (z. B. ein. ASP-Seite), und klicken Sie dann einen **Datensatz** , der die Quelle statt der ausgeführten Inhalt enthält standardmäßig geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-136">If the URL points to a node that contains an executable script (such as an .ASP page), then a **Record** containing the source rather than the executed contents is opened by default.</span></span> <span data-ttu-id="8a3b5-137">Verwenden Sie das Argument *Options* , um dieses Verhalten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-137">Use the *Options* argument to modify this behavior.</span></span>

  - <span data-ttu-id="8a3b5-p109">Ein **Record** -Objekt. Ein aus einem anderen **Record** geöffnetes **Record** -Objekt klont das ursprüngliche **Record** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-p109">A **Record** object. A **Record** object opened from another **Record** will clone the original **Record** object.</span></span>

  - <span data-ttu-id="8a3b5-p110">Ein **Command** -Objekt. Das geöffnete **Record** -Objekt stellt die einzelne Zeile dar, die beim Ausführen des **Command** zurückgegeben wurde. Enthalten die Ergebnisse mehrere Zeilen, wird der Inhalt der ersten Zeile im Datensatz platziert und der **Errors** -Auflistung wird möglicherweise ein Fehler hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-p110">A **Command** object. The opened **Record** object represents the single row returned by executing the **Command**. If the results contain more than a single row, the contents of the first row are placed in the record and an error may be added to the **Errors** collection.</span></span>

  - <span data-ttu-id="8a3b5-p111">Eine SQL SELECT-Anweisung. Das geöffnete **Record** -Objekt stellt die einzelne Zeile dar, die beim Ausführen des Inhalts der Zeichenfolge zurückgegeben wird. Enthalten die Ergebnisse mehrere Zeilen, wird der Inhalt der ersten Zeile im Datensatz platziert und der **Errors** -Auflistung wird möglicherweise ein Fehler hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-p111">A SQL SELECT statement. The opened **Record** object represents the single row returned by executing the contents of the string. If the results contain more than a single row, the contents of the first row are placed in the record and an error may be added to the **Errors** collection.</span></span>

  - <span data-ttu-id="8a3b5-146">Einen Tabellennamen.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-146">A table name.</span></span>

<span data-ttu-id="8a3b5-147">Stellt das **Record** -Objekt eine Entität dar, auf die nicht mithilfe einer URL zugegriffen werden kann (z. B. eine Zeile eines aus einer Datenbank abgeleiteten **Recordset** -Objekts), sind die Werte der [ParentURL](parenturl-property-ado.md)-Eigenschaft und des Felds, auf das mit der **adRecordURL** -Konstante zugegriffen wird, gleich 0 (Null).</span><span class="sxs-lookup"><span data-stu-id="8a3b5-147">If the **Record** object represents an entity that cannot be accessed with a URL (for example, a row of a **Recordset** derived from a database), then the values of both the [ParentURL](parenturl-property-ado.md) property and the field accessed with the **adRecordURL** constant are null.</span></span>


> [!NOTE]
<span data-ttu-id="8a3b5-148"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="8a3b5-148"><<<<<<< HEAD</span></span>
> <P><span data-ttu-id="8a3b5-p112">[!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird der <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider für Internet Publishing</A> automatisch aufgerufen. Weitere Informationen erhalten Sie unter <A href="absolute-and-relative-urls.md">Absolute und relative URLs</A>.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-p112">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>
=======
> <span data-ttu-id="8a3b5-151">[!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird der [Microsoft OLE DB Provider für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) automatisch aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-151">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="8a3b5-152">Weitere Informationen finden Sie unter [Absolute und relative URLs](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="8a3b5-152">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>
>>>>>>> <span data-ttu-id="8a3b5-153">master</span><span class="sxs-lookup"><span data-stu-id="8a3b5-153">master</span></span>


