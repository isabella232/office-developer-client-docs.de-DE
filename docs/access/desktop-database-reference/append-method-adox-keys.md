---
title: Append-Methode (ADOX Keys)
TOCTitle: Append Method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d7e10e272155d2d0377810bf8aa1704a30bad39
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475539"
---
# <a name="append-method-adox-keys"></a><span data-ttu-id="64549-102">Append-Methode (ADOX Keys)</span><span class="sxs-lookup"><span data-stu-id="64549-102">Append Method (ADOX Keys)</span></span>


<span data-ttu-id="64549-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="64549-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="64549-104">Fügt der [Keys](key-object-adox.md)-Auflistung ein neues [Key](keys-collection-adox.md)-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="64549-104">Adds a new [Key](key-object-adox.md) object to the [Keys](keys-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="64549-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="64549-105">Syntax</span></span>

<span data-ttu-id="64549-106">*Schlüssel*. Fügen Sie*Schlüssel* \[,*Schlüsseltyp* \] \[,*Spalte* \] \[,*RelatedTable* \] \[,*RelatedColumn*\]</span><span class="sxs-lookup"><span data-stu-id="64549-106">*Keys*.Append*Key* \[,*KeyType*\] \[,*Column*\] \[,*RelatedTable*\] \[,*RelatedColumn*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="64549-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="64549-107">Parameters</span></span>

  - <span data-ttu-id="64549-108">*Key*</span><span class="sxs-lookup"><span data-stu-id="64549-108">*Key*</span></span>

  - <span data-ttu-id="64549-109">Das anzufügende **Key** -Objekt oder der Name des zu erstellenden und anzufügenden Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="64549-109">The **Key** object to append or the name of the key to create and append.</span></span>

  - <span data-ttu-id="64549-110">*Schlüsseltyp*</span><span class="sxs-lookup"><span data-stu-id="64549-110">*KeyType*</span></span>

  - <span data-ttu-id="64549-111">Optional.</span><span class="sxs-lookup"><span data-stu-id="64549-111">Optional.</span></span> <span data-ttu-id="64549-112">Ein **Long** -Wert, der den Schlüsseltyp angibt.</span><span class="sxs-lookup"><span data-stu-id="64549-112">A **Long** value that specifies the type of key.</span></span> <span data-ttu-id="64549-113">Der Parameter *Schlüssel* entspricht der [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) -Eigenschaft eines **Key** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="64549-113">The *Key* parameter corresponds to the [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) property of a **Key** object.</span></span>

  - <span data-ttu-id="64549-114">*Column*</span><span class="sxs-lookup"><span data-stu-id="64549-114">*Column*</span></span>

  - <span data-ttu-id="64549-115">Optional.</span><span class="sxs-lookup"><span data-stu-id="64549-115">Optional.</span></span> <span data-ttu-id="64549-116">Ein **String** -Wert, der den Namen der zu indizierenden Spalte angibt.</span><span class="sxs-lookup"><span data-stu-id="64549-116">A **String** value that specifies the name of the column to be indexed.</span></span> <span data-ttu-id="64549-117">Der *Columns* -Parameter entspricht dem Wert der [Name](name-property-adox.md) -Eigenschaft eines [Column](column-object-adox.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="64549-117">The *Columns* parameter corresponds to the value of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object.</span></span>

  - <span data-ttu-id="64549-118">*RelatedTable*</span><span class="sxs-lookup"><span data-stu-id="64549-118">*RelatedTable*</span></span>

  - <span data-ttu-id="64549-119">Optional.</span><span class="sxs-lookup"><span data-stu-id="64549-119">Optional.</span></span> <span data-ttu-id="64549-120">Ein **String** -Wert, der den Namen der verknüpften Tabelle angibt.</span><span class="sxs-lookup"><span data-stu-id="64549-120">A **String** value that specifies the name of the related table.</span></span> <span data-ttu-id="64549-121">Der Parameter *RelatedTable* entspricht dem Wert der **Name** -Eigenschaft eines [Table](table-object-adox.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="64549-121">The *RelatedTable* parameter corresponds to the value of the **Name** property of a [Table](table-object-adox.md) object.</span></span>

  - <span data-ttu-id="64549-122">*RelatedColumn*</span><span class="sxs-lookup"><span data-stu-id="64549-122">*RelatedColumn*</span></span>

  - <span data-ttu-id="64549-p104">Optional. Ein String-Wert, der den Namen der verknüpften Spalte für einen Fremdschlüssel angibt. Der RelatedColumn-Parameter entspricht dem Wert der Name-Eigenschaft eines Column-Objekts.</span><span class="sxs-lookup"><span data-stu-id="64549-p104">Optional. A **String** value that specifies the name of the related column for a foreign key. The RelatedColumn parameter corresponds to the value of the **Name** property of a **Column** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="64549-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="64549-126">Remarks</span></span>

<span data-ttu-id="64549-127">Der *Columns* -Parameter kann entweder den Namen einer Spalte oder ein Array von Spaltennamen dauern.</span><span class="sxs-lookup"><span data-stu-id="64549-127">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

