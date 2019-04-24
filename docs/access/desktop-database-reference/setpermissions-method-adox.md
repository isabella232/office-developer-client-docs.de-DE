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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314581"
---
# <a name="setpermissions-method-adox"></a><span data-ttu-id="36cd4-102">SetPermissions-Methode (ADOX)</span><span class="sxs-lookup"><span data-stu-id="36cd4-102">SetPermissions method (ADOX)</span></span>

<span data-ttu-id="36cd4-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="36cd4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="36cd4-104">Gibt die Berechtigungen für eine Gruppe oder einen Benutzer für ein Objekt an.</span><span class="sxs-lookup"><span data-stu-id="36cd4-104">Specifies the permissions for a group or user on an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="36cd4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="36cd4-105">Syntax</span></span>

<span data-ttu-id="36cd4-106">*GroupOrUser*. SetPermissions*Name*, ObjectType, *Action*, *Rights* \[,*inherit* \] \[, \*\* objecttyper\*\*\]</span><span class="sxs-lookup"><span data-stu-id="36cd4-106">*GroupOrUser*.SetPermissions*Name*, *ObjectType*, *Action*, *Rights* \[,*Inherit*\] \[,*ObjectTypeId*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="36cd4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="36cd4-107">Parameters</span></span>

|<span data-ttu-id="36cd4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="36cd4-108">Parameter</span></span>|<span data-ttu-id="36cd4-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36cd4-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="36cd4-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="36cd4-110">*Name*</span></span> |<span data-ttu-id="36cd4-111">Ein **String** -Wert, der den Namen des Objekts angibt, für das Berechtigungen festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="36cd4-111">A **String** value that specifies the name of the object for which to set permissions.</span></span>|
|<span data-ttu-id="36cd4-112">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="36cd4-112">*ObjectType*</span></span> |<span data-ttu-id="36cd4-113">Ein **Long** -Wert, der eine der [ObjectTypeEnum](objecttypeenum.md)-Konstanten sein kann, die den Typ des Objekts angibt, für das die Berechtigungen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="36cd4-113">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>|
|<span data-ttu-id="36cd4-114">*Action*</span><span class="sxs-lookup"><span data-stu-id="36cd4-114">*Action*</span></span> |<span data-ttu-id="36cd4-115">Ein **Long** -Wert, der eine der [ActionEnum](actionenum.md)-Konstanten sein kann, die den Aktionstyp angibt, der beim Festlegen der Berechtigungen ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="36cd4-115">A **Long** value which can be one of the [ActionEnum](actionenum.md) constants that specifies the type of action to perform when setting permissions.</span></span>|
|<span data-ttu-id="36cd4-116">*Rights*</span><span class="sxs-lookup"><span data-stu-id="36cd4-116">*Rights*</span></span> |<span data-ttu-id="36cd4-117">Ein **Long** -Wert, der eine Bitmaske einer oder mehrerer [RightsEnum](rightsenum.md)-Konstanten sein kann, die die festzulegenden Rechte angibt.</span><span class="sxs-lookup"><span data-stu-id="36cd4-117">A **Long** value which can be a bitmask of one or more of the [RightsEnum](rightsenum.md) constants, that indicates the rights to set.</span></span>|
|<span data-ttu-id="36cd4-118">*Inherit*</span><span class="sxs-lookup"><span data-stu-id="36cd4-118">*Inherit*</span></span> |<span data-ttu-id="36cd4-p101">Optional. Ein **Long** -Wert, der eine der [InheritTypeEnum](inherittypeenum.md)-Konstanten sein kann, die angibt, wie Objekte diese Berechtigungen erben. Der Standardwert lautet **adInheritNone**.</span><span class="sxs-lookup"><span data-stu-id="36cd4-p101">Optional. A **Long** value which can be one of the [InheritTypeEnum](inherittypeenum.md) constants, that specifies how objects will inherit these permissions. The default value is **adInheritNone**.</span></span>|
|<span data-ttu-id="36cd4-122">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="36cd4-122">*ObjectTypeId*</span></span> |<span data-ttu-id="36cd4-p102">Optional. Ein **Variant**-Wert, der die GUID für einen Anbieterobjekttyp angibt, der nicht durch die OLE DB-Spezifikation definiert ist. Dieser Parameter ist erforderlich, wenn *ObjectType* auf **adPermObjProviderSpecific** festgelegt ist. Andernfalls wird dieser Parameter nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="36cd4-p102">Optional. A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification. This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="36cd4-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36cd4-126">Remarks</span></span>

<span data-ttu-id="36cd4-127">Wenn der Anbieter das Festlegen von Zugriffsrechten für Gruppen oder Benutzer nicht unterstützt, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="36cd4-127">An error will occur if the provider does not support setting access rights for groups or users.</span></span>

> [!NOTE]
> <span data-ttu-id="36cd4-128">Wenn Sie \*\*\*\* SetPermissions aufrufen, werden beim Festlegen von Aktionen auf **adAccessRevoke** alle Einstellungen des *Rights* -Parameters überschrieben.</span><span class="sxs-lookup"><span data-stu-id="36cd4-128">When calling **SetPermissions**, setting Actions to **adAccessRevoke** overrides any settings of the *Rights* parameter.</span></span> <span data-ttu-id="36cd4-129">Legen Sie keine *Aktionen* auf **adAccessRevoke** fest, wenn die im *Rights* -Parameter angegebenen Rechte wirksam werden sollen.</span><span class="sxs-lookup"><span data-stu-id="36cd4-129">Do not set *Actions* to **adAccessRevoke** if you want the rights specified in the *Rights* parameter to take effect.</span></span>


