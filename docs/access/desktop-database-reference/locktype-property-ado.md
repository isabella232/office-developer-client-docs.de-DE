---
title: LockType-Eigenschaft (ADO)
TOCTitle: LockType property (ADO)
ms:assetid: 1d2622dc-6cab-1b7f-98a8-97a41d5c047f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248965(v=office.15)
ms:contentKeyID: 48543589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d12946a90d61a941bf5ef7d479970c8c96e074f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289843"
---
# <a name="locktype-property-ado"></a>LockType-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt den Typ der Sperren an, die bei der Bearbeitung auf Datensätze angewendet werden.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen [LockTypeEnum](locktypeenum.md)-Wert fest oder gibt den Wert zurück. Der Standardwert ist **adLockReadOnly**.

## <a name="remarks"></a>Bemerkungen

Legen Sie die **LockType** -Eigenschaft fest, bevor Sie ein [Recordset](recordset-object-ado.md) öffnen, und geben Sie den Sperrtyp an, den der Anbieter beim Öffnen verwenden soll. Lesen Sie die Eigenschaft, um den Sperrtyp zu ermitteln, der bei einem geöffneten **Recordset** -Objekt verwendet wird.

Anbieter unterstützen möglicherweise nicht alle Sperrtypen. Falls ein Anbieter die angeforderte **LockType** -Einstellung nicht unterstützt, wird der Sperrtyp ausgetauscht. Wenn Sie die Sperrfunktionalität ermitteln möchten, die tatsächlich für ein **Recordset** -Objekt verfügbar ist, verwenden Sie die [Supports](supports-method-ado.md)-Methode mit **adUpdate** und **adUpdateBatch**.

Die Einstellung **adLockPessimistic** wird nicht unterstützt, wenn die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt ist. Wurde ein nicht unterstützter Wert festgelegt, tritt kein Fehler auf. Stattdessen wird der nächstliegende unterstützte **LockType** -Wert verwendet.

Die **LockType** -Eigenschaft ist nicht schreibgeschützt, wenn das **Recordset** -Objekt geschlossen ist, und schreibgeschützt, wenn es geöffnet ist.

**Remote Data Service-Verwendung** Bei Verwendung in einem clientseitigen Recordset-Objekt kann **** die LockType-Eigenschaft nur auf **adLockBatchOptimistic**festgelegt werden.

