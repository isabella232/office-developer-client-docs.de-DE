---
title: SetPermissions-Methode (ADOX)
TOCTitle: SetPermissions Method (ADOX)
ms:assetid: 63d1053d-fb32-456b-ae67-3a4e45aa01af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249382(v=office.15)
ms:contentKeyID: 48545274
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 35578de28509e510e9ba5329cfdabc2eff8207b1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475127"
---
# <a name="setpermissions-method-adox"></a>SetPermissions-Methode (ADOX)


**Betrifft**: Access 2013 | Office 2013



Gibt die Berechtigungen für eine Gruppe oder einen Benutzer für ein Objekt an.

## <a name="syntax"></a>Syntax

*Gruppe_oder_benutzer*. SetPermissions*Name*, *ObjectType*, *Action*, *Rechte* \[,*erben* \] \[,*ObjectTypeId*\]

## <a name="parameters"></a>Parameter

  - *Name*

  - Ein **String** -Wert, der den Namen des Objekts angibt, für das Berechtigungen festgelegt werden sollen.

  - *ObjectType*

  - Ein **Long** -Wert, der eine der [ObjectTypeEnum](objecttypeenum.md)-Konstanten sein kann, die den Typ des Objekts angibt, für das die Berechtigungen zurückgegeben werden sollen.

  - *Action*

  - Ein **Long** -Wert, der eine der [ActionEnum](actionenum.md)-Konstanten sein kann, die den Aktionstyp angibt, der beim Festlegen der Berechtigungen ausgeführt werden soll.

  - *Rights*

  - Ein **Long** -Wert, der eine Bitmaske einer oder mehrerer [RightsEnum](rightsenum.md)-Konstanten sein kann, die die festzulegenden Rechte angibt.

  - *Inherit*

  - Optional. Ein **Long** -Wert, der eine der [InheritTypeEnum](inherittypeenum.md)-Konstanten sein kann, die angibt, wie Objekte diese Berechtigungen erben. Der Standardwert lautet **adInheritNone**.

  - *ObjectTypeId*

  - Optional. Ein **Variant** -Wert, der die GUID für einen Anbieterobjekttyp angibt, der nicht durch die OLE DB-Spezifikation definiert ist. Dieser Parameter ist erforderlich, wenn *ObjectType* auf **AdPermObjProviderSpecific**festgelegt ist; Andernfalls wird es nicht verwendet.

## <a name="remarks"></a>Hinweise

Wenn der Anbieter das Festlegen von Zugriffsrechten für Gruppen oder Benutzer nicht unterstützt, tritt ein Fehler auf.


> [!NOTE]
> <P>Beim Aufrufen von SetPermissions werden durch das Festlegen von Actions auf adAccessRevoke alle Einstellungen der Rights-Parameter überschrieben. Legen Sie Actions nicht auf adAccessRevoke fest, wenn die im Rights-Parameter angegebenen Berechtigungen wirksam werden sollen.</P>


