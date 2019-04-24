---
title: GetObjectOwner-Methode (ADOX)
TOCTitle: GetObjectOwner method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 948464534f9bbfbea50c8eba2c926dea9cb9bcac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292258"
---
# <a name="getobjectowner-method-adox"></a><span data-ttu-id="54395-102">GetObjectOwner-Methode (ADOX)</span><span class="sxs-lookup"><span data-stu-id="54395-102">GetObjectOwner method (ADOX)</span></span>

<span data-ttu-id="54395-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="54395-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="54395-104">Gibt den Besitzer eines Objekts in einem [Catalog](catalog-object-adox.md)-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="54395-104">Returns the owner of an object in a [Catalog](catalog-object-adox.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="54395-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="54395-105">Syntax</span></span>

<span data-ttu-id="54395-106">*Besitzer* = *Katalog*. GetObjectOwner (*objectName*, *Objekttyp* \[, objecttypecode)\*\*\]</span><span class="sxs-lookup"><span data-stu-id="54395-106">*Owner* = *Catalog*.GetObjectOwner(*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="54395-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54395-107">Return value</span></span>

<span data-ttu-id="54395-108">Gibt einen **String**-Wert zurück, der den [Namen](name-property-adox.md) des [User](user-object-adox.md)- oder [Group](group-object-adox.md)-Objekts angibt, das das Objekt besitzt.</span><span class="sxs-lookup"><span data-stu-id="54395-108">Returns a **String** value that specifies the [Name](name-property-adox.md) of the [User](user-object-adox.md) or [Group](group-object-adox.md) that owns the object.</span></span>

## <a name="parameters"></a><span data-ttu-id="54395-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="54395-109">Parameters</span></span>

|<span data-ttu-id="54395-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="54395-110">Parameter</span></span>|<span data-ttu-id="54395-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54395-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="54395-112">*ObjectName*</span><span class="sxs-lookup"><span data-stu-id="54395-112">*ObjectName*</span></span> |<span data-ttu-id="54395-113">Ein **String** -Wert, der den Namen des Objekts angibt, für das der Besitzer zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="54395-113">A **String** value that specifies the name of the object for which to return the owner.</span></span>|
|<span data-ttu-id="54395-114">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="54395-114">*ObjectType*</span></span> |<span data-ttu-id="54395-115">Ein **Long** -Wert, der eine der [ObjectTypeEnum](objecttypeenum.md)-Konstanten sein kann, die den Typ des Objekts angibt, für das der Besitzer zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="54395-115">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get the owner.</span></span>|
|<span data-ttu-id="54395-116">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="54395-116">*ObjectTypeId*</span></span> |<span data-ttu-id="54395-p101">Optional. Ein **Variant**-Wert, der die GUID für einen Anbieterobjekttyp angibt, der nicht durch die OLE DB-Spezifikation definiert ist. Dieser Parameter ist erforderlich, wenn *ObjectType* auf **adPermObjProviderSpecific** festgelegt ist. Andernfalls wird dieser Parameter nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="54395-p101">Optional. A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification. This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="54395-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54395-120">Remarks</span></span>

<span data-ttu-id="54395-121">Wenn der Anbieter nicht die Rückgabe von Objektbesitzern unterstützt, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="54395-121">An error will occur if the provider does not support returning object owners.</span></span>

