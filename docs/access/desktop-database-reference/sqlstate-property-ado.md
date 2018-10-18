---
<span data-ttu-id="22255-101"><<<<<<< HEAD-Titel: SQLState-Eigenschaft (ADO) TOCTitle: SQLState-Eigenschaft (ADO) === Titel: SQLState-Eigenschaft (ADO) TOCTitle: SQLState-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="22255-101"><<<<<<< HEAD title: SQLState Property (ADO) TOCTitle: SQLState Property (ADO) ======= title: SQLState property (ADO) TOCTitle: SQLState property (ADO)</span></span>
>>>>>>> <span data-ttu-id="22255-102">Master Ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15) Ms:contentKeyID: 48547806 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="22255-102">master ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15) ms:contentKeyID: 48547806 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="22255-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="22255-103"><<<<<<< HEAD</span></span>
# <a name="sqlstate-property-ado"></a><span data-ttu-id="22255-104">SQLState-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="22255-104">SQLState Property (ADO)</span></span>
=======
# <a name="sqlstate-property-ado"></a><span data-ttu-id="22255-105">SQLState-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="22255-105">SQLState property (ADO)</span></span>
>>>>>>> <span data-ttu-id="22255-106">master</span><span class="sxs-lookup"><span data-stu-id="22255-106">master</span></span>


<span data-ttu-id="22255-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="22255-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="22255-108">Gibt den SQL-Status für ein bestimmtes [Error](error-object-ado.md)-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="22255-108">Indicates the SQL state for a given [Error](error-object-ado.md) object.</span></span>

<span data-ttu-id="22255-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="22255-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="22255-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22255-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="22255-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22255-111">Return value</span></span>
>>>>>>> <span data-ttu-id="22255-112">master</span><span class="sxs-lookup"><span data-stu-id="22255-112">master</span></span>

<span data-ttu-id="22255-113">Gibt einen aus fünf Zeichen bestehenden **String** -Wert zurück, der dem ANSI SQL-Standard entspricht und einen Fehlercode angibt.</span><span class="sxs-lookup"><span data-stu-id="22255-113">Returns a five-character **String** value that follows the ANSI SQL standard and indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="22255-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="22255-114">Remarks</span></span>

<span data-ttu-id="22255-p101">Verwenden Sie die **SQLState** -Eigenschaft, um den aus fünf Zeichen bestehenden Fehlercode zu lesen, der vom Anbieter im Falle eines Fehlers bei der Verarbeitung einer SQL-Anweisung zurückgegeben wird. Wenn Sie z. B. den Microsoft OLE DB-Anbieter für ODBC mit einer Microsoft SQL Server-Datenbank verwenden, stammen SQL-Statusfehlercodes von ODBC. Die Codes basieren entweder auf Fehlern, die nur für ODBC gelten, oder auf Fehlern, die von Microsoft SQL Server stammen und dann ODBC-Fehlern zugeordnet wurden. Dieses Fehlercodes sind im ANSI SQL-Standard dokumentiert, sind jedoch in verschiedenen Datenquellen möglicherweise unterschiedlich implementiert.</span><span class="sxs-lookup"><span data-stu-id="22255-p101">Use the **SQLState** property to read the five-character error code that the provider returns when an error occurs during the processing of an SQL statement. For example, when using the Microsoft OLE DB Provider for ODBC with a Microsoft SQL Server database, SQL state error codes originate from ODBC, based either on errors specific to ODBC or on errors that originate from Microsoft SQL Server, and are then mapped to ODBC errors. These error codes are documented in the ANSI SQL standard, but may be implemented differently by different data sources.</span></span>

