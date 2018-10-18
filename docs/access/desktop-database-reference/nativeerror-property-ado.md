---
<span data-ttu-id="c11cf-101"><<<<<<< HEAD-Titel: NativeError-Eigenschaft (ADO) TOCTitle: NativeError-Eigenschaft (ADO) === Titel: NativeError-Eigenschaft (ADO) TOCTitle: NativeError-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="c11cf-101"><<<<<<< HEAD title: NativeError Property (ADO) TOCTitle: NativeError Property (ADO) ======= title: NativeError property (ADO) TOCTitle: NativeError property (ADO)</span></span>
>>>>>>> <span data-ttu-id="c11cf-102">Master Ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15) Ms:contentKeyID: 48546685 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="c11cf-102">master ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15) ms:contentKeyID: 48546685 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="c11cf-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="c11cf-103"><<<<<<< HEAD</span></span>
# <a name="nativeerror-property-ado"></a><span data-ttu-id="c11cf-104">NativeError-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="c11cf-104">NativeError Property (ADO)</span></span>
=======
# <a name="nativeerror-property-ado"></a><span data-ttu-id="c11cf-105">NativeError-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="c11cf-105">NativeError property (ADO)</span></span>
>>>>>>> <span data-ttu-id="c11cf-106">master</span><span class="sxs-lookup"><span data-stu-id="c11cf-106">master</span></span>


<span data-ttu-id="c11cf-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c11cf-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c11cf-108">Gibt den anbieterspezifischen Fehlercode für ein bestimmtes [Error](error-object-ado.md)-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="c11cf-108">Indicates the provider-specific error code for a given [Error](error-object-ado.md) object.</span></span>

<span data-ttu-id="c11cf-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="c11cf-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="c11cf-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c11cf-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="c11cf-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c11cf-111">Return value</span></span>
>>>>>>> <span data-ttu-id="c11cf-112">master</span><span class="sxs-lookup"><span data-stu-id="c11cf-112">master</span></span>

<span data-ttu-id="c11cf-113">Gibt einen **Long** -Wert zurück, der den Fehlercode angibt.</span><span class="sxs-lookup"><span data-stu-id="c11cf-113">Returns a **Long** value that indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c11cf-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c11cf-114">Remarks</span></span>

<span data-ttu-id="c11cf-p101">Rufen Sie mit der **NativeError** -Eigenschaft die datenbankspezifische Fehlerinformation für ein bestimmtes **Error** -Objekt ab. Wenn z. B. der Microsoft OLE DB-Anbieter für ODBC mit einer Microsoft SQL Server-Datenbank verwendet wird, werden systemeigene Fehlercodes, die aus SQL Server stammen, über ODBC und den ODBC-Anbieter an die **NativeError** -Eigenschaft übergeben.</span><span class="sxs-lookup"><span data-stu-id="c11cf-p101">Use the **NativeError** property to retrieve the database-specific error information for a particular **Error** object. For example, when using the Microsoft ODBC Provider for OLE DB with a Microsoft SQL Server database, native error codes that originate from SQL Server pass through ODBC and the ODBC Provider to the ADO **NativeError** property.</span></span>

