---
title: Update Resync dynamische-Eigenschaft (ADO)
TOCTitle: Update Resync dynamic property (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 653291ade258d602d7ec523dcac7e9fe51dd91fb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702026"
---
# <a name="update-resync-dynamic-property-ado"></a>Update Resync dynamische-Eigenschaft (ADO)


**Betrifft**: Access 2013, Office 2013

Gibt an, ob auf die [UpdateBatch](updatebatch-method-ado.md)-Methode ein impliziter Vorgang mit einer [Resync](resync-method-ado.md)-Methode folgt. Wenn dies der Fall ist, wird der Bereich des Vorgangs angegeben.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt fest oder gibt mindestens eines der [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) Werte.

## <a name="remarks"></a>Bemerkungen

Die Werte der ADCPROP\_UPDATERESYNC\_ENUM kann kombiniert werden, und abgesehen vom Wert AdResyncAll, der bereits die Kombination der restlichen Werte darstellt.

Mit der **adResyncConflicts** -Konstante werden die Neusynchronisierungswerte als zugrunde liegende Werte gespeichert, aber ausstehende Änderungen werden nicht außer Kraft gesetzt.

**Update Resync** ist eine dynamische Eigenschaft, die an die [Properties](recordset-object-ado.md)-Auflistung des [Recordset](properties-collection-ado.md)-Objekts angefügt wird, wenn die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt ist.

