---
title: Recordset2.Filter-Eigenschaft (DAO)
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720352"
---
# <a name="recordset2filter-property-dao"></a><span data-ttu-id="11567-102">Recordset2.Filter-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="11567-102">Recordset2.Filter property (DAO)</span></span>


<span data-ttu-id="11567-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="11567-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="11567-p101">Legt einen Wert fest, der die in einem nachfolgend geöffneten **Recordset** -Objekt enthaltenen Datensätze bestimmt, oder gibt diesen Wert zurück (nur Microsoft Access-Arbeitsbereich). Lese-/Schreibzugriff **String**.</span><span class="sxs-lookup"><span data-stu-id="11567-p101">Sets or returns a value that determines the records included in a subsequently opened **Recordset** object (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="11567-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="11567-106">Syntax</span></span>

<span data-ttu-id="11567-107">*Ausdruck* . Filter</span><span class="sxs-lookup"><span data-stu-id="11567-107">*expression* .Filter</span></span>

<span data-ttu-id="11567-108">*Ausdruck* Ein Ausdruck, der ein **Recordset2** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="11567-108">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="11567-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11567-109">Remarks</span></span>

<span data-ttu-id="11567-110">Die Einstellung bzw. der Rückgabewert ist ein String-Datentyp, der die WHERE-Klausel einer SQL-Anweisung ohne das reservierte Wort WHERE enthält.</span><span class="sxs-lookup"><span data-stu-id="11567-110">The setting or return value is a String data type that contains the WHERE clause of an SQL statement without the reserved word WHERE.</span></span>

<span data-ttu-id="11567-111">Verwenden Sie die **Filter** -Eigenschaft, um einen Filter auf ein Dynaset, Snapshot oder vorwärts Typ **Recordset** -Objekt anwenden.</span><span class="sxs-lookup"><span data-stu-id="11567-111">Use the **Filter** property to apply a filter to a dynaset–, snapshot–, or forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="11567-112">Mit der **Filter** -Eigenschaft können Sie die Datensätze beschränken, die von einem vorhandenen Objekt zurückgegeben werden, wenn ein neues **Recordset** -Objekt basierend auf einem vorhandenen **Recordset** -Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="11567-112">You can use the **Filter** property to restrict the records returned from an existing object when a new **Recordset** object is opened based on an existing **Recordset** object.</span></span>

<span data-ttu-id="11567-113">Verwenden Sie das US-Datumsformat (Monat-Tag-Jahr) Wenn Sie Felder mit Datumsangaben filtern, auch wenn Sie nicht die US-Version von Microsoft Access-Datenbankmodul verwenden (in diesem Fall Sie alle Datumsangaben durch Verketten von Zeichenfolgen, beispielsweise StrMonth & zusammensetzen müssen "-" _ aMP_ StrDay & "-" & erstellen).</span><span class="sxs-lookup"><span data-stu-id="11567-113">Use the U.S. date format (month-day-year) when you filter fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine (in which case you must assemble any dates by concatenating strings, for example, strMonth & "-" & strDay & "-" & strYear).</span></span> <span data-ttu-id="11567-114">Andernfalls können die Daten nicht gefiltert werden, wie erwartet.</span><span class="sxs-lookup"><span data-stu-id="11567-114">Otherwise, the data may not be filtered as you expect.</span></span>

<span data-ttu-id="11567-115">In vielen Fällen geht es schneller, ein neues **Recordset** -Objekt mithilfe einer SQL-Anweisung zu öffnen, die eine WHERE-Klausel enthält.</span><span class="sxs-lookup"><span data-stu-id="11567-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes a WHERE clause.</span></span>

<span data-ttu-id="11567-116">Wenn Sie die Eigenschaft auf eine Zeichenfolge mit einem nicht-Ganzzahl-Wert verkettet festlegen und die Systemparameter einer US-decimal Zeichen wie etwa ein Komma angeben (beispielsweise StrFilter = "PRICE \> " &-LngPrice und LngPrice = 125,50), ein Fehler tritt auf, wenn Sie versuchen, Öffnen Sie das nächste **Recordset-Objekt**.</span><span class="sxs-lookup"><span data-stu-id="11567-116">If you set the property to a string concatenated with a non–integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strFilter = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the next **Recordset**.</span></span> <span data-ttu-id="11567-117">Dies liegt daran, dass der Wert während der Verkettung mithilfe des Standard-Dezimaltrennzeichens in eine Zeichenfolge konvertiert wird und Microsoft Access SQL nur US-Dezimaltrennzeichen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="11567-117">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

