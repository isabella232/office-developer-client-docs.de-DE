---
title: StayInSync-Eigenschaft (ADO)
TOCTitle: StayInSync property (ADO)
ms:assetid: 02c95c10-4032-14e1-e506-f334a8787142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15)
ms:contentKeyID: 48542966
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d5e9782fa9ff94c8fe40f10ed4a73aa1362d5c03
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568362"
---
# <a name="stayinsync-property-ado"></a>StayInSync-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt in einem hierarchischen [Recordset-Objekt](recordset-object-ado.md) an, ob sich der Verweis auf die zugrunde liegenden untergeordneten Datensätze (d. h. das *Kapitel)* ändert, wenn sich die Position der übergeordneten Zeile ändert.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Legt einen **Boolean**-Wert fest oder gibt den Wert zurück. Der Standardwert lautet **True**. Wenn **True** festgelegt ist, wird das Kapitel bei einer Änderung der Zeilenposition des übergeordneten **Recordset**-Objekts aktualisiert. Ist **False** festgelegt, verweist das Kapitel weiterhin auf Daten im vorherigen Kapitel, auch wenn sich die Zeilenposition des übergeordneten **Recordset**-Objekts geändert hat.

## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft gilt für hierarchische Recordsets wie diejenigen, die vom [Microsoft Data Shaping Dienst für OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) unterstützt werden. Die Eigenschaft muss für das übergeordnete **Recordset**-Objekt festgelegt werden, bevor das untergeordnete **Recordset**-Objekt abgerufen wird. Das Navigieren in hierarchischen Recordsets wird mit dieser Eigenschaft vereinfacht.

