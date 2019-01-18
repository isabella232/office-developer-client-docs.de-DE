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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720030"
---
# <a name="deleterule-property-adox"></a>DeleteRule-Eigenschaft (ADOX)


**Betrifft**: Access 2013, Office 2013

Gibt die ausgeführte Aktion an, wenn ein Primärschlüssel gelöscht wird.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **Long** -Wert fest und gibt diesen zurück. Der Wert kann einer der [RuleEnum](ruleenum.md)-Konstanten sein. Der Standardwert lautet **adRINone**.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist schreibgeschützt für [Key](key-object-adox.md)-Objekte, die bereits an eine Auflistung angefügt wurden.

