---
title: NumericScale-Eigenschaft (ADOX)
TOCTitle: NumericScale property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d706bad7d1f605933a951498705657c3c454a2d6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709054"
---
# <a name="numericscale-property-adox"></a>NumericScale-Eigenschaft (ADOX)


**Betrifft**: Access 2013, Office 2013

Gibt die Dezimalstelle eines numerischen Werts in der Spalte an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen Byte-Wert fest bzw. gibt einen Byte-Wert zurück, der als Skala der Datenwerte in der Spalte dient, wenn die Type-Eigenschaft auf adNumeric oder adDecimal festgelegt ist. NumericScale wird für alle anderen Datentypen ignoriert.

## <a name="remarks"></a>Hinweise

Der Standardwert lautet Null (0).

**NumericScale** ist für [Column](column-object-adox.md)-Objekte, die bereits an eine Auflistung angefügt wurden, schreibgeschützt.

