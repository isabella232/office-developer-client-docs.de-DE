---
title: Append-Methode (ADOX Columns)
TOCTitle: Append method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48bc100b7b56265a570ce963b80f569f1d827150
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711231"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="0821f-102">Append-Methode (ADOX Columns)</span><span class="sxs-lookup"><span data-stu-id="0821f-102">Append method (ADOX Columns)</span></span>

<span data-ttu-id="0821f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0821f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0821f-104">Fügt der [Columns](column-object-adox.md)-Auflistung ein neues [Column](columns-collection-adox.md)-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="0821f-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0821f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0821f-105">Syntax</span></span>

<span data-ttu-id="0821f-106">*Spalten*.</span><span class="sxs-lookup"><span data-stu-id="0821f-106">*Columns*.</span></span> <span data-ttu-id="0821f-107">Fügen Sie die*Spalte* \[,*Typ* \] \[,*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="0821f-107">Append*Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="0821f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0821f-108">Parameters</span></span>

|<span data-ttu-id="0821f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0821f-109">Parameter</span></span>|<span data-ttu-id="0821f-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0821f-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="0821f-111">*Column*</span><span class="sxs-lookup"><span data-stu-id="0821f-111">*Column*</span></span> |<span data-ttu-id="0821f-112">Das anzufügende **Column** -Objekt oder der Name der zu erstellenden und anzufügenden Spalte.</span><span class="sxs-lookup"><span data-stu-id="0821f-112">The **Column** object to append or the name of the column to create and append.</span></span>|
|<span data-ttu-id="0821f-113">*Type*</span><span class="sxs-lookup"><span data-stu-id="0821f-113">*Type*</span></span> |<span data-ttu-id="0821f-114">Optional.</span><span class="sxs-lookup"><span data-stu-id="0821f-114">Optional.</span></span> <span data-ttu-id="0821f-115">Ein **Long** -Wert, der den Datentyp der Spalte angibt.</span><span class="sxs-lookup"><span data-stu-id="0821f-115">A **Long** value that specifies the data type of the column.</span></span> <span data-ttu-id="0821f-116">Die [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) -Eigenschaft ein **Column** -Objekt entspricht der *Type* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="0821f-116">The *Type* parameter corresponds to the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property of a **Column** object.</span></span>|
|<span data-ttu-id="0821f-117">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="0821f-117">*DefinedSize*</span></span> |<span data-ttu-id="0821f-118">Optional.</span><span class="sxs-lookup"><span data-stu-id="0821f-118">Optional.</span></span> <span data-ttu-id="0821f-119">Ein **Long** -Wert, der die Größe einer Spalte angibt.</span><span class="sxs-lookup"><span data-stu-id="0821f-119">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="0821f-120">Der Parameter *DefinedSize* entspricht der [DefinedSize](definedsize-property-adox.md) -Eigenschaft eines **Column** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="0821f-120">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>|


> [!NOTE]
> <span data-ttu-id="0821f-121">[!HINWEIS] Es tritt ein Fehler auf, wenn ein **Column** -Objekt an die **Columns** -Auflistung eines [Index](index-object-adox.md)-Objekts angefügt wird und das **Column** -Objekt nicht in einem [Table](table-object-adox.md)-Objekt vorhanden ist, das bereits an die [Tables](tables-collection-adox.md)-Auflistung angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="0821f-121">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


