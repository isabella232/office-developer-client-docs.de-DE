---
title: Open-Methode (ADO-Verbindung)
TOCTitle: Open method (ADO Connection)
ms:assetid: 1adaa17d-dfe1-22e0-3415-720516d138f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248951(v=office.15)
ms:contentKeyID: 48543525
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3b83eb87b181320c86e1aea91ede70cd173a5ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288427"
---
# <a name="open-method-ado-connection"></a><span data-ttu-id="22cba-102">Open-Methode (ADO-Verbindung)</span><span class="sxs-lookup"><span data-stu-id="22cba-102">Open method (ADO Connection)</span></span>

<span data-ttu-id="22cba-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="22cba-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="22cba-104">Eine Verbindung mit einer Datenquelle wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="22cba-104">Opens a connection to a data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="22cba-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="22cba-105">Syntax</span></span>

<span data-ttu-id="22cba-106">*Connection*. Open*ConnectionString*, *UserID*, *Password*, *Optionen*</span><span class="sxs-lookup"><span data-stu-id="22cba-106">*connection*.Open*ConnectionString*, *UserID*, *Password*, *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="22cba-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="22cba-107">Parameters</span></span>

|<span data-ttu-id="22cba-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="22cba-108">Parameter</span></span>|<span data-ttu-id="22cba-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22cba-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="22cba-110">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="22cba-110">*ConnectionString*</span></span> |<span data-ttu-id="22cba-p101">Optional. Ein **String** -Wert, der Verbindungsinformationen enthält. Details zu den gültigen Einstellungen finden Sie unter der [ConnectionString](connectionstring-property-ado.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="22cba-p101">Optional. A **String** value that contains connection information. See the [ConnectionString](connectionstring-property-ado.md) property for details on valid settings.</span></span>|
|<span data-ttu-id="22cba-114">*UserID*</span><span class="sxs-lookup"><span data-stu-id="22cba-114">*UserID*</span></span> |<span data-ttu-id="22cba-p102">Optional. Ein **String** -Wert, der einen Benutzernamen enthält, der beim Herstellen der Verbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="22cba-p102">Optional. A **String** value that contains a user name to use when establishing the connection.</span></span>|
|<span data-ttu-id="22cba-117">*Password*</span><span class="sxs-lookup"><span data-stu-id="22cba-117">*Password*</span></span> |<span data-ttu-id="22cba-p103">Optional. Ein **String** -Wert, der ein Kennwort enthält, das beim Herstellen der Verbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="22cba-p103">Optional. A **String** value that contains a password to use when establishing the connection.</span></span>|
|<span data-ttu-id="22cba-120">*Options*</span><span class="sxs-lookup"><span data-stu-id="22cba-120">*Options*</span></span> |<span data-ttu-id="22cba-p104">Optional. Ein [ConnectOptionEnum](connectoptionenum.md)-Wert, durch den festgelegt wird, dass diese Methode nach (synchron) oder vor (asynchron) dem Herstellen der Verbindung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="22cba-p104">Optional. A [ConnectOptionEnum](connectoptionenum.md) value that determines whether this method should return after (synchronously) or before (asynchronously) the connection is established.</span></span>|

## <a name="remarks"></a><span data-ttu-id="22cba-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22cba-123">Remarks</span></span>

<span data-ttu-id="22cba-p105">Durch Verwenden der **Open**-Methode für ein [Connection](connection-object-ado.md)-Objekt wird die physische Verbindung mit einer Datenquelle hergestellt. Nach dem erfolgreichen Abschluss dieser Methode ist die Verbindung aktiv, und Sie können Befehle für sie ausgeben und die Ergebnisse verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="22cba-p105">Using the **Open** method on a [Connection](connection-object-ado.md) object establishes the physical connection to a data source. After this method successfully completes, the connection is live and you can issue commands against it and process the results.</span></span>

<span data-ttu-id="22cba-126">Verwenden Sie das optionale *ConnectionString* -Argument, um eine Verbindungszeichenfolge anzugeben, die eine Reihe von durch Semikolons getrennte *Argument* *= Wert* -Anweisungen enthält, oder eine Datei oder eine Verzeichnis Ressource, die mit einer URL identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="22cba-126">Use the optional *ConnectionString* argument to specify either a connection string containing a series of *argument* *= value* statements separated by semicolons, or a file or directory resource identified with a URL.</span></span> <span data-ttu-id="22cba-127">Die **ConnectionString**-Eigenschaft erbt automatisch den für das *ConnectionString*-Argument verwendeten Wert.</span><span class="sxs-lookup"><span data-stu-id="22cba-127">The **ConnectionString** property automatically inherits the value used for the *ConnectionString* argument.</span></span> <span data-ttu-id="22cba-128">Daher können Sie die **ConnectionString**-Eigenschaft des **Connection**-Objekts festlegen, bevor Sie es öffnen, oder das *ConnectionString*-Argument verwenden, um die aktuellen Verbindungsparameter während des Aufrufs der **Open**-Methode festzulegen oder außer Kraft zu setzen.</span><span class="sxs-lookup"><span data-stu-id="22cba-128">Therefore, you can either set the **ConnectionString** property of the **Connection** object before opening it, or use the *ConnectionString* argument to set or override the current connection parameters during the **Open** method call.</span></span>

<span data-ttu-id="22cba-129">Wenn Sie Benutzer- und Kennwortinformationen sowohl im *ConnectionString*-Argument als auch in den optionalen Argumenten *UserID* und *Password* übergeben, werden durch die Argumente *UserID* und *Password* die in *ConnectionString* angegebenen Werte außer Kraft gesetzt.</span><span class="sxs-lookup"><span data-stu-id="22cba-129">If you pass user and password information both in the *ConnectionString* argument and in the optional *UserID* and *Password* arguments, the *UserID* and *Password* arguments will override the values specified in *ConnectionString*.</span></span>

<span data-ttu-id="22cba-p107">Wenn Sie die Operationen über eine offene **Verbindung** abgeschlossen haben, verwenden Sie die [Close](close-method-ado.md)-Methode, um zugeordnete Systemressourcen freizugeben. Durch das Schließen eines Objekts wird dieses nicht aus dem Speicher entfernt. Sie können seine Eigenschafteneinstellungen ändern und es später mit der **Open**-Methode erneut öffnen. Legen Sie die Objektvariable auf *Nothing* fest, um ein Objekt vollständig aus dem Speicher zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="22cba-p107">When you have concluded your operations over an open **Connection**, use the [Close](close-method-ado.md) method to free any associated system resources. Closing an object does not remove it from memory; you can change its property settings and use the **Open** method to open it again later. To completely eliminate an object from memory, set the object variable to *Nothing*.</span></span>

<span data-ttu-id="22cba-133">**Remote Data Service-Verwendung** Bei Verwendung in einem clientseitigen **Connection** -Objekt stellt die **Open** -Methode erst dann eine Verbindung mit dem Server her, wenn für das **Connection** -Objekt ein [Recordset](recordset-object-ado.md) geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="22cba-133">**Remote Data Service Usage**When used on a client-side **Connection** object, the **Open** method doesn't actually establish a connection to the server until a [Recordset](recordset-object-ado.md) is opened on the **Connection** object.</span></span>

> [!NOTE]
> <span data-ttu-id="22cba-134">Bei URLs, die das HTTP-Schema verwenden, wird automatisch der [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="22cba-134">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="22cba-135">Weitere Informationen finden Sie unter [absolute und relative URLs](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="22cba-135">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


