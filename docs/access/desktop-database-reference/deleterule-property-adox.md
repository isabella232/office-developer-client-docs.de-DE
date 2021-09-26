---
title: DeleteRule-Eigenschaft (ADOX)
TOCTitle: DeleteRule property (ADOX)
ms:assetid: cd05e024-c1fc-a0b8-8ada-e05ec899c334
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250018(v=office.15)
ms:contentKeyID: 48547752
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: fdad6d240bba087b6786683ec32b44e8493c88b7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618238"
---
# <a name="deleterule-property-adox"></a>DeleteRule-Eigenschaft (ADOX)


**Gilt für**: Access 2013, Office 2013

Gibt die ausgeführte Aktion an, wenn ein Primärschlüssel gelöscht wird.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Legt einen **Long**-Wert fest und gibt diesen zurück. Der Wert kann eine der [RuleEnum](ruleenum.md)-Konstanten sein kann. Der Standardwert lautet **adRINone**.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist schreibgeschützt für [Key](key-object-adox.md)-Objekte, die bereits an eine Auflistung angefügt wurden.

