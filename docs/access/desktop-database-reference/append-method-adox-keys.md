---
title: Append-Methode (ADOX Keys)
TOCTitle: Append method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d99af00f1ad83087994737f5bb3ca29acf2a9deb
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949817"
---
# <a name="append-method-adox-keys"></a><span data-ttu-id="c9df7-102">Append-Methode (ADOX Keys)</span><span class="sxs-lookup"><span data-stu-id="c9df7-102">Append method (ADOX Keys)</span></span>

<span data-ttu-id="c9df7-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9df7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c9df7-104">Fügt der [Keys](key-object-adox.md)-Auflistung ein neues [Key](keys-collection-adox.md)-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="c9df7-104">Adds a new [Key](key-object-adox.md) object to the [Keys](keys-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9df7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9df7-105">Syntax</span></span>

<span data-ttu-id="c9df7-106">*Schlüssel*. Fügen Sie*Schlüssel* \[,*Schlüsseltyp* \] \[,*Spalte* \] \[,*RelatedTable* \] \[,*RelatedColumn*\]</span><span class="sxs-lookup"><span data-stu-id="c9df7-106">*Keys*.Append*Key* \[,*KeyType*\] \[,*Column*\] \[,*RelatedTable*\] \[,*RelatedColumn*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="c9df7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9df7-107">Parameters</span></span>

|<span data-ttu-id="c9df7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9df7-108">Parameter</span></span>|<span data-ttu-id="c9df7-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9df7-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c9df7-110">*Key*</span><span class="sxs-lookup"><span data-stu-id="c9df7-110">*Key*</span></span> |<span data-ttu-id="c9df7-111">Das anzufügende **Key** -Objekt oder der Name des zu erstellenden und anzufügenden Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="c9df7-111">The **Key** object to append or the name of the key to create and append.</span></span>|
|<span data-ttu-id="c9df7-112">*Schlüsseltyp*</span><span class="sxs-lookup"><span data-stu-id="c9df7-112">*KeyType*</span></span> |<span data-ttu-id="c9df7-113">Optional.</span><span class="sxs-lookup"><span data-stu-id="c9df7-113">Optional.</span></span> <span data-ttu-id="c9df7-114">Ein **Long** -Wert, der den Schlüsseltyp angibt.</span><span class="sxs-lookup"><span data-stu-id="c9df7-114">A **Long** value that specifies the type of key.</span></span> <span data-ttu-id="c9df7-115">Der Parameter *Schlüssel* entspricht der [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) -Eigenschaft eines **Key** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="c9df7-115">The *Key* parameter corresponds to the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) property of a **Key** object.</span></span>|
|<span data-ttu-id="c9df7-116">*Column*</span><span class="sxs-lookup"><span data-stu-id="c9df7-116">*Column*</span></span> |<span data-ttu-id="c9df7-117">Optional.</span><span class="sxs-lookup"><span data-stu-id="c9df7-117">Optional.</span></span> <span data-ttu-id="c9df7-118">Ein **String** -Wert, der den Namen der zu indizierenden Spalte angibt.</span><span class="sxs-lookup"><span data-stu-id="c9df7-118">A **String** value that specifies the name of the column to be indexed.</span></span> <span data-ttu-id="c9df7-119">Der *Columns* -Parameter entspricht dem Wert der [Name](name-property-adox.md) -Eigenschaft eines [Column](column-object-adox.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="c9df7-119">The *Columns* parameter corresponds to the value of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object.</span></span>|
|<span data-ttu-id="c9df7-120">*RelatedTable*</span><span class="sxs-lookup"><span data-stu-id="c9df7-120">*RelatedTable*</span></span> |<span data-ttu-id="c9df7-121">Optional.</span><span class="sxs-lookup"><span data-stu-id="c9df7-121">Optional.</span></span> <span data-ttu-id="c9df7-122">Ein **String** -Wert, der den Namen der verknüpften Tabelle angibt.</span><span class="sxs-lookup"><span data-stu-id="c9df7-122">A **String** value that specifies the name of the related table.</span></span> <span data-ttu-id="c9df7-123">Der Parameter *RelatedTable* entspricht dem Wert der **Name** -Eigenschaft eines [Table](table-object-adox.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="c9df7-123">The *RelatedTable* parameter corresponds to the value of the **Name** property of a [Table](table-object-adox.md) object.</span></span>|
|<span data-ttu-id="c9df7-124">*RelatedColumn*</span><span class="sxs-lookup"><span data-stu-id="c9df7-124">*RelatedColumn*</span></span> |<span data-ttu-id="c9df7-p104">Optional. Ein String-Wert, der den Namen der verknüpften Spalte für einen Fremdschlüssel angibt. Der RelatedColumn-Parameter entspricht dem Wert der Name-Eigenschaft eines Column-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c9df7-p104">Optional. A **String** value that specifies the name of the related column for a foreign key. The RelatedColumn parameter corresponds to the value of the **Name** property of a **Column** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="c9df7-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c9df7-128">Remarks</span></span>

<span data-ttu-id="c9df7-129">Der *Columns* -Parameter kann entweder den Namen einer Spalte oder ein Array von Spaltennamen dauern.</span><span class="sxs-lookup"><span data-stu-id="c9df7-129">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

