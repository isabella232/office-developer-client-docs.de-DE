---
title: UpdateRule-Eigenschaft (ADOX)
TOCTitle: UpdateRule property (ADOX)
ms:assetid: edefa80a-b83b-e811-996c-6f0318722c84
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250206(v=office.15)
ms:contentKeyID: 48548548
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4c375a4eb9931008ea9753181b44aa5509377d11
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726232"
---
# <a name="updaterule-property-adox"></a>UpdateRule-Eigenschaft (ADOX)


**Betrifft**: Access 2013, Office 2013

Gibt die Aktion an, die bei der Aktualisierung eines Primärschlüssels ausgeführt wurde.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **Long** -Wert fest und gibt diesen zurück. Der Wert kann einer der [RuleEnum](ruleenum.md)-Konstanten sein. Der Standardwert lautet **adRINone**.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist schreibgeschützt für [Key](key-object-adox.md)-Objekte, die bereits an die Auflistung angefügt wurden.

