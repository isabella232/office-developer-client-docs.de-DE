---
title: SetPermissions-Methode (ADOX)
TOCTitle: SetPermissions method (ADOX)
ms:assetid: 63d1053d-fb32-456b-ae67-3a4e45aa01af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249382(v=office.15)
ms:contentKeyID: 48545274
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f9b393e90d579c131865b112263efd0aef3216b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710286"
---
# <a name="setpermissions-method-adox"></a><span data-ttu-id="8d1fb-102">SetPermissions-Methode (ADOX)</span><span class="sxs-lookup"><span data-stu-id="8d1fb-102">SetPermissions method (ADOX)</span></span>

<span data-ttu-id="8d1fb-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d1fb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8d1fb-104">Gibt die Berechtigungen für eine Gruppe oder einen Benutzer für ein Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8d1fb-104">Specifies the permissions for a group or user on an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d1fb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d1fb-105">Syntax</span></span>

<span data-ttu-id="8d1fb-106">*Gruppe_oder_benutzer*. SetPermissions*Name*, *ObjectType*, *Action*, *Rechte* \[,*erben* \] \[,*ObjectTypeId*\]</span><span class="sxs-lookup"><span data-stu-id="8d1fb-106">*GroupOrUser*.SetPermissions*Name*, *ObjectType*, *Action*, *Rights* \[,*Inherit*\] \[,*ObjectTypeId*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="8d1fb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d1fb-107">Parameters</span></span>

|<span data-ttu-id="8d1fb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d1fb-108">Parameter</span></span>|<span data-ttu-id="8d1fb-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d1fb-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="8d1fb-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="8d1fb-110">*Name*</span></span> |<span data-ttu-id="8d1fb-111">Ein **String** -Wert, der den Namen des Objekts angibt, für das Berechtigungen festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8d1fb-111">A **String** value that specifies the name of the object for which to set permissions.</span></span>|
|<span data-ttu-id="8d1fb-112">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="8d1fb-112">*ObjectType*</span></span> |<span data-ttu-id="8d1fb-113">Ein **Long** -Wert, der eine der [ObjectTypeEnum](objecttypeenum.md)-Konstanten sein kann, die den Typ des Objekts angibt, für das die Berechtigungen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8d1fb-113">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>|
|<span data-ttu-id="8d1fb-114">*Action*</span><span class="sxs-lookup"><span data-stu-id="8d1fb-114">*Action*</span></span> |<span data-ttu-id="8d1fb-115">Ein **Long** -Wert, der eine der [ActionEnum](actionenum.md)-Konstanten sein kann, die den Aktionstyp angibt, der beim Festlegen der Berechtigungen ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8d1fb-115">A **Long** value which can be one of the [ActionEnum](actionenum.md) constants that specifies the type of action to perform when setting permissions.</span></span>|
|<span data-ttu-id="8d1fb-116">*Rights*</span><span class="sxs-lookup"><span data-stu-id="8d1fb-116">*Rights*</span></span> |<span data-ttu-id="8d1fb-117">Ein **Long** -Wert, der eine Bitmaske einer oder mehrerer [RightsEnum](rightsenum.md)-Konstanten sein kann, die die festzulegenden Rechte angibt.</span><span class="sxs-lookup"><span data-stu-id="8d1fb-117">A **Long** value which can be a bitmask of one or more of the [RightsEnum](rightsenum.md) constants, that indicates the rights to set.</span></span>|
|<span data-ttu-id="8d1fb-118">*Inherit*</span><span class="sxs-lookup"><span data-stu-id="8d1fb-118">*Inherit*</span></span> |<span data-ttu-id="8d1fb-p101">Optional. Ein **Long** -Wert, der eine der [InheritTypeEnum](inherittypeenum.md)-Konstanten sein kann, die angibt, wie Objekte diese Berechtigungen erben. Der Standardwert lautet **adInheritNone**.</span><span class="sxs-lookup"><span data-stu-id="8d1fb-p101">Optional. A **Long** value which can be one of the [InheritTypeEnum](inherittypeenum.md) constants, that specifies how objects will inherit these permissions. The default value is **adInheritNone**.</span></span>|
|<span data-ttu-id="8d1fb-122">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="8d1fb-122">*ObjectTypeId*</span></span> |<span data-ttu-id="8d1fb-123">Optional.</span><span class="sxs-lookup"><span data-stu-id="8d1fb-123">Optional.</span></span> <span data-ttu-id="8d1fb-124">Ein **Variant** -Wert, der die GUID für einen Anbieterobjekttyp angibt, der nicht durch die OLE DB-Spezifikation definiert ist.</span><span class="sxs-lookup"><span data-stu-id="8d1fb-124">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="8d1fb-125">Dieser Parameter ist erforderlich, wenn *ObjectType* auf **AdPermObjProviderSpecific**festgelegt ist; Andernfalls wird es nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8d1fb-125">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="8d1fb-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8d1fb-126">Remarks</span></span>

<span data-ttu-id="8d1fb-127">Wenn der Anbieter das Festlegen von Zugriffsrechten für Gruppen oder Benutzer nicht unterstützt, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="8d1fb-127">An error will occur if the provider does not support setting access rights for groups or users.</span></span>

> [!NOTE]
> <span data-ttu-id="8d1fb-p103">Beim Aufrufen von SetPermissions werden durch das Festlegen von Actions auf adAccessRevoke alle Einstellungen der Rights-Parameter überschrieben. Legen Sie Actions nicht auf adAccessRevoke fest, wenn die im Rights-Parameter angegebenen Berechtigungen wirksam werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8d1fb-p103">When calling **SetPermissions**, setting Actions to **adAccessRevoke** overrides any settings of the *Rights* parameter. Do not set *Actions* to **adAccessRevoke** if you want the rights specified in the *Rights* parameter to take effect.</span></span>


