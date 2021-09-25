---
title: GetObjectOwner-Methode (ADOX)
TOCTitle: GetObjectOwner method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 215546377e085dfb1385b2f00ed882b9d3e85179
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568964"
---
# <a name="getobjectowner-method-adox"></a>GetObjectOwner-Methode (ADOX)

**Gilt für**: Access 2013, Office 2013

Gibt den Besitzer eines Objekts in einem [Catalog](catalog-object-adox.md)-Objekt zurück.

## <a name="syntax"></a>Syntax

*Besitzer*  =  *Catalog*. GetObjectOwner(*ObjectName*, *ObjectType* \[ ,*ObjectTypeId* \] )

## <a name="return-value"></a>Rückgabewert

Gibt einen **String**-Wert zurück, der den [Namen](name-property-adox.md) des [User](user-object-adox.md)- oder [Group](group-object-adox.md)-Objekts angibt, das das Objekt besitzt.

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*ObjectName* |Ein **String** -Wert, der den Namen des Objekts angibt, für das der Besitzer zurückgegeben werden soll.|
|*ObjectType* |Ein **Long** -Wert, der eine der [ObjectTypeEnum](objecttypeenum.md)-Konstanten sein kann, die den Typ des Objekts angibt, für das der Besitzer zurückgegeben werden soll.|
|*ObjectTypeId* |Optional. Ein **Variant**-Wert, der die GUID für einen Anbieterobjekttyp angibt, der nicht durch die OLE DB-Spezifikation definiert ist. Dieser Parameter ist erforderlich, wenn *ObjectType* auf **adPermObjProviderSpecific** festgelegt ist. Andernfalls wird dieser Parameter nicht verwendet.|

## <a name="remarks"></a>HinwBemerkungeneise

Wenn der Anbieter nicht die Rückgabe von Objektbesitzern unterstützt, tritt ein Fehler auf.

