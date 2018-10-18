---
<span data-ttu-id="ffb39-101"><<<<<<< HEAD-Titel: PageSize-Eigenschaft (ADO) TOCTitle: PageSize-Eigenschaft (ADO) === Titel: PageSize-Eigenschaft (ADO) TOCTitle: PageSize-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="ffb39-101"><<<<<<< HEAD title: PageSize Property (ADO) TOCTitle: PageSize Property (ADO) ======= title: PageSize property (ADO) TOCTitle: PageSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="ffb39-102">Master Ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b Ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15) Ms:contentKeyID: 48548079 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="ffb39-102">master ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15) ms:contentKeyID: 48548079 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="ffb39-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="ffb39-103"><<<<<<< HEAD</span></span>
# <a name="pagesize-property-ado"></a><span data-ttu-id="ffb39-104">PageSize-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="ffb39-104">PageSize Property (ADO)</span></span>
=======
# <a name="pagesize-property-ado"></a><span data-ttu-id="ffb39-105">PageSize-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="ffb39-105">PageSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="ffb39-106">master</span><span class="sxs-lookup"><span data-stu-id="ffb39-106">master</span></span>


<span data-ttu-id="ffb39-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ffb39-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ffb39-108">Gibt an, aus wie vielen Datensätze eine Seite im [Recordset](recordset-object-ado.md) besteht.</span><span class="sxs-lookup"><span data-stu-id="ffb39-108">Indicates how many records constitute one page in the [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="ffb39-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="ffb39-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="ffb39-110">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="ffb39-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="ffb39-111">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="ffb39-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="ffb39-112">master</span><span class="sxs-lookup"><span data-stu-id="ffb39-112">master</span></span>

<span data-ttu-id="ffb39-p101">Legt einen Long-Wert fest, der angibt, wie viele Datensätze sich auf einer Seite befinden. Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="ffb39-p101">Sets or returns a **Long** value that indicates how many records are on a page. The default is 10.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffb39-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ffb39-115">Remarks</span></span>

<span data-ttu-id="ffb39-116"><<<<<<< HEAD **PageSize** -Eigenschaft verwenden, um zu bestimmen, wie vielen Datensätzen eine logische Datenseite besteht.</span><span class="sxs-lookup"><span data-stu-id="ffb39-116"><<<<<<< HEAD Use the **PageSize** property to determine how many records make up a logical page of data.</span></span> <span data-ttu-id="ffb39-117">Durch das Einrichten einer Seitengröße können Sie mit der [AbsolutePage](absolutepage-property-ado.md)-Eigenschaft zum ersten Datensatz einer bestimmten Seite navigieren.</span><span class="sxs-lookup"><span data-stu-id="ffb39-117">Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page.</span></span> <span data-ttu-id="ffb39-118">Dies ist für Webserverszenarien hilfreich, wenn Sie dem Benutzer gestatten möchten, in den Daten zu blättern und jeweils eine bestimmte Anzahl von Datensätzen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ffb39-118">This is useful in Web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>
<span data-ttu-id="ffb39-119">=== Verwenden Sie die **PageSize** -Eigenschaft, um festzulegen, wie vielen Datensätzen eine logische Datenseite besteht.</span><span class="sxs-lookup"><span data-stu-id="ffb39-119">======= Use the **PageSize** property to determine how many records make up a logical page of data.</span></span> <span data-ttu-id="ffb39-120">Durch das Einrichten einer Seitengröße können Sie mit der [AbsolutePage](absolutepage-property-ado.md)-Eigenschaft zum ersten Datensatz einer bestimmten Seite navigieren.</span><span class="sxs-lookup"><span data-stu-id="ffb39-120">Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page.</span></span> <span data-ttu-id="ffb39-121">Dies ist nützlich in Szenarien, Web Server, wenn Sie den Benutzer zur Seite durch Daten sowie zulassen, jeweils eine bestimmte Anzahl von Datensätzen anzuzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="ffb39-121">This is useful in web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>
>>>>>>> <span data-ttu-id="ffb39-122">master</span><span class="sxs-lookup"><span data-stu-id="ffb39-122">master</span></span>

<span data-ttu-id="ffb39-123">Diese Eigenschaft kann jederzeit festgelegt werden. Mit ihrem Wert wird berechnet, wo sich der erste Datensatz auf einer bestimmten Seite befindet.</span><span class="sxs-lookup"><span data-stu-id="ffb39-123">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

