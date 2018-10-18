---
title: CreateObject-Methode (RDS)
TOCTitle: CreateObject Method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2ff2381626e8cf81aa95ee9d49f9396bd4b0316
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602720"
---
# <a name="createobject-method-rds"></a><span data-ttu-id="d7148-102">CreateObject-Methode (RDS)</span><span class="sxs-lookup"><span data-stu-id="d7148-102">CreateObject Method (RDS)</span></span>


<span data-ttu-id="d7148-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7148-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="d7148-p101">Erstellt den Proxy für das Zielgeschäftsobjekt und gibt einen Zeiger auf das Objekt zurück. Der Proxy verpackt Daten und leitet diese Daten an den serverseitigen Stub für die Kommunikation mit dem Geschäftsobjekt weiter, damit Anfragen und Daten über das Internet gesendet werden. Bei In-Process-Komponentenobjekten werden keine Proxies verwendet, sondern wird lediglich ein Zeiger auf das Objekt bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d7148-p101">Creates the proxy for the target business object and returns a pointer to it. The proxy packages and marshals data to the server-side stub for communications with the business object to send requests and data over the Internet. For in-process component objects, no proxies are used, just a pointer to the object is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7148-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7148-107">Syntax</span></span>

<span data-ttu-id="d7148-108">Von Remote Data Service werden die folgenden Protokolle unterstützt: HTTP, HTTPS (HTTP über Secure Socket Layer), DCOM und In-Process (prozessinternes Protokoll).</span><span class="sxs-lookup"><span data-stu-id="d7148-108">Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP over Secure Socket Layer), DCOM, and in-process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d7148-109">Protokoll</span><span class="sxs-lookup"><span data-stu-id="d7148-109">Protocol</span></span></p></th>
<th><p><span data-ttu-id="d7148-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7148-110">Syntax</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d7148-111">HTTP</span><span class="sxs-lookup"><span data-stu-id="d7148-111">HTTP</span></span></p></td>
<td><p><span data-ttu-id="d7148-112">Legen Sie<em>Objekt</em> = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>https://awebsrvr</em> &quot;)</span><span class="sxs-lookup"><span data-stu-id="d7148-112">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7148-113">HTTPS</span><span class="sxs-lookup"><span data-stu-id="d7148-113">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="d7148-114">Legen Sie<em>Objekt</em> = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>https://awebsrvr</em> &quot;)</span><span class="sxs-lookup"><span data-stu-id="d7148-114">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7148-115">DCOM</span><span class="sxs-lookup"><span data-stu-id="d7148-115">DCOM</span></span></p></td>
<td><p><span data-ttu-id="d7148-116">Legen Sie<em>Objekt</em> = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>Computername</em>&quot;)</span><span class="sxs-lookup"><span data-stu-id="d7148-116">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>computername</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7148-117">In-Process</span><span class="sxs-lookup"><span data-stu-id="d7148-117">In-process</span></span></p></td>
<td><p><span data-ttu-id="d7148-118">Legen Sie<em>Objekt</em> = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span><span class="sxs-lookup"><span data-stu-id="d7148-118">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a><span data-ttu-id="d7148-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7148-119">Parameters</span></span>

  - <span data-ttu-id="d7148-120">*Object*</span><span class="sxs-lookup"><span data-stu-id="d7148-120">*Object*</span></span>

  - <span data-ttu-id="d7148-121">Eine Objektvariable, die zu einem Objekt ausgewertet wird, das den in *ProgID* angegebenen Typ hat.</span><span class="sxs-lookup"><span data-stu-id="d7148-121">An object variable that evaluates to an object that is the type specified in *ProgID*.</span></span>

  - <span data-ttu-id="d7148-122">*DataSpace*</span><span class="sxs-lookup"><span data-stu-id="d7148-122">*DataSpace*</span></span>

  - <span data-ttu-id="d7148-123">Eine Objektvariable, die ein [RDS.DataSpace](dataspace-object-rds.md)-Objekt darstellt, das zum Erstellen einer Instanz des neuen Objekts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d7148-123">An object variable that represents an [RDS.DataSpace](dataspace-object-rds.md) object used to create an instance of the new object.</span></span>

  - <span data-ttu-id="d7148-124">*ProgID*</span><span class="sxs-lookup"><span data-stu-id="d7148-124">*ProgID*</span></span>

  - <span data-ttu-id="d7148-125">Ein **String** -Wert mit dem programmgesteuerten Bezeichner, der ein serverseitiges Geschäftsobjekt angibt, das die Geschäftregeln Ihrer Anwendung implementiert.</span><span class="sxs-lookup"><span data-stu-id="d7148-125">A **String** value that contains the programmatic identifier specifying a server-side business object that implements your application's business rules.</span></span>

  - <span data-ttu-id="d7148-126">*Awebsrvr* oder *computername*</span><span class="sxs-lookup"><span data-stu-id="d7148-126">*awebsrvr* or *computername*</span></span>

<span data-ttu-id="d7148-127"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="d7148-127"><<<<<<< HEAD</span></span>
  - <span data-ttu-id="d7148-128">Ein **String** -Wert, der eine URL darstellt, die den Webserver der Internetinformationsdienste angibt, auf denen eine Instanz des Servergeschäftsobjekts erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d7148-128">A **String** value that represents a URL identifying the Internet Information Services (IIS) Web server where an instance of the server business object is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7148-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d7148-129">Remarks</span></span>

<a name="the-http-protocol-is-the-standard-web-protocol-https-is-a-secure-web-protocol-use-the-dcom-protocol-when-running-a-local-area-network-without-http-the-in-process-protocol-is-a-local-dynamic-link-library-dll-it-does-not-use-a-network"></a><span data-ttu-id="d7148-130">Das *http-Protokoll* ist das Standardprotokoll Web; *HTTPS* ist eine sichere Webprotokoll.</span><span class="sxs-lookup"><span data-stu-id="d7148-130">The *HTTP protocol* is the standard Web protocol; *HTTPS* is a secure Web protocol.</span></span> <span data-ttu-id="d7148-131">Verwenden Sie das *DCOM-Protokoll* , wenn ein LAN ohne HTTP ausführen.</span><span class="sxs-lookup"><span data-stu-id="d7148-131">Use the *DCOM protocol* when running a local-area network without HTTP.</span></span> <span data-ttu-id="d7148-132">Das *in-Process* -Protokoll ist einer lokalen Dynamic-Link Library (DLL); Es wird ein Netzwerk nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7148-132">The *in-process* protocol is a local dynamic-link library (DLL); it does not use a network.</span></span>
=======
  - <span data-ttu-id="d7148-133">Ein **String** -Wert, der eine URL, die den Webserver der Internetinformationsdienste (Internet Information Services, IIS) identifiziert, auf denen eine Instanz des Objekts Business Server darstellt, wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="d7148-133">A **String** value that represents a URL identifying the Internet Information Services (IIS) web server where an instance of the server business object is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7148-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d7148-134">Remarks</span></span>

<span data-ttu-id="d7148-135">Das *http-Protokoll* ist ein standard-Web-Protokoll. *HTTPS* ist eine sichere Web-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="d7148-135">The *HTTP protocol* is the standard web protocol; *HTTPS* is a secure web protocol.</span></span> <span data-ttu-id="d7148-136">Verwenden Sie das *DCOM-Protokoll* , wenn ein LAN ohne HTTP ausführen.</span><span class="sxs-lookup"><span data-stu-id="d7148-136">Use the *DCOM protocol* when running a local-area network without HTTP.</span></span> <span data-ttu-id="d7148-137">Das *in-Process* -Protokoll ist einer lokalen Dynamic-Link Library (DLL); Es wird ein Netzwerk nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7148-137">The *in-process* protocol is a local dynamic-link library (DLL); it does not use a network.</span></span>
>>>>>>> <span data-ttu-id="d7148-138">master</span><span class="sxs-lookup"><span data-stu-id="d7148-138">master</span></span>

