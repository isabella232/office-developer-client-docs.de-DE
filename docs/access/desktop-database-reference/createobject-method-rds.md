---
title: CreateObject-Methode (RDS)
TOCTitle: CreateObject method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d08b596afb24fff430c6c662a557da1880addefa
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921180"
---
# <a name="createobject-method-rds"></a><span data-ttu-id="0d62e-102">CreateObject-Methode (RDS)</span><span class="sxs-lookup"><span data-stu-id="0d62e-102">CreateObject method (RDS)</span></span>


<span data-ttu-id="0d62e-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d62e-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="0d62e-p101">Erstellt den Proxy für das Zielgeschäftsobjekt und gibt einen Zeiger auf das Objekt zurück. Der Proxy verpackt Daten und leitet diese Daten an den serverseitigen Stub für die Kommunikation mit dem Geschäftsobjekt weiter, damit Anfragen und Daten über das Internet gesendet werden. Bei In-Process-Komponentenobjekten werden keine Proxies verwendet, sondern wird lediglich ein Zeiger auf das Objekt bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="0d62e-p101">Creates the proxy for the target business object and returns a pointer to it. The proxy packages and marshals data to the server-side stub for communications with the business object to send requests and data over the Internet. For in-process component objects, no proxies are used, just a pointer to the object is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d62e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d62e-107">Syntax</span></span>

<span data-ttu-id="0d62e-108">Von Remote Data Service werden die folgenden Protokolle unterstützt: HTTP, HTTPS (HTTP über Secure Socket Layer), DCOM und In-Process (prozessinternes Protokoll).</span><span class="sxs-lookup"><span data-stu-id="0d62e-108">Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP over Secure Socket Layer), DCOM, and in-process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0d62e-109">Protokoll</span><span class="sxs-lookup"><span data-stu-id="0d62e-109">Protocol</span></span></p></th>
<th><p><span data-ttu-id="0d62e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d62e-110">Syntax</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d62e-111">HTTP</span><span class="sxs-lookup"><span data-stu-id="0d62e-111">HTTP</span></span></p></td>
<td><p><span data-ttu-id="0d62e-112">Legen Sie<em>Objekt</em> = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>https://awebsrvr</em> &quot;)</span><span class="sxs-lookup"><span data-stu-id="0d62e-112">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d62e-113">HTTPS</span><span class="sxs-lookup"><span data-stu-id="0d62e-113">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="0d62e-114">Legen Sie<em>Objekt</em> = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>https://awebsrvr</em> &quot;)</span><span class="sxs-lookup"><span data-stu-id="0d62e-114">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d62e-115">DCOM</span><span class="sxs-lookup"><span data-stu-id="0d62e-115">DCOM</span></span></p></td>
<td><p><span data-ttu-id="0d62e-116">Legen Sie<em>Objekt</em> = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>Computername</em>&quot;)</span><span class="sxs-lookup"><span data-stu-id="0d62e-116">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>computername</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d62e-117">In-Process</span><span class="sxs-lookup"><span data-stu-id="0d62e-117">In-process</span></span></p></td>
<td><p><span data-ttu-id="0d62e-118">Legen Sie<em>Objekt</em> = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span><span class="sxs-lookup"><span data-stu-id="0d62e-118">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a><span data-ttu-id="0d62e-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d62e-119">Parameters</span></span>

  - <span data-ttu-id="0d62e-120">*Object*</span><span class="sxs-lookup"><span data-stu-id="0d62e-120">*Object*</span></span>

  - <span data-ttu-id="0d62e-121">Eine Objektvariable, die zu einem Objekt ausgewertet wird, das den in *ProgID* angegebenen Typ hat.</span><span class="sxs-lookup"><span data-stu-id="0d62e-121">An object variable that evaluates to an object that is the type specified in *ProgID*.</span></span>

  - <span data-ttu-id="0d62e-122">*DataSpace*</span><span class="sxs-lookup"><span data-stu-id="0d62e-122">*DataSpace*</span></span>

  - <span data-ttu-id="0d62e-123">Eine Objektvariable, die ein [RDS.DataSpace](dataspace-object-rds.md)-Objekt darstellt, das zum Erstellen einer Instanz des neuen Objekts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0d62e-123">An object variable that represents an [RDS.DataSpace](dataspace-object-rds.md) object used to create an instance of the new object.</span></span>

  - <span data-ttu-id="0d62e-124">*ProgID*</span><span class="sxs-lookup"><span data-stu-id="0d62e-124">*ProgID*</span></span>

  - <span data-ttu-id="0d62e-125">Ein **String** -Wert mit dem programmgesteuerten Bezeichner, der ein serverseitiges Geschäftsobjekt angibt, das die Geschäftregeln Ihrer Anwendung implementiert.</span><span class="sxs-lookup"><span data-stu-id="0d62e-125">A **String** value that contains the programmatic identifier specifying a server-side business object that implements your application's business rules.</span></span>

  - <span data-ttu-id="0d62e-126">*Awebsrvr* oder *computername*</span><span class="sxs-lookup"><span data-stu-id="0d62e-126">*awebsrvr* or *computername*</span></span>

  - <span data-ttu-id="0d62e-127">Ein **String** -Wert, der eine URL, die den Webserver der Internetinformationsdienste (Internet Information Services, IIS) identifiziert, auf denen eine Instanz des Objekts Business Server darstellt, wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="0d62e-127">A **String** value that represents a URL identifying the Internet Information Services (IIS) web server where an instance of the server business object is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d62e-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0d62e-128">Remarks</span></span>

<span data-ttu-id="0d62e-129">Das *http-Protokoll* ist ein standard-Web-Protokoll. *HTTPS* ist eine sichere Web-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="0d62e-129">The *HTTP protocol* is the standard web protocol; *HTTPS* is a secure web protocol.</span></span> <span data-ttu-id="0d62e-130">Verwenden Sie das *DCOM-Protokoll* , wenn ein LAN ohne HTTP ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d62e-130">Use the *DCOM protocol* when running a local-area network without HTTP.</span></span> <span data-ttu-id="0d62e-131">Das *in-Process* -Protokoll ist einer lokalen Dynamic-Link Library (DLL); Es wird ein Netzwerk nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0d62e-131">The *in-process* protocol is a local dynamic-link library (DLL); it does not use a network.</span></span>

