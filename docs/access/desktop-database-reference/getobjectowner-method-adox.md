---
title: GetObjectOwner-Methode (ADOX)
TOCTitle: GetObjectOwner method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7243e70c95da3502a3c7b86e691858715730a955
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949244"
---
# <a name="getobjectowner-method-adox"></a><span data-ttu-id="a0e93-102">GetObjectOwner-Methode (ADOX)</span><span class="sxs-lookup"><span data-stu-id="a0e93-102">GetObjectOwner method (ADOX)</span></span>

<span data-ttu-id="a0e93-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a0e93-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a0e93-104">Gibt den Besitzer eines Objekts in einem [Catalog](catalog-object-adox.md)-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="a0e93-104">Returns the owner of an object in a [Catalog](catalog-object-adox.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a0e93-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0e93-105">Syntax</span></span>

<span data-ttu-id="a0e93-106">*Besitzer* = *Katalog*. GetObjectOwner (*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span><span class="sxs-lookup"><span data-stu-id="a0e93-106">*Owner* = *Catalog*.GetObjectOwner(*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="a0e93-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0e93-107">Return value</span></span>

<span data-ttu-id="a0e93-108">Gibt einen **String** -Wert zurück, der den [Namen](name-property-adox.md) des [User](user-object-adox.md)- oder [Group](group-object-adox.md)-Objekts angibt, das das Objekt besitzt.</span><span class="sxs-lookup"><span data-stu-id="a0e93-108">Returns a **String** value that specifies the [Name](name-property-adox.md) of the [User](user-object-adox.md) or [Group](group-object-adox.md) that owns the object.</span></span>

## <a name="parameters"></a><span data-ttu-id="a0e93-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0e93-109">Parameters</span></span>

|<span data-ttu-id="a0e93-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0e93-110">Parameter</span></span>|<span data-ttu-id="a0e93-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0e93-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a0e93-112">*ObjectName*</span><span class="sxs-lookup"><span data-stu-id="a0e93-112">*ObjectName*</span></span> |<span data-ttu-id="a0e93-113">Ein **String** -Wert, der den Namen des Objekts angibt, für das der Besitzer zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0e93-113">A **String** value that specifies the name of the object for which to return the owner.</span></span>|
|<span data-ttu-id="a0e93-114">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="a0e93-114">*ObjectType*</span></span> |<span data-ttu-id="a0e93-115">Ein **Long** -Wert, der eine der [ObjectTypeEnum](objecttypeenum.md)-Konstanten sein kann, die den Typ des Objekts angibt, für das der Besitzer zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0e93-115">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get the owner.</span></span>|
|<span data-ttu-id="a0e93-116">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="a0e93-116">*ObjectTypeId*</span></span> |<span data-ttu-id="a0e93-117">Optional.</span><span class="sxs-lookup"><span data-stu-id="a0e93-117">Optional.</span></span> <span data-ttu-id="a0e93-118">Ein **Variant** -Wert, der die GUID für einen Anbieterobjekttyp angibt, der nicht durch die OLE DB-Spezifikation definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a0e93-118">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="a0e93-119">Dieser Parameter ist erforderlich, wenn *ObjectType* auf **AdPermObjProviderSpecific**festgelegt ist; Andernfalls wird es nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0e93-119">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a0e93-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a0e93-120">Remarks</span></span>

<span data-ttu-id="a0e93-121">Wenn der Anbieter nicht die Rückgabe von Objektbesitzern unterstützt, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="a0e93-121">An error will occur if the provider does not support returning object owners.</span></span>

