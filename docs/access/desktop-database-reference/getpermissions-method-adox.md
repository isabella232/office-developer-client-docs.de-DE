---
title: GetPermissions-Methode (ADOX)
TOCTitle: GetPermissions method (ADOX)
ms:assetid: 98a2b2b6-a8af-15ee-b052-622a6f0661b9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249683(v=office.15)
ms:contentKeyID: 48546496
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa5dda3c8e2ee8251fc54f4ff3bc12be0aca5002
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719743"
---
# <a name="getpermissions-method-adox"></a><span data-ttu-id="8a933-102">GetPermissions-Methode (ADOX)</span><span class="sxs-lookup"><span data-stu-id="8a933-102">GetPermissions method (ADOX)</span></span>

<span data-ttu-id="8a933-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8a933-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8a933-104">Gibt die Berechtigungen einer Gruppe oder eines Benutzers für ein Objekt oder einen Objektcontainers zurück.</span><span class="sxs-lookup"><span data-stu-id="8a933-104">Returns the permissions for a group or user on an object or object container.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a933-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a933-105">Syntax</span></span>

<span data-ttu-id="8a933-106">*ReturnValue* = *Gruppe_oder_benutzer*. GetPermissions (*Name*, *ObjectType* \[,*ObjectTypeId*\])</span><span class="sxs-lookup"><span data-stu-id="8a933-106">*ReturnValue* = *GroupOrUser*.GetPermissions(*Name*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="8a933-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a933-107">Return value</span></span>

<span data-ttu-id="8a933-p101">Gibt einen **Long** -Wert zurück, der eine Bitmaske angibt, die die Berechtigungen enthält, über die die Gruppe oder der Benutzer für das Objekt verfügen. Dieser Wert kann eine bzw. mehrere der [RightsEnum](rightsenum.md)-Konstanten sein.</span><span class="sxs-lookup"><span data-stu-id="8a933-p101">Returns a **Long** value that specifies a bitmask containing the permissions that the group or user has on the object. This value can be one or more of the [RightsEnum](rightsenum.md) constants.</span></span>

## <a name="parameters"></a><span data-ttu-id="8a933-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a933-110">Parameters</span></span>

|<span data-ttu-id="8a933-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a933-111">Parameter</span></span>|<span data-ttu-id="8a933-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a933-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="8a933-113">*Name*</span><span class="sxs-lookup"><span data-stu-id="8a933-113">*Name*</span></span> |<span data-ttu-id="8a933-114">Ein **Variant** -Wert, der den Namen des Objekts angibt, für das Berechtigungen festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8a933-114">A **Variant** value that specifies the name of the object for which to set permissions.</span></span> <span data-ttu-id="8a933-115">Legen Sie *Namen* auf einen null-Wert, wenn Sie die Berechtigungen für den Objektcontainer abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="8a933-115">Set *Name* to a null value if you want to get the permissions for the object container.</span></span>|
|<span data-ttu-id="8a933-116">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="8a933-116">*ObjectType*</span></span> |<span data-ttu-id="8a933-117">Ein **Long** -Wert, der eine der [ObjectTypeEnum](objecttypeenum.md)-Konstanten sein kann, die den Typ des Objekts angibt, für das die Berechtigungen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8a933-117">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>|
|<span data-ttu-id="8a933-118">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="8a933-118">*ObjectTypeId*</span></span> |<span data-ttu-id="8a933-119">Optional.</span><span class="sxs-lookup"><span data-stu-id="8a933-119">Optional.</span></span> <span data-ttu-id="8a933-120">Ein **Variant** -Wert, der die GUID für einen Anbieterobjekttyp angibt, der nicht durch die OLE DB-Spezifikation definiert ist.</span><span class="sxs-lookup"><span data-stu-id="8a933-120">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="8a933-121">Dieser Parameter ist erforderlich, wenn *ObjectType* auf **AdPermObjProviderSpecific**festgelegt ist; Andernfalls wird es nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8a933-121">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

