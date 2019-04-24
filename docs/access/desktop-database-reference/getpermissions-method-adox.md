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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292244"
---
# <a name="getpermissions-method-adox"></a>GetPermissions-Methode (ADOX)

**Gilt für**: Access 2013, Office 2013

Gibt die Berechtigungen einer Gruppe oder eines Benutzers für ein Objekt oder einen Objektcontainers zurück.

## <a name="syntax"></a>Syntax

*ReturnValue* = *GroupOrUser*. GetPermissions (*Name*, *Objekttyp* \[, objecttypecode)**\]

## <a name="return-value"></a>Rückgabewert

Gibt einen **Long**-Wert zurück, der eine Bitmaske angibt, die die Berechtigungen enthält, über die die Gruppe oder der Benutzer für das Objekt verfügen. Dieser Wert kann eine bzw. mehrere der [RightsEnum](rightsenum.md)-Konstanten sein.

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Name* |Ein **Variant**-Wert, der den Namen des Objekts angibt, für das Berechtigungen festgelegt werden sollen. Legen Sie *Name* auf einen Nullwert fest, wenn Sie die Berechtigungen für den Objektcontainer abrufen möchten.|
|*ObjectType* |Ein **Long** -Wert, der eine der [ObjectTypeEnum](objecttypeenum.md)-Konstanten sein kann, die den Typ des Objekts angibt, für das die Berechtigungen zurückgegeben werden sollen.|
|*ObjectType* |Optional. Ein **Variant**-Wert, der die GUID für einen Anbieterobjekttyp angibt, der nicht durch die OLE DB-Spezifikation definiert ist. Dieser Parameter ist erforderlich, wenn *ObjectType* auf **adPermObjProviderSpecific** festgelegt ist.Andernfalls wird dieser Parameter nicht verwendet.|

