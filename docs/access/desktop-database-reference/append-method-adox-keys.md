---
title: Append-Methode (ADOX Keys)
TOCTitle: Append method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c301f6809ab7f785497637b12e0b5d7a0bb7772d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297088"
---
# <a name="append-method-adox-keys"></a><span data-ttu-id="55e72-102">Append-Methode (ADOX Keys)</span><span class="sxs-lookup"><span data-stu-id="55e72-102">Append method (ADOX Keys)</span></span>

<span data-ttu-id="55e72-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="55e72-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="55e72-104">Fügt der [Keys](key-object-adox.md)-Auflistung ein neues [Key](keys-collection-adox.md)-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="55e72-104">Adds a new [Key](key-object-adox.md) object to the [Keys](keys-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="55e72-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="55e72-105">Syntax</span></span>

<span data-ttu-id="55e72-106">*Schlüssel*. Append *-Taste* \[, KeyType\*\* \] \[,*Column* \] \[,*relatedable* \] \[,*RelatedColumn*\]</span><span class="sxs-lookup"><span data-stu-id="55e72-106">*Keys*.Append*Key* \[,*KeyType*\] \[,*Column*\] \[,*RelatedTable*\] \[,*RelatedColumn*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="55e72-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="55e72-107">Parameters</span></span>

|<span data-ttu-id="55e72-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="55e72-108">Parameter</span></span>|<span data-ttu-id="55e72-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="55e72-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="55e72-110">*Key*</span><span class="sxs-lookup"><span data-stu-id="55e72-110">*Key*</span></span> |<span data-ttu-id="55e72-111">Das anzufügende **Key** -Objekt oder der Name des zu erstellenden und anzufügenden Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="55e72-111">The **Key** object to append or the name of the key to create and append.</span></span>|
|<span data-ttu-id="55e72-112">*KeyType*</span><span class="sxs-lookup"><span data-stu-id="55e72-112">*KeyType*</span></span> |<span data-ttu-id="55e72-113">Optional.</span><span class="sxs-lookup"><span data-stu-id="55e72-113">Optional.</span></span> <span data-ttu-id="55e72-114">Ein **Long**-Wert, der den Schlüsseltyp angibt.</span><span class="sxs-lookup"><span data-stu-id="55e72-114">A **Long** value that specifies the type of key.</span></span> <span data-ttu-id="55e72-115">Der *Key*-Parameter entspricht der [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox)-Eigenschaft eines **Key**-Objekts.</span><span class="sxs-lookup"><span data-stu-id="55e72-115">The *Key* parameter corresponds to the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) property of a **Key** object.</span></span>|
|<span data-ttu-id="55e72-116">*Spalte*</span><span class="sxs-lookup"><span data-stu-id="55e72-116">*Column*</span></span> |<span data-ttu-id="55e72-p102">Optional. Ein **String**-Wert, der den Namen der zu indizierenden Spalte angibt. Der *Columns*-Parameter entspricht dem Wert der [Name](name-property-adox.md)-Eigenschaft eines [Column](column-object-adox.md)-Objekts.</span><span class="sxs-lookup"><span data-stu-id="55e72-p102">Optional. A **String** value that specifies the name of the column to be indexed. The *Columns* parameter corresponds to the value of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object.</span></span>|
|<span data-ttu-id="55e72-120">*RelatedTable*</span><span class="sxs-lookup"><span data-stu-id="55e72-120">*RelatedTable*</span></span> |<span data-ttu-id="55e72-p103">Optional. Ein **String**-Wert, der den Namen der verknüpften Tabelle angibt. Der *RelatedTable*-Parameter entspricht dem Wert der **Name**-Eigenschaft eines [Table](table-object-adox.md)-Objekts.</span><span class="sxs-lookup"><span data-stu-id="55e72-p103">Optional. A **String** value that specifies the name of the related table. The *RelatedTable* parameter corresponds to the value of the **Name** property of a [Table](table-object-adox.md) object.</span></span>|
|<span data-ttu-id="55e72-124">*RelatedColumn*</span><span class="sxs-lookup"><span data-stu-id="55e72-124">*RelatedColumn*</span></span> |<span data-ttu-id="55e72-p104">Optional. A **String** value that specifies the name of the related column for a foreign key. The RelatedColumn parameter corresponds to the value of the **Name** property of a **Column** object.</span><span class="sxs-lookup"><span data-stu-id="55e72-p104">Optional. A **String** value that specifies the name of the related column for a foreign key. The RelatedColumn parameter corresponds to the value of the **Name** property of a **Column** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="55e72-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55e72-128">Remarks</span></span>

<span data-ttu-id="55e72-129">Der *Columns*-Parameter kann entweder den Namen einer Spalte oder einen Array von Spaltennamen festlegen.</span><span class="sxs-lookup"><span data-stu-id="55e72-129">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

