---
title: StayInSync-Eigenschaft (ADO)
TOCTitle: StayInSync Property (ADO)
ms:assetid: 02c95c10-4032-14e1-e506-f334a8787142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15)
ms:contentKeyID: 48542966
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f492b2c3f58084be55eca4787cde486dab29ca67
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474590"
---
# <a name="stayinsync-property-ado"></a>StayInSync-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt an, in einem hierarchischen [Recordset](recordset-object-ado.md) -Objekt, ob der Verweis auf die zugrunde liegenden untergeordneten Datensätze (d. h., das *Kapitel*) ändert, wenn die Position der übergeordneten Zeile geändert wird.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **Boolean** -Wert fest oder gibt den Wert zurück. Der Standardwert lautet **True**. Wenn **True** festgelegt ist, wird das Kapitel bei einer Änderung der Zeilenposition des übergeordneten **Recordset** -Objekts aktualisiert. Ist **False** festgelegt, verweist das Kapitel weiterhin auf Daten im vorherigen Kapitel, auch wenn sich die Zeilenposition des übergeordneten **Recordset** -Objekts geändert hat.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft gilt für hierarchische Recordsets wie diejenigen, die vom [Microsoft Data Shaping Dienst für OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) unterstützt werden. Die Eigenschaft muss für das übergeordnete **Recordset** -Objekt festgelegt werden, bevor das untergeordnete **Recordset** -Objekt abgerufen wird. Das Navigieren in hierarchischen Recordsets wird mit dieser Eigenschaft vereinfacht.

