---
title: Precision-Eigenschaft (ADOX)
TOCTitle: Precision property (ADOX)
ms:assetid: 5d8ca497-572a-52e0-18aa-f82deaea0813
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249330(v=office.15)
ms:contentKeyID: 48545117
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: fe859810252376024ebaa327a9203309d4bb8cd7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622116"
---
# <a name="precision-property-adox"></a>Precision-Eigenschaft (ADOX)


**Gilt für**: Access 2013, Office 2013

Gibt die maximale Genauigkeit von Datenwerten in der Spalte an.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Legt einen **Long**-Wert fest bzw. gibt diesen zurück. Der Wert ist die maximale Genauigkeit von Datenwerten in der Spalte, wenn die [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox)-Eigenschaft ein numerischer Typ ist. **Precision** wird für alle anderen Datentypen ignoriert.

## <a name="remarks"></a>Bemerkungen

Der Standardwert lautet Null (0).

Diese Eigenschaft ist schreibgeschützt für [Column](column-object-adox.md)-Objekte, die bereits an eine Auflistung angefügt wurden.

