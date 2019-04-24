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
# <a name="setpermissions-method-adox"></a>SetPermissions-Methode (ADOX)

**Gilt für**: Access 2013, Office 2013

Gibt die Berechtigungen für eine Gruppe oder einen Benutzer für ein Objekt an.

## <a name="syntax"></a>Syntax

*GroupOrUser*. SetPermissions*Name*, ObjectType, *Action*, *Rights* \[,*inherit* \] \[, ** objecttyper**\]

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Name* |Ein **String** -Wert, der den Namen des Objekts angibt, für das Berechtigungen festgelegt werden sollen.|
|*ObjectType* |Ein **Long** -Wert, der eine der [ObjectTypeEnum](objecttypeenum.md)-Konstanten sein kann, die den Typ des Objekts angibt, für das die Berechtigungen zurückgegeben werden sollen.|
|*Action* |Ein **Long** -Wert, der eine der [ActionEnum](actionenum.md)-Konstanten sein kann, die den Aktionstyp angibt, der beim Festlegen der Berechtigungen ausgeführt werden soll.|
|*Rights* |Ein **Long** -Wert, der eine Bitmaske einer oder mehrerer [RightsEnum](rightsenum.md)-Konstanten sein kann, die die festzulegenden Rechte angibt.|
|*Inherit* |Optional. Ein **Long** -Wert, der eine der [InheritTypeEnum](inherittypeenum.md)-Konstanten sein kann, die angibt, wie Objekte diese Berechtigungen erben. Der Standardwert lautet **adInheritNone**.|
|*ObjectType* |Optional. Ein **Variant**-Wert, der die GUID für einen Anbieterobjekttyp angibt, der nicht durch die OLE DB-Spezifikation definiert ist. Dieser Parameter ist erforderlich, wenn *ObjectType* auf **adPermObjProviderSpecific** festgelegt ist. Andernfalls wird dieser Parameter nicht verwendet.|

## <a name="remarks"></a>Bemerkungen

Wenn der Anbieter das Festlegen von Zugriffsrechten für Gruppen oder Benutzer nicht unterstützt, tritt ein Fehler auf.

> [!NOTE]
> Wenn Sie **** SetPermissions aufrufen, werden beim Festlegen von Aktionen auf **adAccessRevoke** alle Einstellungen des *Rights* -Parameters überschrieben. Legen Sie keine *Aktionen* auf **adAccessRevoke** fest, wenn die im *Rights* -Parameter angegebenen Rechte wirksam werden sollen.


