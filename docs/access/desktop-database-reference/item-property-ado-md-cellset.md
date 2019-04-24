---
title: Item-Eigenschaft (ADO MD-Zellmenge)
TOCTitle: Item property (ADO MD Cellset)
ms:assetid: 47510643-47af-0bfd-dc1f-ab984057bcd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249220(v=office.15)
ms:contentKeyID: 48544595
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 99f381ad2f38dc7d2c467ed1e40e4084032006d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290867"
---
# <a name="item-property-ado-md-cellset"></a><span data-ttu-id="7b891-102">Item-Eigenschaft (ADO MD-Zellmenge)</span><span class="sxs-lookup"><span data-stu-id="7b891-102">Item property (ADO MD Cellset)</span></span>

<span data-ttu-id="7b891-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7b891-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7b891-104">Ruft eine Zelle aus einer Zellmenge mithilfe der entsprechenden Koordinaten ab.</span><span class="sxs-lookup"><span data-stu-id="7b891-104">Retrieves a cell from a cellset using its coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b891-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b891-105">Syntax</span></span>

<span data-ttu-id="7b891-106">*Zellmenge* = \*\* festlegen. Element (*Positionen*)</span><span class="sxs-lookup"><span data-stu-id="7b891-106">Set*Cell* = *Cellset*.Item (*Positions*)</span></span>

## <a name="parameters"></a><span data-ttu-id="7b891-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b891-107">Parameters</span></span>

|<span data-ttu-id="7b891-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b891-108">Parameter</span></span>|<span data-ttu-id="7b891-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b891-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="7b891-110">*Positions*</span><span class="sxs-lookup"><span data-stu-id="7b891-110">*Positions*</span></span> |<span data-ttu-id="7b891-111">Ein **Variant-Array** mit Werten, die eine Zelle eindeutig angeben.</span><span class="sxs-lookup"><span data-stu-id="7b891-111">A **Variant array** of values that uniquely specify a cell.</span></span> <span data-ttu-id="7b891-112">*Positionen* können eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="7b891-112">*Positions* can be one of the following:</span></span><br/><br/><span data-ttu-id="7b891-113">-Ein Array von Positionsnummern</span><span class="sxs-lookup"><span data-stu-id="7b891-113">- An array of position numbers</span></span><br/><span data-ttu-id="7b891-114">-Ein Array von Elementnamen</span><span class="sxs-lookup"><span data-stu-id="7b891-114">- An array of member names</span></span><br/><span data-ttu-id="7b891-115">-Die Ordnungsposition</span><span class="sxs-lookup"><span data-stu-id="7b891-115">- The ordinal position</span></span> |

## <a name="remarks"></a><span data-ttu-id="7b891-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b891-116">Remarks</span></span>

<span data-ttu-id="7b891-p102">Verwenden Sie die **Item**-Eigenschaft, um ein [Cell](cell-object-ado-md.md)-Objekt in einem [Cellset](cellset-object-ado-md.md)-Objekt zurückzugeben. Wenn die **Item**-Eigenschaft die Zelle, die dem Argument *Positions* entspricht, nicht finden kann, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="7b891-p102">Use the **Item** property to return a [Cell](cell-object-ado-md.md) object within a [Cellset](cellset-object-ado-md.md) object. If the **Item** property cannot find the cell corresponding to the *Positions* argument, an error occurs.</span></span>

<span data-ttu-id="7b891-119">Die **Item**-Eigenschaft ist die Standardeigenschaft für das **Cellset**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7b891-119">The **Item** property is the default property for the **Cellset** object.</span></span> <span data-ttu-id="7b891-120">Die folgenden Syntaxformen sind austauschbar:</span><span class="sxs-lookup"><span data-stu-id="7b891-120">The following syntax forms are interchangeable:</span></span>

```vb
    Cellset.Item ( Positions )
    Cellset ( Positions )
```

<span data-ttu-id="7b891-p104">Durch das Argument *Positions* wird angegeben, welche Zelle zurückgegeben wird. Sie können die Zelle anhand ihrer Ordnungsposition oder anhand der einzelnen Achsenpositionen angeben. Wenn Sie die Zelle anhand der Achsenpositionen angeben, können Sie den numerischen Wert der Position oder die Namen der einzelnen Positionselemente angeben.</span><span class="sxs-lookup"><span data-stu-id="7b891-p104">The *Positions* argument specifies which cell to return. You can specify the cell by ordinal position or by the position along each axis. When specifying the cell by position along each axis, you can specify the numeric value of the position or the names of the members for each position.</span></span>

<span data-ttu-id="7b891-p105">Die Ordnungsposition ist eine Zahl, durch die eine Zelle innerhalb der\*\*\*\* Zellmenge eindeutig bestimmt wird. Bei diesem Konzept sind die Zellen in einer\*\*\*\* Zellmenge nummeriert, als wäre die\*\*\*\* Zellmenge ein *p*-dimensionales Array, wobei *p* die Anzahl der Achsen darstellt. Zellen sind zeilenweise strukturiert.</span><span class="sxs-lookup"><span data-stu-id="7b891-p105">The ordinal position is a number that uniquely identifies one cell within the **Cellset**. Conceptually, cells are numbered in a **Cellset** as if the **Cellset** were a *p*-dimensional array, where *p* is the number of axes. Cells are addressed in row-major order.</span></span>

<span data-ttu-id="7b891-p106">Wenn Elementnamen als Zeichenfolgen an **Item** übergeben werden, müssen die Elemente aufsteigend nach numerischen Achsen-IDs sortiert sein. Innerhalb einer Achse müssen die Elemente in Bezug auf die geschachtelten Dimensionen in aufsteigender Reihenfolge aufgeführt sein, d. h. das Element der äußersten Dimension wird zuerst aufgelistet, dann folgen die Elemente der inneren Dimensionen. Jede Dimension sollte durch eine separate Zeichenfolge dargestellt werden, und die einzelnen Elementzeichenfolgen sollten in der Liste durch Kommas voneinander getrennt sein.</span><span class="sxs-lookup"><span data-stu-id="7b891-p106">If member names are passed as strings to **Item**, the members must be listed in increasing order of the numeric axis identifiers. Within an axis, the members must be listed in increasing order of dimension nesting — that is, the outermost dimension's member comes first, followed by members of inner dimensions. Each dimension should be represented by a separate string, and the list of member strings should be separated by commas.</span></span>


> [!NOTE]
> <span data-ttu-id="7b891-p107">[!HINWEIS] Das Abrufen von Zellen nach Elementnamen wird möglicherweise von Ihrem Datenanbieter nicht unterstützt. Weitere Informationen finden Sie in der Anbieterdokumentation.</span><span class="sxs-lookup"><span data-stu-id="7b891-p107">Retrieving cells by member name may not be supported by your data provider. See the documentation for your provider for more information.</span></span>


