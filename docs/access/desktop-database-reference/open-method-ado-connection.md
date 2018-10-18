---
title: Open-Methode (ADO-Verbindung)
TOCTitle: Open Method (ADO Connection)
ms:assetid: 1adaa17d-dfe1-22e0-3415-720516d138f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248951(v=office.15)
ms:contentKeyID: 48543525
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 78c20ce6da4c20385bd22488ce910312c737986e
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606332"
---
# <a name="open-method-ado-connection"></a><span data-ttu-id="36528-102">Open-Methode (ADO-Verbindung)</span><span class="sxs-lookup"><span data-stu-id="36528-102">Open Method (ADO Connection)</span></span>


<span data-ttu-id="36528-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="36528-103">**Applies to**: Access 2013 | Office 2013</span></span>
 

<span data-ttu-id="36528-104">Eine Verbindung mit einer Datenquelle wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="36528-104">Opens a connection to a data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="36528-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="36528-105">Syntax</span></span>

<span data-ttu-id="36528-106">*Verbindung*. Öffnen Sie*ConnectionString*, *UserID*, *Kennwort*, *Optionen*</span><span class="sxs-lookup"><span data-stu-id="36528-106">*connection*.Open*ConnectionString*, *UserID*, *Password*, *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="36528-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="36528-107">Parameters</span></span>

  - <span data-ttu-id="36528-108">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="36528-108">*ConnectionString*</span></span>

  - <span data-ttu-id="36528-p101">Optional. Ein **String** -Wert, der Verbindungsinformationen enthält. Details zu den gültigen Einstellungen finden Sie unter der [ConnectionString](connectionstring-property-ado.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="36528-p101">Optional. A **String** value that contains connection information. See the [ConnectionString](connectionstring-property-ado.md) property for details on valid settings.</span></span>

  - <span data-ttu-id="36528-112">*UserID*</span><span class="sxs-lookup"><span data-stu-id="36528-112">*UserID*</span></span>

  - <span data-ttu-id="36528-p102">Optional. Ein **String** -Wert, der einen Benutzernamen enthält, der beim Herstellen der Verbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="36528-p102">Optional. A **String** value that contains a user name to use when establishing the connection.</span></span>

  - <span data-ttu-id="36528-115">*Password*</span><span class="sxs-lookup"><span data-stu-id="36528-115">*Password*</span></span>

  - <span data-ttu-id="36528-p103">Optional. Ein **String** -Wert, der ein Kennwort enthält, das beim Herstellen der Verbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="36528-p103">Optional. A **String** value that contains a password to use when establishing the connection.</span></span>

  - <span data-ttu-id="36528-118">*Options*</span><span class="sxs-lookup"><span data-stu-id="36528-118">*Options*</span></span>

  - <span data-ttu-id="36528-p104">Optional. Ein [ConnectOptionEnum](connectoptionenum.md)-Wert, durch den festgelegt wird, dass diese Methode nach (synchron) oder vor (asynchron) dem Herstellen der Verbindung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="36528-p104">Optional. A [ConnectOptionEnum](connectoptionenum.md) value that determines whether this method should return after (synchronously) or before (asynchronously) the connection is established.</span></span>

## <a name="remarks"></a><span data-ttu-id="36528-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="36528-121">Remarks</span></span>

<span data-ttu-id="36528-p105">Durch Verwenden der **Open** -Methode für ein [Connection](connection-object-ado.md)-Objekt wird die physische Verbindung mit einer Datenquelle hergestellt. Nach dem erfolgreichen Abschluss dieser Methode ist die Verbindung aktiv, und Sie können Befehle für sie ausgeben und die Ergebnisse verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="36528-p105">Using the **Open** method on a [Connection](connection-object-ado.md) object establishes the physical connection to a data source. After this method successfully completes, the connection is live and you can issue commands against it and process the results.</span></span>

<span data-ttu-id="36528-124">Verwenden Sie das optionale Argument *ConnectionString* , um entweder eine Verbindungszeichenfolge fest, die mit einer Reihe von durch Semikolons oder eine Datei getrennte *Argument* *= Wert* Anweisungen oder Directory-Ressource mit einer URL identifiziert anzugeben.</span><span class="sxs-lookup"><span data-stu-id="36528-124">Use the optional *ConnectionString* argument to specify either a connection string containing a series of *argument* *= value* statements separated by semicolons, or a file or directory resource identified with a URL.</span></span> <span data-ttu-id="36528-125">Die **ConnectionString** -Eigenschaft erbt automatisch den Wert für das Argument *ConnectionString* verwendet.</span><span class="sxs-lookup"><span data-stu-id="36528-125">The **ConnectionString** property automatically inherits the value used for the *ConnectionString* argument.</span></span> <span data-ttu-id="36528-126">Aus diesem Grund kann entweder die **ConnectionString** -Eigenschaft des **Connection** -Objekts festlegen, bevor Sie ihn öffnen, oder verwenden Sie das Argument *ConnectionString* festzulegen oder außer Kraft setzen die aktuellen Verbindungsparameter während des Aufrufs der **Open** -Methode .</span><span class="sxs-lookup"><span data-stu-id="36528-126">Therefore, you can either set the **ConnectionString** property of the **Connection** object before opening it, or use the *ConnectionString* argument to set or override the current connection parameters during the **Open** method call.</span></span>

<span data-ttu-id="36528-127">Wenn Sie Benutzer- und Kennwortinformationen sowohl im *ConnectionString*-Argument als auch in den optionalen Argumenten *UserID* und *Password* übergeben, werden durch die Argumente *UserID* und *Password* die in *ConnectionString* angegebenen Werte außer Kraft gesetzt.</span><span class="sxs-lookup"><span data-stu-id="36528-127">If you pass user and password information both in the *ConnectionString* argument and in the optional *UserID* and *Password* arguments, the *UserID* and *Password* arguments will override the values specified in *ConnectionString*.</span></span>

<span data-ttu-id="36528-p107">Wenn Sie die Operationen über eine offene **Verbindung** abgeschlossen haben, verwenden Sie die [Close](close-method-ado.md)-Methode, um zugeordnete Systemressourcen freizugeben. Durch das Schließen eines Objekts wird dieses nicht aus dem Speicher entfernt. Sie können seine Eigenschafteneinstellungen ändern und es später mit der **Open**-Methode erneut öffnen. Legen Sie die Objektvariable auf *Nothing* fest, um ein Objekt vollständig aus dem Speicher zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="36528-p107">When you have concluded your operations over an open **Connection**, use the [Close](close-method-ado.md) method to free any associated system resources. Closing an object does not remove it from memory; you can change its property settings and use the **Open** method to open it again later. To completely eliminate an object from memory, set the object variable to *Nothing*.</span></span>

<span data-ttu-id="36528-131">**Remote Data Service-Verwendung** Wenn für ein clientseitiges **Connection** -Objekt verwendet, herstellen nicht die **Open** -Methode tatsächlich eine Verbindung mit dem Server, bis ein [Recordset-Objekt](recordset-object-ado.md) für das **Connection** -Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="36528-131">**Remote Data Service Usage**When used on a client-side **Connection** object, the **Open** method doesn't actually establish a connection to the server until a [Recordset](recordset-object-ado.md) is opened on the **Connection** object.</span></span>


> [!NOTE]
<span data-ttu-id="36528-132"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="36528-132"><<<<<<< HEAD</span></span>
> <P><span data-ttu-id="36528-p108">[!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird der <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider für Internet Publishing</A> automatisch aufgerufen. Weitere Informationen erhalten Sie unter <A href="absolute-and-relative-urls.md">Absolute und relative URLs</A>.</span><span class="sxs-lookup"><span data-stu-id="36528-p108">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>
=======
> <span data-ttu-id="36528-135">[!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird der [Microsoft OLE DB Provider für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) automatisch aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="36528-135">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="36528-136">Weitere Informationen finden Sie unter [Absolute und relative URLs](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="36528-136">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>
>>>>>>> <span data-ttu-id="36528-137">master</span><span class="sxs-lookup"><span data-stu-id="36528-137">master</span></span>


