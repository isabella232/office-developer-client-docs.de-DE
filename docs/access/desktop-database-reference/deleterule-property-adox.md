---
title: DeleteRule-Eigenschaft (ADOX)
TOCTitle: DeleteRule property (ADOX)
ms:assetid: cd05e024-c1fc-a0b8-8ada-e05ec899c334
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250018(v=office.15)
ms:contentKeyID: 48547752
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3d40e7565b04f3c621dfe0f39ae3a629585224b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928516"
---
# <a name="deleterule-property-adox"></a>DeleteRule-Eigenschaft (ADOX)


**Betrifft**: Access 2013, Office 2013

Gibt die ausgeführte Aktion an, wenn ein Primärschlüssel gelöscht wird.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **Long** -Wert fest und gibt diesen zurück. Der Wert kann einer der [RuleEnum](ruleenum.md)-Konstanten sein. Der Standardwert lautet **adRINone**.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist schreibgeschützt für [Key](key-object-adox.md)-Objekte, die bereits an eine Auflistung angefügt wurden.

