---
title: Update Resync (dynamische Eigenschaft) (ADO)
TOCTitle: Update Resync Property--Dynamic (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 16600f22084718a6b32656ebfc56d6a9be06c676
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474210"
---
# <a name="update-resync-property--dynamic-ado"></a>Update Resync (dynamische Eigenschaft) (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt an, ob auf die [UpdateBatch](updatebatch-method-ado.md)-Methode ein impliziter Vorgang mit einer [Resync](resync-method-ado.md)-Methode folgt. Wenn dies der Fall ist, wird der Bereich des Vorgangs angegeben.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt fest oder gibt mindestens eines der [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) Werte.

## <a name="remarks"></a>Hinweise

Die Werte der ADCPROP\_UPDATERESYNC\_ENUM kann kombiniert werden, und abgesehen vom Wert AdResyncAll, der bereits die Kombination der restlichen Werte darstellt.

Mit der **adResyncConflicts** -Konstante werden die Neusynchronisierungswerte als zugrunde liegende Werte gespeichert, aber ausstehende Änderungen werden nicht außer Kraft gesetzt.

**Update Resync** ist eine dynamische Eigenschaft, die an die [Properties](recordset-object-ado.md)-Auflistung des [Recordset](properties-collection-ado.md)-Objekts angefügt wird, wenn die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt ist.

