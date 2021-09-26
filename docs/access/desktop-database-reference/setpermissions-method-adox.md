---
title: SetPermissions-Methode (ADOX)
TOCTitle: SetPermissions method (ADOX)
ms:assetid: 63d1053d-fb32-456b-ae67-3a4e45aa01af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249382(v=office.15)
ms:contentKeyID: 48545274
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4e9dc5b2f0c1501dd313a0f70c241d8dfa7fbe59
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621843"
---
# <a name="setpermissions-method-adox"></a>SetPermissions-Methode (ADOX)

**Gilt für**: Access 2013, Office 2013

Gibt die Berechtigungen für eine Gruppe oder einen Benutzer für ein Objekt an.

## <a name="syntax"></a>Syntax

*GroupOrUser*. SetPermissions *Name*, *ObjectType*, *Action*, *Rights* \[ ,*Inherit* \] \[ ,*ObjectTypeId*\]

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Name* |Ein **String** -Wert, der den Namen des Objekts angibt, für das Berechtigungen festgelegt werden sollen.|
|*ObjectType* |Ein **Long** -Wert, der eine der [ObjectTypeEnum](objecttypeenum.md)-Konstanten sein kann, die den Typ des Objekts angibt, für das die Berechtigungen zurückgegeben werden sollen.|
|*Action* |Ein **Long** -Wert, der eine der [ActionEnum](actionenum.md)-Konstanten sein kann, die den Aktionstyp angibt, der beim Festlegen der Berechtigungen ausgeführt werden soll.|
|*Rights* |Ein **Long** -Wert, der eine Bitmaske einer oder mehrerer [RightsEnum](rightsenum.md)-Konstanten sein kann, die die festzulegenden Rechte angibt.|
|*Inherit* |Optional. Ein **Long** -Wert, der eine der [InheritTypeEnum](inherittypeenum.md)-Konstanten sein kann, die angibt, wie Objekte diese Berechtigungen erben. Der Standardwert lautet **adInheritNone**.|
|*ObjectTypeId* |Optional. Ein **Variant**-Wert, der die GUID für einen Anbieterobjekttyp angibt, der nicht durch die OLE DB-Spezifikation definiert ist. Dieser Parameter ist erforderlich, wenn *ObjectType* auf **adPermObjProviderSpecific** festgelegt ist. Andernfalls wird dieser Parameter nicht verwendet.|

## <a name="remarks"></a>Bemerkungen

Wenn der Anbieter das Festlegen von Zugriffsrechten für Gruppen oder Benutzer nicht unterstützt, tritt ein Fehler auf.

> [!NOTE]
> Beim Aufrufen von **SetPermissions** überschreibt das Festlegen von Aktionen auf **"adAccessRevoke"** alle Einstellungen des *Parameters "Rights".* Legen Sie *"Actions"* nicht auf **"adAccessRevoke"** fest, wenn die im Parameter *"Rights"* angegebenen Rechte wirksam werden sollen.


