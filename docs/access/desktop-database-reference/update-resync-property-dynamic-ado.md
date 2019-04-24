---
title: Update Resync Dynamic-Eigenschaft (ADO)
TOCTitle: Update Resync dynamic property (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 653291ade258d602d7ec523dcac7e9fe51dd91fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308344"
---
# <a name="update-resync-dynamic-property-ado"></a>Update Resync Dynamic-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Es wird angegeben, ob auf die [UpdateBatch](updatebatch-method-ado.md)-Methode eine implizite [Resync](resync-method-ado.md)-Methodenoperation folgt, und es wird gegebenenfalls der Umfang der Operation angegeben.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen oder mehrere [ADCPROP\_-UPDATERESYNC\_-Enumerationswerte](adcprop-updateresync-enum.md) fest oder gibt diesen zurück.

## <a name="remarks"></a>Bemerkungen

Die Werte der ADCPROP\_UPDATERESYNC\_-Enumeration können kombiniert werden, mit Ausnahme von adResyncAll, die bereits die Kombination der restlichen Werte darstellt.

Mit der **adResyncConflicts** -Konstante werden die Neusynchronisierungswerte als zugrunde liegende Werte gespeichert, aber ausstehende Änderungen werden nicht außer Kraft gesetzt.

**Update Resync** ist eine dynamische Eigenschaft, die an die [Properties](recordset-object-ado.md)-Auflistung des [Recordset](properties-collection-ado.md)-Objekts angefügt wird, wenn die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt ist.

