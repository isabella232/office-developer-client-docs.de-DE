---
title: DeleteRule-Eigenschaft (ADOX)
TOCTitle: DeleteRule property (ADOX)
ms:assetid: cd05e024-c1fc-a0b8-8ada-e05ec899c334
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250018(v=office.15)
ms:contentKeyID: 48547752
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cb7d1e5f6a25fc92d43d9e75181a3651a2031856
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294008"
---
# <a name="deleterule-property-adox"></a>DeleteRule-Eigenschaft (ADOX)


**Gilt für**: Access 2013, Office 2013

Gibt die ausgeführte Aktion an, wenn ein Primärschlüssel gelöscht wird.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **Long**-Wert fest und gibt diesen zurück. Der Wert kann eine der [RuleEnum](ruleenum.md)-Konstanten sein kann. Der Standardwert lautet **adRINone**.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist schreibgeschützt für [Key](key-object-adox.md)-Objekte, die bereits an eine Auflistung angefügt wurden.

