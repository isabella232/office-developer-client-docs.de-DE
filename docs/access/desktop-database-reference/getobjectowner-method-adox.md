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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710730"
---
# <a name="getobjectowner-method-adox"></a>GetObjectOwner-Methode (ADOX)

**Betrifft**: Access 2013, Office 2013

Gibt den Besitzer eines Objekts in einem [Catalog](catalog-object-adox.md)-Objekt zurück.

## <a name="syntax"></a>Syntax

*Besitzer* = *Katalog*. GetObjectOwner (*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])

## <a name="return-value"></a>Rückgabewert

Gibt einen **String** -Wert zurück, der den [Namen](name-property-adox.md) des [User](user-object-adox.md)- oder [Group](group-object-adox.md)-Objekts angibt, das das Objekt besitzt.

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*ObjectName* |Ein **String** -Wert, der den Namen des Objekts angibt, für das der Besitzer zurückgegeben werden soll.|
|*ObjectType* |Ein **Long** -Wert, der eine der [ObjectTypeEnum](objecttypeenum.md)-Konstanten sein kann, die den Typ des Objekts angibt, für das der Besitzer zurückgegeben werden soll.|
|*ObjectTypeId* |Optional. Ein **Variant** -Wert, der die GUID für einen Anbieterobjekttyp angibt, der nicht durch die OLE DB-Spezifikation definiert ist. Dieser Parameter ist erforderlich, wenn *ObjectType* auf **AdPermObjProviderSpecific**festgelegt ist; Andernfalls wird es nicht verwendet.|

## <a name="remarks"></a>Hinweise

Wenn der Anbieter nicht die Rückgabe von Objektbesitzern unterstützt, tritt ein Fehler auf.

