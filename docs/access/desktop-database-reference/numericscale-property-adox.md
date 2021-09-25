---
title: NumericScale-Eigenschaft (ADOX)
TOCTitle: NumericScale property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 17cc0a52a138cf1d16904fc1b7b2bd907a79aba8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615186"
---
# <a name="numericscale-property-adox"></a>NumericScale-Eigenschaft (ADOX)


**Gilt für**: Access 2013, Office 2013

Gibt die Dezimalstelle eines numerischen Werts in der Spalte an.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Sets and returns a **Byte** value that is the scale of data values in the column when the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property is **adNumeric** or **adDecimal**. **NumericScale** is ignored for all other data types.

## <a name="remarks"></a>Bemerkungen

Der Standardwert lautet Null (0).

**NumericScale** ist für [Column](column-object-adox.md)-Objekte, die bereits an eine Auflistung angefügt wurden, schreibgeschützt.

