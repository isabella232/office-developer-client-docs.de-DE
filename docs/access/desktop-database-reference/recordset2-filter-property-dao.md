---
title: Recordset2. Filter-Eigenschaft (DAO)
TOCTitle: Filter Property
ms:assetid: 5b3b4e18-8af4-5acd-a129-513ba2d913d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194529(v=office.15)
ms:contentKeyID: 48545069
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053062
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 19f3c017aa5d4a353f3e832a3678d921565ea822
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307329"
---
# <a name="recordset2filter-property-dao"></a><span data-ttu-id="a807c-102">Recordset2. Filter-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="a807c-102">Recordset2.Filter property (DAO)</span></span>


<span data-ttu-id="a807c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a807c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a807c-104">Legt einen Wert fest, der feststellt, welche Datensätze in einem nachfolgend geöffneten **Recordset**-Objekt einbezogen werden, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="a807c-104">Sets or returns a value that determines the records included in a subsequently opened **Recordset** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="a807c-105">**String**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a807c-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a807c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a807c-106">Syntax</span></span>

<span data-ttu-id="a807c-107">*Ausdruck* . Filter</span><span class="sxs-lookup"><span data-stu-id="a807c-107">*expression* .Filter</span></span>

<span data-ttu-id="a807c-108">*Ausdruck* Ein Ausdruck, der ein **Recordset2** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a807c-108">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a807c-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a807c-109">Remarks</span></span>

<span data-ttu-id="a807c-110">Die Einstellung bzw. der Rückgabewert ist ein String-Datentyp, der die WHERE-Klausel einer SQL-Anweisung ohne das reservierte Wort WHERE enthält.</span><span class="sxs-lookup"><span data-stu-id="a807c-110">The setting or return value is a String data type that contains the WHERE clause of an SQL statement without the reserved word WHERE.</span></span>

<span data-ttu-id="a807c-111">Verwenden Sie die **Filter**-Eigenschaft zum Anwenden eines Filters auf ein **Recordset**-Objekt vom Typ "Dynaset", "Snapshot" oder "Forward-only".</span><span class="sxs-lookup"><span data-stu-id="a807c-111">Use the **Filter** property to apply a filter to a dynaset–, snapshot–, or forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="a807c-112">Mit der **Filter**-Eigenschaft können Sie die Datensätze beschränken, die von einem vorhandenen Objekt zurückgegeben werden, wenn ein neues **Recordset**-Objekt basierend auf einem vorhandenen **Recordset**-Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="a807c-112">You can use the **Filter** property to restrict the records returned from an existing object when a new **Recordset** object is opened based on an existing **Recordset** object.</span></span>

<span data-ttu-id="a807c-113">Verwenden Sie das US-Datumsformat (Monat-Tag-Jahr) beim Filtern von Feldern, die Datumsangaben enthalten, auch wenn Sie nicht die US-Version des Microsoft Access-Datenbankmoduls verwenden (in diesem Fall müssen Sie Datumsangaben durch Verketten von Zeichenfolgen zusammensetzen, beispielsweise strMonth & "-" _ aMP_ strDay & "-" & strYear).</span><span class="sxs-lookup"><span data-stu-id="a807c-113">Use the U.S. date format (month-day-year) when you filter fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine (in which case you must assemble any dates by concatenating strings, for example, strMonth & "-" & strDay & "-" & strYear).</span></span> <span data-ttu-id="a807c-114">Andernfalls werden die Daten möglicherweise nicht wie erwartet gefiltert.</span><span class="sxs-lookup"><span data-stu-id="a807c-114">Otherwise, the data may not be filtered as you expect.</span></span>

<span data-ttu-id="a807c-115">In vielen Fällen ist es schneller, ein neues **Recordset**-Objekt zu öffnen, indem Sie eine SQL-Anweisung mit einer WHERE-Klausel verwenden.</span><span class="sxs-lookup"><span data-stu-id="a807c-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes a WHERE clause.</span></span>

<span data-ttu-id="a807c-116">Wenn Sie die-Eigenschaft auf eine Zeichenfolge festlegen, die mit einem nicht-ganzzahligen Wert verkettet ist, und die Systemparameter ein nicht-U. S. Decimal-Zeichen wie ein Komma (beispielsweise strFilter \> = "Price" & lngPrice und lngPrice = 125, 50) angeben, tritt ein Fehler auf, wenn Sie versuchen, Öffnen Sie das nächste **Recordset**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a807c-116">If you set the property to a string concatenated with a non–integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strFilter = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the next **Recordset**.</span></span> <span data-ttu-id="a807c-117">Dies liegt daran, dass der Wert während der Verkettung mithilfe des Standard-Dezimaltrennzeichens in eine Zeichenfolge konvertiert wird und Microsoft Access SQL nur US-Dezimaltrennzeichen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="a807c-117">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

