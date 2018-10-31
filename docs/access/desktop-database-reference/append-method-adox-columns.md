---
title: Append-Methode (ADOX Columns)
TOCTitle: Append Method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 727634356a08646b1e2757996cc6bf071de07353
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861575"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="b89b3-102">Append-Methode (ADOX Columns)</span><span class="sxs-lookup"><span data-stu-id="b89b3-102">Append Method (ADOX Columns)</span></span>


<span data-ttu-id="b89b3-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b89b3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b89b3-104">Fügt der [Columns](column-object-adox.md)-Auflistung ein neues [Column](columns-collection-adox.md)-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="b89b3-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b89b3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b89b3-105">Syntax</span></span>

<span data-ttu-id="b89b3-106">*Spalten*.</span><span class="sxs-lookup"><span data-stu-id="b89b3-106">*Columns*.</span></span> <span data-ttu-id="b89b3-107">Fügen Sie die*Spalte* \[,*Typ* \] \[,*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="b89b3-107">Append*Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="b89b3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b89b3-108">Parameters</span></span>

  - <span data-ttu-id="b89b3-109">*Column*</span><span class="sxs-lookup"><span data-stu-id="b89b3-109">*Column*</span></span>

  - <span data-ttu-id="b89b3-110">Das anzufügende **Column** -Objekt oder der Name der zu erstellenden und anzufügenden Spalte.</span><span class="sxs-lookup"><span data-stu-id="b89b3-110">The **Column** object to append or the name of the column to create and append.</span></span>

  - <span data-ttu-id="b89b3-111">*Type*</span><span class="sxs-lookup"><span data-stu-id="b89b3-111">*Type*</span></span>

  - <span data-ttu-id="b89b3-112">Optional.</span><span class="sxs-lookup"><span data-stu-id="b89b3-112">Optional.</span></span> <span data-ttu-id="b89b3-113">Ein **Long** -Wert, der den Datentyp der Spalte angibt.</span><span class="sxs-lookup"><span data-stu-id="b89b3-113">A **Long** value that specifies the data type of the column.</span></span> <span data-ttu-id="b89b3-114">Die [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) -Eigenschaft ein **Column** -Objekt entspricht der *Type* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="b89b3-114">The *Type* parameter corresponds to the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property of a **Column** object.</span></span>

  - <span data-ttu-id="b89b3-115">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="b89b3-115">*DefinedSize*</span></span>

  - <span data-ttu-id="b89b3-116">Optional.</span><span class="sxs-lookup"><span data-stu-id="b89b3-116">Optional.</span></span> <span data-ttu-id="b89b3-117">Ein **Long** -Wert, der die Größe einer Spalte angibt.</span><span class="sxs-lookup"><span data-stu-id="b89b3-117">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="b89b3-118">Der Parameter *DefinedSize* entspricht der [DefinedSize](definedsize-property-adox.md) -Eigenschaft eines **Column** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="b89b3-118">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>


> [!NOTE]
> <span data-ttu-id="b89b3-119">[!HINWEIS] Es tritt ein Fehler auf, wenn ein **Column** -Objekt an die **Columns** -Auflistung eines [Index](index-object-adox.md)-Objekts angefügt wird und das **Column** -Objekt nicht in einem [Table](table-object-adox.md)-Objekt vorhanden ist, das bereits an die [Tables](tables-collection-adox.md)-Auflistung angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b89b3-119">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


