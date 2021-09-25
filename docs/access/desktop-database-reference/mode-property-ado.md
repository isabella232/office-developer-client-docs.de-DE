---
title: Mode-Eigenschaft (ADO)
TOCTitle: Mode property (ADO)
ms:assetid: 62086f4f-8624-16c4-dae1-a17475d1864d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249365(v=office.15)
ms:contentKeyID: 48545227
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 166f214eb43cb8aafed63e1f17a013a71d51ac08
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606583"
---
# <a name="mode-property-ado"></a>Mode-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Es werden die verfügbaren Berechtigungen zum Ändern von Daten in einem [Connection](connection-object-ado.md)-, [Record](record-object-ado.md)- oder [Stream](stream-object-ado.md)-Objekt angegeben.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen [ConnectModeEnum](connectmodeenum.md)-Wert fest oder gibt den Wert zurück. Der Standardwert für ein **Connection**-Objekt ist **adModeUnknown**. Der Standardwert für ein **Record**-Objekt ist **adModeRead**. Der Standardwert für ein **Stream**-Objekt, das mit einer zugrunde liegenden Quelle (geöffnet mit einer URL als Quelle oder als **Stream**-Objekt eines **Record**-Objekts) verknüpft ist, lautet **adModeRead**. Der Standardwert für ein **Stream**-Objekt, das nicht mit einer zugrunde liegenden Quelle verknüpft ist (im Speicher instanziiert), lautet **adModeUnknown**.

## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie die **Mode** -Eigenschaft, um die von einem Anbieter mit der aktuellen Verbindung verwendeten Zugriffsberechtigungen festzulegen oder zurückzugeben. Die **Mode** -Eigenschaft kann nur bei geschlossenem **Connection** -Objekt festgelegt werden.

Wenn Sie den Zugriffsmodus bei einem **Stream** -Objekt nicht angeben, wird er von der zum Öffnen des **Stream** -Objekts verwendeten Quelle vererbt. Angenommen, Sie öffnen ein **Stream** -Objekt aus einem **Record** -Objekt, dann wird es standardmäßig in demselben Modus wie das **Record** -Objekt geöffnet.

Die Eigenschaft ist nicht schreibgeschützt, wenn das Objekt geschlossen ist, und schreibgeschützt, wenn es geöffnet ist.

**Remote data service usage** Wenn sie für ein clientseitiges Connection -Objekt verwendet wird, kann die **Mode-Eigenschaft** nur auf **adModeUnknown** festgelegt werden.

