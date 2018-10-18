---
title: GetObjectOwner-Methode (ADOX)
TOCTitle: GetObjectOwner Method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e6c2432370f2480484cf1165249bc8573b27372
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603112"
---
# <a name="getobjectowner-method-adox"></a><span data-ttu-id="5a149-102">GetObjectOwner-Methode (ADOX)</span><span class="sxs-lookup"><span data-stu-id="5a149-102">GetObjectOwner Method (ADOX)</span></span>


<span data-ttu-id="5a149-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5a149-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="5a149-104">Gibt den Besitzer eines Objekts in einem [Catalog](catalog-object-adox.md)-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="5a149-104">Returns the owner of an object in a [Catalog](catalog-object-adox.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5a149-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a149-105">Syntax</span></span>

<span data-ttu-id="5a149-106">*Besitzer* = *Katalog*. GetObjectOwner (*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span><span class="sxs-lookup"><span data-stu-id="5a149-106">*Owner* = *Catalog*.GetObjectOwner(*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

<span data-ttu-id="5a149-107"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="5a149-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="5a149-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a149-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="5a149-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a149-109">Return value</span></span>
>>>>>>> <span data-ttu-id="5a149-110">master</span><span class="sxs-lookup"><span data-stu-id="5a149-110">master</span></span>

<span data-ttu-id="5a149-111">Gibt einen **String** -Wert zurück, der den [Namen](name-property-adox.md) des [User](user-object-adox.md)- oder [Group](group-object-adox.md)-Objekts angibt, das das Objekt besitzt.</span><span class="sxs-lookup"><span data-stu-id="5a149-111">Returns a **String** value that specifies the [Name](name-property-adox.md) of the [User](user-object-adox.md) or [Group](group-object-adox.md) that owns the object.</span></span>

## <a name="parameters"></a><span data-ttu-id="5a149-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a149-112">Parameters</span></span>

  - <span data-ttu-id="5a149-113">*ObjectName*</span><span class="sxs-lookup"><span data-stu-id="5a149-113">*ObjectName*</span></span>

  - <span data-ttu-id="5a149-114">Ein **String** -Wert, der den Namen des Objekts angibt, für das der Besitzer zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a149-114">A **String** value that specifies the name of the object for which to return the owner.</span></span>

  - <span data-ttu-id="5a149-115">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="5a149-115">*ObjectType*</span></span>

  - <span data-ttu-id="5a149-116">Ein **Long** -Wert, der eine der [ObjectTypeEnum](objecttypeenum.md)-Konstanten sein kann, die den Typ des Objekts angibt, für das der Besitzer zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a149-116">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get the owner.</span></span>

  - <span data-ttu-id="5a149-117">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="5a149-117">*ObjectTypeId*</span></span>

  - <span data-ttu-id="5a149-118">Optional.</span><span class="sxs-lookup"><span data-stu-id="5a149-118">Optional.</span></span> <span data-ttu-id="5a149-119">Ein **Variant** -Wert, der die GUID für einen Anbieterobjekttyp angibt, der nicht durch die OLE DB-Spezifikation definiert ist.</span><span class="sxs-lookup"><span data-stu-id="5a149-119">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="5a149-120">Dieser Parameter ist erforderlich, wenn *ObjectType* auf **AdPermObjProviderSpecific**festgelegt ist; Andernfalls wird es nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="5a149-120">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a149-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5a149-121">Remarks</span></span>

<span data-ttu-id="5a149-122">Wenn der Anbieter nicht die Rückgabe von Objektbesitzern unterstützt, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="5a149-122">An error will occur if the provider does not support returning object owners.</span></span>

