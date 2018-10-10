---
title: DeleteRule-Eigenschaft (ADOX)
TOCTitle: DeleteRule Property (ADOX)
ms:assetid: cd05e024-c1fc-a0b8-8ada-e05ec899c334
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250018(v=office.15)
ms:contentKeyID: 48547752
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: beb13efbf41f90763685757964c80fce6ce38927
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475089"
---
# <a name="deleterule-property-adox"></a>DeleteRule-Eigenschaft (ADOX)


**Betrifft**: Access 2013 | Office 2013

Gibt die ausgeführte Aktion an, wenn ein Primärschlüssel gelöscht wird.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **Long** -Wert fest und gibt diesen zurück. Der Wert kann einer der [RuleEnum](ruleenum.md)-Konstanten sein. Der Standardwert lautet **adRINone**.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist schreibgeschützt für [Key](key-object-adox.md)-Objekte, die bereits an eine Auflistung angefügt wurden.

