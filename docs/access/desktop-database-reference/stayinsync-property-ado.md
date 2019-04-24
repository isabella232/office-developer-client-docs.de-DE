---
title: StayInSync-Eigenschaft (ADO)
TOCTitle: StayInSync property (ADO)
ms:assetid: 02c95c10-4032-14e1-e506-f334a8787142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15)
ms:contentKeyID: 48542966
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bfc9ef5229fe230ad0c83ebde7a887e0fac0c233
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308491"
---
# <a name="stayinsync-property-ado"></a>StayInSync-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt in einem hierarchischen [Recordset](recordset-object-ado.md) -Objekt an, ob sich der Verweis auf die zugrunde liegenden untergeordneten Datensätze (also das *Kapitel*) ändert, wenn die übergeordnete Zeilenposition geändert wird.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **Boolean**-Wert fest oder gibt den Wert zurück. Der Standardwert lautet **True**. Wenn **True** festgelegt ist, wird das Kapitel bei einer Änderung der Zeilenposition des übergeordneten **Recordset**-Objekts aktualisiert. Ist **False** festgelegt, verweist das Kapitel weiterhin auf Daten im vorherigen Kapitel, auch wenn sich die Zeilenposition des übergeordneten **Recordset**-Objekts geändert hat.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gilt für hierarchische Recordsets wie diejenigen, die vom [Microsoft Data Shaping Dienst für OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) unterstützt werden. Die Eigenschaft muss für das übergeordnete **Recordset**-Objekt festgelegt werden, bevor das untergeordnete **Recordset**-Objekt abgerufen wird. Das Navigieren in hierarchischen Recordsets wird mit dieser Eigenschaft vereinfacht.

