---
title: Append-Methode (ADOX Columns)
TOCTitle: Append Method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f64f3b04df989348173ad2fc975dcefbd1114b2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473114"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="b9016-102">Append-Methode (ADOX Columns)</span><span class="sxs-lookup"><span data-stu-id="b9016-102">Append Method (ADOX Columns)</span></span>


<span data-ttu-id="b9016-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b9016-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b9016-104">Fügt der [Columns](column-object-adox.md)-Auflistung ein neues [Column](columns-collection-adox.md)-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="b9016-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9016-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9016-105">Syntax</span></span>

<span data-ttu-id="b9016-106">*Spalten*.</span><span class="sxs-lookup"><span data-stu-id="b9016-106">*Columns*.</span></span> <span data-ttu-id="b9016-107">Fügen Sie die*Spalte* \[,*Typ* \] \[,*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="b9016-107">Append*Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="b9016-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9016-108">Parameters</span></span>

  - <span data-ttu-id="b9016-109">*Column*</span><span class="sxs-lookup"><span data-stu-id="b9016-109">*Column*</span></span>

  - <span data-ttu-id="b9016-110">Das anzufügende **Column** -Objekt oder der Name der zu erstellenden und anzufügenden Spalte.</span><span class="sxs-lookup"><span data-stu-id="b9016-110">The **Column** object to append or the name of the column to create and append.</span></span>

  - <span data-ttu-id="b9016-111">*Type*</span><span class="sxs-lookup"><span data-stu-id="b9016-111">*Type*</span></span>

  - <span data-ttu-id="b9016-112">Optional.</span><span class="sxs-lookup"><span data-stu-id="b9016-112">Optional.</span></span> <span data-ttu-id="b9016-113">Ein **Long** -Wert, der den Datentyp der Spalte angibt.</span><span class="sxs-lookup"><span data-stu-id="b9016-113">A **Long** value that specifies the data type of the column.</span></span> <span data-ttu-id="b9016-114">Die [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) -Eigenschaft ein **Column** -Objekt entspricht der *Type* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="b9016-114">The *Type* parameter corresponds to the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property of a **Column** object.</span></span>

  - <span data-ttu-id="b9016-115">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="b9016-115">*DefinedSize*</span></span>

  - <span data-ttu-id="b9016-116">Optional.</span><span class="sxs-lookup"><span data-stu-id="b9016-116">Optional.</span></span> <span data-ttu-id="b9016-117">Ein **Long** -Wert, der die Größe einer Spalte angibt.</span><span class="sxs-lookup"><span data-stu-id="b9016-117">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="b9016-118">Der Parameter *DefinedSize* entspricht der [DefinedSize](definedsize-property-adox.md) -Eigenschaft eines **Column** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="b9016-118">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b9016-119">[!HINWEIS] Es tritt ein Fehler auf, wenn ein <STRONG>Column</STRONG> -Objekt an die <STRONG>Columns</STRONG> -Auflistung eines <A href="index-object-adox.md">Index</A>-Objekts angefügt wird und das <STRONG>Column</STRONG> -Objekt nicht in einem <A href="table-object-adox.md">Table</A>-Objekt vorhanden ist, das bereits an die <A href="tables-collection-adox.md">Tables</A>-Auflistung angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b9016-119">An error will occur when appending a <STRONG>Column</STRONG> to the <STRONG>Columns</STRONG> collection of an <A href="index-object-adox.md">Index</A> if the <STRONG>Column</STRONG> does not exist in a <A href="table-object-adox.md">Table</A> that is already appended to the <A href="tables-collection-adox.md">Tables</A> collection.</span></span></P>


